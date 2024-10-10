[**@isdk/common-error**](../README.md) • **Docs**

***

[@isdk/common-error](../globals.md) / createError

# Function: createError()

> **createError**(`message`, `name`?, `status`?): [`CommonError`](../classes/CommonError.md)

Create an error object

## Parameters

• **message**: `string`

Error message

• **name?**: `string` \| `Record`\<`string`, `any`\>

Error name, optional

• **status?**: `string` \| `number` = `InternalErrorCode`

Error status code, default to 500

## Returns

[`CommonError`](../classes/CommonError.md)

Error object

## Defined in

[packages/common-error/src/base-error.ts:230](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L230)
