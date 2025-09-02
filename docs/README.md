**@isdk/common-error**

***

# @isdk/common-error

[![npm version](https://img.shields.io/npm/v/@isdk/common-error.svg)](https://www.npmjs.com/package/@isdk/common-error)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A lightweight, extensible error handling library for TypeScript and JavaScript projects. It provides a `BaseError` class that makes it easy to create custom, structured error types with support for error codes and additional metadata.

This library is built upon `abstract-error`.

## Features

- **Extensible:** Easily create your own custom error classes by extending `BaseError`.
- **Structured Errors:** Attach error codes and custom data to your error objects for better error handling and logging.
- **Pre-defined Errors:** Comes with a set of common error types like `NotFoundError`, `AlreadyExistsError`, `NotImplementationError`, and `AbortError`.
- **JSON Serialization:** Convert error objects to and from JSON for easy transport over networks or for logging purposes.
- **TypeScript Support:** Written in TypeScript, with full type definitions.

## Installation

Using npm:

```bash
npm install @isdk/common-error
```

Using yarn:

```bash
yarn add @isdk/common-error
```

## Usage

### Creating a Custom Error

You can easily create your own error classes by extending `BaseError`.

```typescript
import { BaseError } from '@isdk/common-error';

class MyCustomError extends BaseError {
  constructor(message: string, public customData: { reason: string }) {
    super(message, 'MyCustomErrorCode'); // message and error code
    this.data = customData;
  }
}

try {
  throw new MyCustomError('Something went wrong!', { reason: 'internal failure' });
} catch (error) {
  if (error instanceof MyCustomError) {
    console.error(error.toJSON());
    // {
    //   name: 'MyCustomError',
    //   code: 'MyCustomErrorCode',
    //   data: { reason: 'internal failure' },
    //   error: 'Something went wrong!',
    //   stack: '...'
    // }
  }
}
```

### Using Pre-defined Errors

The library includes several common error types out of the box.

```typescript
import { NotFoundError, AlreadyExistsError, NotImplementationError, AbortError } from '@isdk/common-error';

// NotFoundError
try {
  throw new NotFoundError('User');
} catch (e) {
  // e.message will be "Could not find User."
  // e.code will be 404
}

// AlreadyExistsError
try {
  throw new AlreadyExistsError('Project');
} catch (e) {
  // e.message will be "The Project already exists."
  // e.code will be 409
}

// NotImplementationError
try {
  throw new NotImplementationError();
} catch (e) {
  // e.message will be "Not Implementation."
  // e.code will be 501
}

// AbortError
try {
  throw new AbortError('data processing');
} catch (e) {
  // e.message will be "The operation was aborted for data processing."
  // e.code will be 499
}
```

## API Reference

### `BaseError`

The core class of the library.

#### `new BaseError(message: string, code?: ErrorCodeType, name?: string | Record<string, any>)`

- `message`: The error message.
- `code` (optional): An error code (string or number). Defaults to the class name.
- `name` (optional): The error name. Can also be an object to assign additional properties to the error instance.

#### `error.toJSON()`

Returns a serializable JSON object representing the error.

#### `static BaseError.fromJSON(json)`

Creates a new error instance from a JSON representation. This is the reverse of `toJSON()` and is useful for deserializing errors.

- `json`: A JSON object, typically from a serialized error.

```typescript
import { NotFoundError } from '@isdk/common-error';

const originalError = new NotFoundError('thing');
const json = originalError.toJSON();

// Deserialize the error
const newError = NotFoundError.fromJSON(json);

console.log(newError instanceof NotFoundError); // true
console.log(newError.message); // 'Could not find thing.'
```

#### `static BaseError.create({error: message, code?, name?, data?})`

Static method to create a new instance of the error class.

```typescript
const err = BaseError.create({error: 'hello message', code: ErrorCode.NotFound});
// err is an instance of BaseError
```

#### `static BaseError.createErrorClass(aType: string, aErrorCode?: number|string, ParentErrorClass?: typeof BaseError)`

Static method to dynamically create a new Error class that inherits from `ParentErrorClass` (which defaults to `BaseError`).

```typescript
const DatabaseError = BaseError.createErrorClass('DatabaseError', 'DB_ERROR');
const dbErr = new DatabaseError('Connection failed');
console.log(dbErr.name); // 'DatabaseError'
console.log(dbErr.code); // 'DB_ERROR'
```

### Pre-defined Error Classes

All pre-defined error classes inherit from `CommonError`, which itself inherits from `BaseError`.

- `CommonError`: A general-purpose error class.
- `NotImplementationError`: For features that are not yet implemented. (Code: `501`)
- `NotFoundError`: When a resource is not found. (Code: `404`)
- `AlreadyExistsError`: When a resource already exists. (Code: `409`)
- `AbortError`: When an operation is aborted. (Code: `499`)

### Helper Functions

#### `createError(message: string, name?: string, status?: ErrorCodeType)`

Creates and returns an error instance. It will try to pick the most appropriate error class based on the `status` code.

```typescript
const err = createError('Could not find it.', undefined, ErrorCode.NotFound);
// err is an instance of NotFoundError
```

#### `throwError(message: string, name?: string, status?: ErrorCodeType)`

Creates and immediately throws an error.

```typescript
try {
  throwError('Could not find it.', undefined, ErrorCode.NotFound);
} catch (e) {
  // e is an instance of NotFoundError
}
```

### `ErrorCode`

An enum of common HTTP status codes used as error codes.

```typescript
import { ErrorCode } from '@isdk/common-error';

console.log(ErrorCode.NotFound); // 404
console.log(ErrorCode.InternalError); // 500
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License.
