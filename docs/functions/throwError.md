[**@isdk/common-error**](../README.md)

***

[@isdk/common-error](../globals.md) / throwError

# Function: throwError()

> **throwError**(`message`, `name`?, `status`?): `never`

Defined in: [packages/common-error/src/base-error.ts:252](https://github.com/isdk/common-error.js/blob/ba75328e754ba949e73cfe3c3e47f894c8ab334d/src/base-error.ts#L252)

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
