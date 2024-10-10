[**@isdk/common-error**](../README.md) • **Docs**

***

[@isdk/common-error](../globals.md) / CommonError

# Class: CommonError

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

#### Parameters

• **message**: `string`

• **name?**: `string` \| `Record`\<`string`, `any`\>

• **status?**: [`ErrorCodeType`](../type-aliases/ErrorCodeType.md) = `InternalErrorCode`

#### Returns

[`CommonError`](CommonError.md)

#### Overrides

[`BaseError`](BaseError.md).[`constructor`](BaseError.md#constructors)

#### Defined in

[packages/common-error/src/base-error.ts:153](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L153)

## Properties

### caller

> **caller**: `string`

The name of the function that threw the error.

#### Inherited from

[`BaseError`](BaseError.md).[`caller`](BaseError.md#caller)

#### Defined in

[packages/common-error/src/base-error.ts:66](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L66)

***

### code

> **code**: [`ErrorCodeType`](../type-aliases/ErrorCodeType.md)

the error code

#### Inherited from

[`BaseError`](BaseError.md).[`code`](BaseError.md#code)

#### Defined in

[packages/common-error/src/base-error.ts:67](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L67)

***

### data?

> `optional` **data**: `any`

Additional data associated with the error.

#### Inherited from

[`BaseError`](BaseError.md).[`data`](BaseError.md#data)

#### Defined in

[packages/common-error/src/base-error.ts:68](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L68)

***

### message

> **message**: `string`

#### Inherited from

[`BaseError`](BaseError.md).[`message`](BaseError.md#message)

#### Defined in

node\_modules/.pnpm/typescript@5.6.2/node\_modules/typescript/lib/lib.es5.d.ts:1077

***

### name

> **name**: `string`

#### Inherited from

[`BaseError`](BaseError.md).[`name`](BaseError.md#name)

#### Defined in

node\_modules/.pnpm/typescript@5.6.2/node\_modules/typescript/lib/lib.es5.d.ts:1076

***

### stack?

> `optional` **stack**: `string`

#### Inherited from

[`BaseError`](BaseError.md).[`stack`](BaseError.md#stack)

#### Defined in

node\_modules/.pnpm/typescript@5.6.2/node\_modules/typescript/lib/lib.es5.d.ts:1078

***

### code

> `static` **code**: [`ErrorCodeType`](../type-aliases/ErrorCodeType.md)

The error code associated with the error.

#### Inherited from

[`BaseError`](BaseError.md).[`code`](BaseError.md#code-1)

#### Defined in

[packages/common-error/src/base-error.ts:65](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L65)

***

### prepareStackTrace()?

> `static` `optional` **prepareStackTrace**: (`err`, `stackTraces`) => `any`

Optional override for formatting stack traces

#### Parameters

• **err**: `Error`

• **stackTraces**: `CallSite`[]

#### Returns

`any`

#### See

https://v8.dev/docs/stack-trace-api#customizing-stack-traces

#### Inherited from

[`BaseError`](BaseError.md).[`prepareStackTrace`](BaseError.md#preparestacktrace)

#### Defined in

node\_modules/.pnpm/@types+node@20.14.2/node\_modules/@types/node/globals.d.ts:28

***

### stackTraceLimit

> `static` **stackTraceLimit**: `number`

#### Inherited from

[`BaseError`](BaseError.md).[`stackTraceLimit`](BaseError.md#stacktracelimit)

#### Defined in

node\_modules/.pnpm/@types+node@20.14.2/node\_modules/@types/node/globals.d.ts:30

## Methods

### fromJSON()

> **fromJSON**(`json`): [`BaseError`](BaseError.md)

Creates a new BaseError instance from a JSON representation.

#### Parameters

• **json**: `any`

A JSON representation of the error.

#### Returns

[`BaseError`](BaseError.md)

A new BaseError instance.

#### Inherited from

[`BaseError`](BaseError.md).[`fromJSON`](BaseError.md#fromjson)

#### Defined in

[packages/common-error/src/base-error.ts:141](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L141)

***

### toJSON()

> **toJSON**(): `any`

Returns a JSON representation of the error.

#### Returns

`any`

A JSON representation of the error.

#### Inherited from

[`BaseError`](BaseError.md).[`toJSON`](BaseError.md#tojson)

#### Defined in

[packages/common-error/src/base-error.ts:121](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L121)

***

### captureStackTrace()

#### captureStackTrace(targetObject, constructorOpt)

> `static` **captureStackTrace**(`targetObject`, `constructorOpt`?): `void`

Create .stack property on a target object

##### Parameters

• **targetObject**: `object`

• **constructorOpt?**: `Function`

##### Returns

`void`

##### Inherited from

[`BaseError`](BaseError.md).[`captureStackTrace`](BaseError.md#capturestacktrace)

##### Defined in

node\_modules/.pnpm/@types+node@20.14.2/node\_modules/@types/node/globals.d.ts:21

#### captureStackTrace(targetObject, constructorOpt)

> `static` **captureStackTrace**(`targetObject`, `constructorOpt`?): `void`

Create .stack property on a target object

##### Parameters

• **targetObject**: `object`

• **constructorOpt?**: `Function`

##### Returns

`void`

##### Inherited from

[`BaseError`](BaseError.md).[`captureStackTrace`](BaseError.md#capturestacktrace)

##### Defined in

node\_modules/.pnpm/@types+node@22.5.5/node\_modules/@types/node/globals.d.ts:136

***

### create()

> `static` **create**(`__namedParameters`): [`BaseError`](BaseError.md)

#### Parameters

• **\_\_namedParameters**

• **\_\_namedParameters.code?**: `string` \| `number`

• **\_\_namedParameters.data?**: `any`

• **\_\_namedParameters.error**: `string`

• **\_\_namedParameters.name?**: `string`

#### Returns

[`BaseError`](BaseError.md)

#### Inherited from

[`BaseError`](BaseError.md).[`create`](BaseError.md#create)

#### Defined in

[packages/common-error/src/base-error.ts:74](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L74)

***

### createErrorClass()

> `static` **createErrorClass**(`aType`, `aErrorCode`?, `ParentErrorClass`?): *typeof* [`BaseError`](BaseError.md)

Create an Error Class

#### Parameters

• **aType**: `string`

the error type(class) name

• **aErrorCode?**: `string` \| `number` \| *typeof* `AbstractError`

• **ParentErrorClass?**: *typeof* [`BaseError`](BaseError.md) = `BaseError`

the parent error class. defaults to AbstractError

#### Returns

*typeof* [`BaseError`](BaseError.md)

the new Error Class

#### Inherited from

[`BaseError`](BaseError.md).[`createErrorClass`](BaseError.md#createerrorclass)

#### Defined in

[packages/common-error/src/base-error.ts:70](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L70)
