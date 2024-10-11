[**@isdk/common-error**](../README.md) • **Docs**

***

[@isdk/common-error](../globals.md) / AlreadyExistsError

# Class: AlreadyExistsError

Represents an error when a requested resource already exists.
Inherits from BaseError.

## Example

```ts
throw new AlreadyExistsError('user', { id: 123 })
```

## Extends

- [`CommonError`](CommonError.md)

## Constructors

### new AlreadyExistsError()

> **new AlreadyExistsError**(`what`, `name`?): [`AlreadyExistsError`](AlreadyExistsError.md)

#### Parameters

• **what**: `string` \| `number`

• **name?**: `string` \| `Record`\<`string`, `any`\>

#### Returns

[`AlreadyExistsError`](AlreadyExistsError.md)

#### Overrides

[`CommonError`](CommonError.md).[`constructor`](CommonError.md#constructors)

#### Defined in

[packages/common-error/src/base-error.ts:212](https://github.com/isdk/common-error.js/blob/f7578a9ecd75a483a24a80a8e96a99303c1ef148/src/base-error.ts#L212)

## Properties

### caller

> **caller**: `string`

The name of the function that threw the error.

#### Inherited from

[`CommonError`](CommonError.md).[`caller`](CommonError.md#caller)

#### Defined in

[packages/common-error/src/base-error.ts:66](https://github.com/isdk/common-error.js/blob/f7578a9ecd75a483a24a80a8e96a99303c1ef148/src/base-error.ts#L66)

***

### code

> **code**: [`ErrorCodeType`](../type-aliases/ErrorCodeType.md)

the error code

#### Inherited from

[`CommonError`](CommonError.md).[`code`](CommonError.md#code)

#### Defined in

[packages/common-error/src/base-error.ts:67](https://github.com/isdk/common-error.js/blob/f7578a9ecd75a483a24a80a8e96a99303c1ef148/src/base-error.ts#L67)

***

### data?

> `optional` **data**: `any`

Additional data associated with the error.

#### Inherited from

[`CommonError`](CommonError.md).[`data`](CommonError.md#data)

#### Defined in

[packages/common-error/src/base-error.ts:68](https://github.com/isdk/common-error.js/blob/f7578a9ecd75a483a24a80a8e96a99303c1ef148/src/base-error.ts#L68)

***

### message

> **message**: `string`

#### Inherited from

[`CommonError`](CommonError.md).[`message`](CommonError.md#message)

#### Defined in

node\_modules/.pnpm/typescript@5.6.2/node\_modules/typescript/lib/lib.es5.d.ts:1077

***

### name

> **name**: `string`

#### Inherited from

[`CommonError`](CommonError.md).[`name`](CommonError.md#name)

#### Defined in

node\_modules/.pnpm/typescript@5.6.2/node\_modules/typescript/lib/lib.es5.d.ts:1076

***

### stack?

> `optional` **stack**: `string`

#### Inherited from

[`CommonError`](CommonError.md).[`stack`](CommonError.md#stack)

#### Defined in

node\_modules/.pnpm/typescript@5.6.2/node\_modules/typescript/lib/lib.es5.d.ts:1078

***

### code

> `static` **code**: [`ErrorCode`](../enumerations/ErrorCode.md) = `AlreadyExistsErrorCode`

The error code associated with the error.

#### Overrides

[`CommonError`](CommonError.md).[`code`](CommonError.md#code-1)

#### Defined in

[packages/common-error/src/base-error.ts:211](https://github.com/isdk/common-error.js/blob/f7578a9ecd75a483a24a80a8e96a99303c1ef148/src/base-error.ts#L211)

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

[`CommonError`](CommonError.md).[`prepareStackTrace`](CommonError.md#preparestacktrace)

#### Defined in

node\_modules/.pnpm/@types+node@20.14.2/node\_modules/@types/node/globals.d.ts:28

***

### stackTraceLimit

> `static` **stackTraceLimit**: `number`

#### Inherited from

[`CommonError`](CommonError.md).[`stackTraceLimit`](CommonError.md#stacktracelimit)

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

[`CommonError`](CommonError.md).[`fromJSON`](CommonError.md#fromjson)

#### Defined in

[packages/common-error/src/base-error.ts:141](https://github.com/isdk/common-error.js/blob/f7578a9ecd75a483a24a80a8e96a99303c1ef148/src/base-error.ts#L141)

***

### toJSON()

> **toJSON**(): `any`

Returns a JSON representation of the error.

#### Returns

`any`

A JSON representation of the error.

#### Inherited from

[`CommonError`](CommonError.md).[`toJSON`](CommonError.md#tojson)

#### Defined in

[packages/common-error/src/base-error.ts:121](https://github.com/isdk/common-error.js/blob/f7578a9ecd75a483a24a80a8e96a99303c1ef148/src/base-error.ts#L121)

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

[`CommonError`](CommonError.md).[`captureStackTrace`](CommonError.md#capturestacktrace)

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

[`CommonError`](CommonError.md).[`captureStackTrace`](CommonError.md#capturestacktrace)

##### Defined in

node\_modules/.pnpm/@types+node@22.5.5/node\_modules/@types/node/globals.d.ts:136

***

### create()

> `static` **create**(`__namedParameters`): [`CommonError`](CommonError.md)

#### Parameters

• **\_\_namedParameters**

• **\_\_namedParameters.code?**: `string` \| `number`

• **\_\_namedParameters.data?**: `any`

• **\_\_namedParameters.error**: `string`

• **\_\_namedParameters.name?**: `string`

#### Returns

[`CommonError`](CommonError.md)

#### Inherited from

[`CommonError`](CommonError.md).[`create`](CommonError.md#create)

#### Defined in

[packages/common-error/src/base-error.ts:153](https://github.com/isdk/common-error.js/blob/f7578a9ecd75a483a24a80a8e96a99303c1ef148/src/base-error.ts#L153)

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

[`CommonError`](CommonError.md).[`createErrorClass`](CommonError.md#createerrorclass)

#### Defined in

[packages/common-error/src/base-error.ts:70](https://github.com/isdk/common-error.js/blob/f7578a9ecd75a483a24a80a8e96a99303c1ef148/src/base-error.ts#L70)
