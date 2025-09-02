[**@isdk/common-error**](../README.md)

***

[@isdk/common-error](../globals.md) / throwError

# Function: throwError()

> **throwError**(`message`, `name`?, `status`?): `never`

Defined in: [packages/common-error/src/base-error.ts:266](https://github.com/isdk/common-error.js/blob/577bb8389747251b05fc6177a60862a64b029c0d/src/base-error.ts#L266)

Throw an error

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

`never`

## Throws

Throws a BaseError object
