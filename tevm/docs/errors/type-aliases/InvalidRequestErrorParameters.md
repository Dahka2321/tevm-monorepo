[**tevm**](../../README.md)

***

[tevm](../../modules.md) / [errors](../README.md) / InvalidRequestErrorParameters

# Type Alias: InvalidRequestErrorParameters

> **InvalidRequestErrorParameters**: `object`

Defined in: packages/errors/types/ethereum/InvalidRequestError.d.ts:50

Parameters for constructing an InvalidRequestError.

## Type declaration

### cause?

> `optional` **cause**: [`BaseError`](../classes/BaseError.md) \| `Error`

- The cause of the error.

### details?

> `optional` **details**: `string`

- Details of the error.

### docsBaseUrl?

> `optional` **docsBaseUrl**: `string`

- Base URL for the documentation.

### docsPath?

> `optional` **docsPath**: `string`

- Path to the documentation.

### docsSlug?

> `optional` **docsSlug**: `string`

- Slug for the documentation.

### meta?

> `optional` **meta**: `object`

- Optional object containing additional information about the error.

### metaMessages?

> `optional` **metaMessages**: `string`[]

- Additional meta messages.
