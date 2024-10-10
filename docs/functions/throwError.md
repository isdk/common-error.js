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

[packages/common-error/src/base-error.ts:245](https://github.com/isdk/common-error.js/blob/93463fd20d360c4af96d07cc295f19a4c7e514bd/src/base-error.ts#L245)
