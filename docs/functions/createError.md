[**@isdk/common-error**](../README.md)

***

[@isdk/common-error](../globals.md) / createError

# Function: createError()

> **createError**(`message`, `name`?, `status`?): [`CommonError`](../classes/CommonError.md)

Defined in: [packages/common-error/src/base-error.ts:237](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L237)

Create an error object

## Parameters

### message

`string`

Error message

### name?

Error name, optional

`string` | `Record`\<`string`, `any`\>

### status?

Error status code, default to 500

`string` | `number`

## Returns

[`CommonError`](../classes/CommonError.md)

Error object
