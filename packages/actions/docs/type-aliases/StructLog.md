[**@tevm/actions**](../README.md)

***

[@tevm/actions](../globals.md) / StructLog

# Type Alias: StructLog

> **StructLog**: `object`

Defined in: [packages/actions/src/common/StructLog.ts:3](https://github.com/evmts/tevm-monorepo/blob/main/packages/actions/src/common/StructLog.ts#L3)

## Type declaration

### depth

> `readonly` **depth**: `number`

### error?

> `readonly` `optional` **error**: `object`

#### error.error

> **error**: `string`

#### error.errorType

> **errorType**: `string`

### gas

> `readonly` **gas**: `bigint`

### gasCost

> `readonly` **gasCost**: `bigint`

### op

> `readonly` **op**: `string`

### pc

> `readonly` **pc**: `number`

### stack

> `readonly` **stack**: [`Hex`](Hex.md)[]
