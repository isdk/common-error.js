[**@isdk/common-error**](../README.md)

***

[@isdk/common-error](../globals.md) / CommonError

# Class: CommonError

Defined in: [packages/common-error/src/base-error.ts:166](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L166)

BaseError class that extends the Error class.

## Example

```ts
// Create a custom error
class CustomError extends BaseError {
  static code = 'customError';
  constructor(message: string) {
    super(message);
  }
}

// Throw the custom error
throw new CustomError('This is a custom error');
```

## Description

This class is used to create custom errors that extend the built-in Error class. It provides a way to define custom error codes and additional data associated with the error.

## Method

toJSON - Returns a JSON representation of the error.

## Method

fromJSON - Creates a new BaseError instance from a JSON representation.

## Extends

- [`BaseError`](BaseError.md)

## Extended by

- [`NotImplementationError`](NotImplementationError.md)
- [`NotFoundError`](NotFoundError.md)
- [`AlreadyExistsError`](AlreadyExistsError.md)
- [`AbortError`](AbortError.md)

## Constructors

### new CommonError()

> **new CommonError**(`message`, `name`?, `status`?): [`CommonError`](CommonError.md)

Defined in: [packages/common-error/src/base-error.ts:174](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L174)

#### Parameters

##### message

`string`

##### name?

`string` | `Record`\<`string`, `any`\>

##### status?

[`ErrorCodeType`](../type-aliases/ErrorCodeType.md) = `InternalErrorCode`

#### Returns

[`CommonError`](CommonError.md)

#### Overrides

