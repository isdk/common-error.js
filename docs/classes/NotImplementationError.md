[**@isdk/common-error**](../README.md)

***

[@isdk/common-error](../globals.md) / NotImplementationError

# Class: NotImplementationError

Defined in: [packages/common-error/src/base-error.ts:174](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L174)

Represents an error when a function or method is not implemented.
Inherits from BaseError.

## Example

```ts
throw new NotImplementationError()
```

## Extends

- [`CommonError`](CommonError.md)

## Constructors

### new NotImplementationError()

> **new NotImplementationError**(`msg`?, `name`?): [`NotImplementationError`](NotImplementationError.md)

Defined in: [packages/common-error/src/base-error.ts:175](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L175)

#### Parameters

##### msg?

`string`

##### name?

`string` | `Record`\<`string`, `any`\>

#### Returns

[`NotImplementationError`](NotImplementationError.md)

#### Overrides

[`CommonError`](CommonError.md).[`constructor`](CommonError.md#constructors)

## Properties

### caller

> **caller**: `string`

Defined in: [packages/common-error/src/base-error.ts:66](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L66)

The name of the function that threw the error.

#### Inherited from

[`CommonError`](CommonError.md).[`caller`](CommonError.md#caller)

***

### code

> **code**: [`ErrorCodeType`](../type-aliases/ErrorCodeType.md)

Defined in: [packages/common-error/src/base-error.ts:67](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L67)

the error code

#### Inherited from

[`CommonError`](CommonError.md).[`code`](CommonError.md#code)

***

### data?

> `optional` **data**: `any`

Defined in: [packages/common-error/src/base-error.ts:68](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L68)

Additional data associated with the error.

#### Inherited from

[`CommonError`](CommonError.md).[`data`](CommonError.md#data)

***

### message

> **message**: `string`

Defined in: node\_modules/.pnpm/typescript@5.7.3/node\_modules/typescript/lib/lib.es5.d.ts:1077

#### Inherited from

[`CommonError`](CommonError.md).[`message`](CommonError.md#message-1)

***

### name

> **name**: `string`

Defined in: node\_modules/.pnpm/typescript@5.7.3/node\_modules/typescript/lib/lib.es5.d.ts:1076

#### Inherited from

[`CommonError`](CommonError.md).[`name`](CommonError.md#name-1)

***

### stack?

> `optional` **stack**: `string`

Defined in: node\_modules/.pnpm/typescript@5.7.3/node\_modules/typescript/lib/lib.es5.d.ts:1078

#### Inherited from

[`CommonError`](CommonError.md).[`stack`](CommonError.md#stack)

***

### code

> `static` **code**: [`ErrorCodeType`](../type-aliases/ErrorCodeType.md)

Defined in: [packages/common-error/src/base-error.ts:65](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L65)

The error code associated with the error.

#### Inherited from

[`CommonError`](CommonError.md).[`code`](CommonError.md#code-1)

***

### prepareStackTrace()?

> `static` `optional` **prepareStackTrace**: (`err`, `stackTraces`) => `any`

Defined in: node\_modules/.pnpm/@types+node@22.10.10/node\_modules/@types/node/globals.d.ts:143

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

[`CommonError`](CommonError.md).[`prepareStackTrace`](CommonError.md#preparestacktrace)

***

### stackTraceLimit

> `static` **stackTraceLimit**: `number`

Defined in: node\_modules/.pnpm/@types+node@22.10.10/node\_modules/@types/node/globals.d.ts:145

#### Inherited from

[`CommonError`](CommonError.md).[`stackTraceLimit`](CommonError.md#stacktracelimit)

## Methods

### fromJSON()

> **fromJSON**(`json`): [`BaseError`](BaseError.md)

Defined in: [packages/common-error/src/base-error.ts:141](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L141)

Creates a new BaseError instance from a JSON representation.

#### Parameters

##### json

`any`

A JSON representation of the error.

#### Returns

[`BaseError`](BaseError.md)

A new BaseError instance.

#### Inherited from

[`CommonError`](CommonError.md).[`fromJSON`](CommonError.md#fromjson)

***

### toJSON()

> **toJSON**(): `any`

Defined in: [packages/common-error/src/base-error.ts:121](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L121)

Returns a JSON representation of the error.

#### Returns

`any`

A JSON representation of the error.

#### Inherited from

[`CommonError`](CommonError.md).[`toJSON`](CommonError.md#tojson)

***

### captureStackTrace()

#### Call Signature

> `static` **captureStackTrace**(`targetObject`, `constructorOpt`?): `void`

Defined in: node\_modules/.pnpm/@types+node@22.10.10/node\_modules/@types/node/globals.d.ts:136

Create .stack property on a target object

##### Parameters

###### targetObject

`object`

###### constructorOpt?

`Function`

##### Returns

`void`

##### Inherited from

[`CommonError`](CommonError.md).[`captureStackTrace`](CommonError.md#capturestacktrace)

#### Call Signature

> `static` **captureStackTrace**(`targetObject`, `constructorOpt`?): `void`

Defined in: node\_modules/.pnpm/@types+node@22.13.10/node\_modules/@types/node/globals.d.ts:136

Create .stack property on a target object

##### Parameters

###### targetObject

`object`

###### constructorOpt?

`Function`

##### Returns

`void`

##### Inherited from

[`CommonError`](CommonError.md).[`captureStackTrace`](CommonError.md#capturestacktrace)

***

### create()

> `static` **create**(`__namedParameters`): [`CommonError`](CommonError.md)

Defined in: [packages/common-error/src/base-error.ts:153](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L153)

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

#### Inherited from

[`CommonError`](CommonError.md).[`create`](CommonError.md#create)

***

### createErrorClass()

> `static` **createErrorClass**(`aType`, `aErrorCode`?, `ParentErrorClass`?): *typeof* [`BaseError`](BaseError.md)

Defined in: [packages/common-error/src/base-error.ts:70](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L70)

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

[`CommonError`](CommonError.md).[`createErrorClass`](CommonError.md#createerrorclass)
