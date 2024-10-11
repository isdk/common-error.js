[**@isdk/common-error**](../README.md) • **Docs**

***

[@isdk/common-error](../globals.md) / throwError

# Function: throwError()

> **throwError**(`message`, `name`?, `status`?): `void`

Throw an error

## Parameters

• **message**: `string`

Error message

• **name?**: `string` \| `Record`\<`string`, `any`\>

Error name, optional

• **status?**: `string` \| `number` = `InternalErrorCode`

Error status code, default to 500

## Returns

`void`

## Throws

Throws a BaseError object

## Defined in

[packages/common-error/src/base-error.ts:252](https://github.com/isdk/common-error.js/blob/f7578a9ecd75a483a24a80a8e96a99303c1ef148/src/base-error.ts#L252)
