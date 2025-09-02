[**@isdk/common-error**](../README.md)

***

[@isdk/common-error](../globals.md) / createError

# Function: createError()

> **createError**(`message`, `name`?, `status`?): [`CommonError`](../classes/CommonError.md)

Defined in: [packages/common-error/src/base-error.ts:251](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L251)

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