[`BaseError`](BaseError.md).[`constructor`](BaseError.md#constructors)

## Properties

### caller

> **caller**: `string`

Defined in: [packages/common-error/src/base-error.ts:66](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L66)

The name of the function that threw the error.

#### Inherited from

[`BaseError`](BaseError.md).[`caller`](BaseError.md#caller)

***

### code

> **code**: [`ErrorCodeType`](../type-aliases/ErrorCodeType.md)

Defined in: [packages/common-error/src/base-error.ts:67](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L67)

the error code

#### Inherited from

[`BaseError`](BaseError.md).[`code`](BaseError.md#code-1)

***

### data?

> `optional` **data**: `any`

Defined in: [packages/common-error/src/base-error.ts:68](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L68)

Additional data associated with the error.

#### Inherited from

[`BaseError`](BaseError.md).[`data`](BaseError.md#data)

***

### message

> **message**: `string`

Defined in: node\_modules/.pnpm/typescript@5.7.3/node\_modules/typescript/lib/lib.es5.d.ts:1077

#### Inherited from

[`BaseError`](BaseError.md).[`message`](BaseError.md#message-1)

***

### name

> **name**: `string`

Defined in: node\_modules/.pnpm/typescript@5.7.3/node\_modules/typescript/lib/lib.es5.d.ts:1076

#### Inherited from

[`BaseError`](BaseError.md).[`name`](BaseError.md#name-1)

***

### stack?

> `optional` **stack**: `string`

Defined in: node\_modules/.pnpm/typescript@5.7.3/node\_modules/typescript/lib/lib.es5.d.ts:1078

#### Inherited from

[`BaseError`](BaseError.md).[`stack`](BaseError.md#stack)

***

### code

> `static` **code**: [`ErrorCodeType`](../type-aliases/ErrorCodeType.md)

Defined in: [packages/common-error/src/base-error.ts:65](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L65)

The error code associated with the error.

#### Inherited from

[`BaseError`](BaseError.md).[`code`](BaseError.md#code-2)

***

### prepareStackTrace()?

> `static` `optional` **prepareStackTrace**: (`err`, `stackTraces`) => `any`

Defined in: node\_modules/.pnpm/@types+node@22.13.10/node\_modules/@types/node/globals.d.ts:143

Optional override for formatting stack traces

#### Parameters

##### err

`Error`

##### stackTraces

`CallSite`[]

#### Returns

`any`

#### See

https://v8.dev/docs/stack-trace-api#customizing-stack-traces

#### Inherited from

[`BaseError`](BaseError.md).[`prepareStackTrace`](BaseError.md#preparestacktrace)

***

### stackTraceLimit

> `static` **stackTraceLimit**: `number`

Defined in: node\_modules/.pnpm/@types+node@22.13.10/node\_modules/@types/node/globals.d.ts:145

#### Inherited from

[`BaseError`](BaseError.md).[`stackTraceLimit`](BaseError.md#stacktracelimit)

## Methods

### fromJSON()

> **fromJSON**(`json`): [`BaseError`](BaseError.md)

Defined in: [packages/common-error/src/base-error.ts:161](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L161)

#### Parameters

##### json

`any`

#### Returns

[`BaseError`](BaseError.md)

#### Inherited from

[`BaseError`](BaseError.md).[`fromJSON`](BaseError.md#fromjson)

***

### toJSON()

> **toJSON**(): `any`

Defined in: [packages/common-error/src/base-error.ts:121](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L121)

Returns a JSON representation of the error.

#### Returns

`any`

A JSON representation of the error.

#### Inherited from

[`BaseError`](BaseError.md).[`toJSON`](BaseError.md#tojson)

***

### captureStackTrace()

> `static` **captureStackTrace**(`targetObject`, `constructorOpt`?): `void`

Defined in: node\_modules/.pnpm/@types+node@22.13.10/node\_modules/@types/node/globals.d.ts:136

Create .stack property on a target object

#### Parameters

##### targetObject

`object`

##### constructorOpt?

`Function`

#### Returns

`void`

#### Inherited from

[`BaseError`](BaseError.md).[`captureStackTrace`](BaseError.md#capturestacktrace)

***

### create()

> `static` **create**(`__namedParameters`): [`CommonError`](CommonError.md)

Defined in: [packages/common-error/src/base-error.ts:167](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L167)

#### Parameters

##### \_\_namedParameters

###### code?

`string` \| `number`

###### data?

`any`

###### error

`string`

###### name?

`string`

#### Returns

[`CommonError`](CommonError.md)

#### Overrides

[`BaseError`](BaseError.md).[`create`](BaseError.md#create)

***

### createErrorClass()

> `static` **createErrorClass**(`aType`, `aErrorCode`?, `ParentErrorClass`?): *typeof* [`BaseError`](BaseError.md)

Defined in: [packages/common-error/src/base-error.ts:70](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L70)

Create an Error Class

#### Parameters

##### aType

`string`

the error type(class) name

##### aErrorCode?

`string` | `number` | *typeof* `AbstractError`

##### ParentErrorClass?

*typeof* [`BaseError`](BaseError.md) = `BaseError`

the parent error class. defaults to AbstractError

#### Returns

*typeof* [`BaseError`](BaseError.md)

the new Error Class

#### Inherited from

[`BaseError`](BaseError.md).[`createErrorClass`](BaseError.md#createerrorclass)

***

### fromJSON()

> `static` **fromJSON**(`json`): [`BaseError`](BaseError.md)

Defined in: [packages/common-error/src/base-error.ts:151](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L151)

Creates a new error instance from a JSON representation.
This method is useful for deserializing an error that was serialized with `toJSON`.

#### Parameters

##### json

`any`

A JSON object representing the error.

#### Returns

[`BaseError`](BaseError.md)

A new instance of the error class (or a subclass).

#### Example

```ts
const originalError = new NotFoundError('thing');
const json = originalError.toJSON();

// Deserialize
const newError = NotFoundError.fromJSON(json);
console.log(newError instanceof NotFoundError); // true
console.log(newError.message); // 'Could not find thing.'
```

#### Inherited from

[`BaseError`](BaseError.md).[`fromJSON`](BaseError.md#fromjson-2)
