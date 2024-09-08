[@isdk/common-error](README.md) / Exports

# @isdk/common-error

## Table of contents

### Enumerations

- [ErrorCode](enums/ErrorCode.md)

### Classes

- [AbortError](classes/AbortError.md)
- [AlreadyExistsError](classes/AlreadyExistsError.md)
- [BaseError](classes/BaseError.md)
- [CommonError](classes/CommonError.md)
- [NotFoundError](classes/NotFoundError.md)
- [NotImplementationError](classes/NotImplementationError.md)

### Type Aliases

- [ErrorCodeType](modules.md#errorcodetype)

### Variables

- [AbortErrorCode](modules.md#aborterrorcode)
- [AlreadyExistsErrorCode](modules.md#alreadyexistserrorcode)
- [InternalErrorCode](modules.md#internalerrorcode)
- [NotFoundErrorCode](modules.md#notfounderrorcode)
- [NotImplementedErrorCode](modules.md#notimplementederrorcode)

### Functions

- [createError](modules.md#createerror)
- [throwError](modules.md#throwerror)

## Type Aliases

### ErrorCodeType

Ƭ **ErrorCodeType**: `number` \| `string`

#### Defined in

[packages/common-error/src/base-error.ts:3](https://github.com/isdk/common-error.js/blob/533ed946686188be88f8a204d390f4c3d1e25f73/src/base-error.ts#L3)

## Variables

### AbortErrorCode

• `Const` **AbortErrorCode**: [`Aborted`](enums/ErrorCode.md#aborted) = `ErrorCode.Aborted`

#### Defined in

[packages/common-error/src/base-error.ts:33](https://github.com/isdk/common-error.js/blob/533ed946686188be88f8a204d390f4c3d1e25f73/src/base-error.ts#L33)

___

### AlreadyExistsErrorCode

• `Const` **AlreadyExistsErrorCode**: [`Conflict`](enums/ErrorCode.md#conflict) = `ErrorCode.Conflict`

#### Defined in

[packages/common-error/src/base-error.ts:32](https://github.com/isdk/common-error.js/blob/533ed946686188be88f8a204d390f4c3d1e25f73/src/base-error.ts#L32)

___

### InternalErrorCode

• `Const` **InternalErrorCode**: [`InternalError`](enums/ErrorCode.md#internalerror) = `ErrorCode.InternalError`

#### Defined in

[packages/common-error/src/base-error.ts:29](https://github.com/isdk/common-error.js/blob/533ed946686188be88f8a204d390f4c3d1e25f73/src/base-error.ts#L29)

___

### NotFoundErrorCode

• `Const` **NotFoundErrorCode**: [`NotFound`](enums/ErrorCode.md#notfound) = `ErrorCode.NotFound`

#### Defined in

[packages/common-error/src/base-error.ts:31](https://github.com/isdk/common-error.js/blob/533ed946686188be88f8a204d390f4c3d1e25f73/src/base-error.ts#L31)

___

### NotImplementedErrorCode

• `Const` **NotImplementedErrorCode**: [`NotImplemented`](enums/ErrorCode.md#notimplemented) = `ErrorCode.NotImplemented`

#### Defined in

[packages/common-error/src/base-error.ts:30](https://github.com/isdk/common-error.js/blob/533ed946686188be88f8a204d390f4c3d1e25f73/src/base-error.ts#L30)

## Functions

### createError

▸ **createError**(`message`, `name?`, `status?`): [`CommonError`](classes/CommonError.md)

Create an error object

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `message` | `string` | `undefined` | Error message |
| `name?` | `string` \| `Record`\<`string`, `any`\> | `undefined` | Error name, optional |
| `status` | `string` \| `number` | `InternalErrorCode` | Error status code, default to 500 |

#### Returns

[`CommonError`](classes/CommonError.md)

Error object

#### Defined in

[packages/common-error/src/base-error.ts:220](https://github.com/isdk/common-error.js/blob/533ed946686188be88f8a204d390f4c3d1e25f73/src/base-error.ts#L220)

___

### throwError

▸ **throwError**(`message`, `name?`, `status?`): `void`

Throw an error

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `message` | `string` | `undefined` | Error message |
| `name?` | `string` \| `Record`\<`string`, `any`\> | `undefined` | Error name, optional |
| `status` | `string` \| `number` | `InternalErrorCode` | Error status code, default to 500 |

#### Returns

`void`

**`Throws`**

Throws a BaseError object

#### Defined in

[packages/common-error/src/base-error.ts:235](https://github.com/isdk/common-error.js/blob/533ed946686188be88f8a204d390f4c3d1e25f73/src/base-error.ts#L235)
