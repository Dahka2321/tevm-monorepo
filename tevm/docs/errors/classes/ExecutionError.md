[**tevm**](../../README.md)

***

[tevm](../../modules.md) / [errors](../README.md) / ExecutionError

# Class: ExecutionError

Defined in: packages/errors/types/ethereum/ExecutionErrorError.d.ts:37

Represents an error that occurs when an execution error happens on the Ethereum node.

This error is typically encountered when there is a general execution error that does not fit more specific categories.

## Example

```ts
try {
  // Some operation that can throw an ExecutionError
} catch (error) {
  if (error instanceof ExecutionError) {
    console.error(error.message);
    // Handle the execution error
  }
}
```

## Param

A human-readable error message.

## Param

Additional parameters for the BaseError.

## Extends

- [`BaseError`](BaseError.md)

## Extended by

- [`InvalidOpcodeError`](InvalidOpcodeError.md)
- [`StopError`](StopError.md)
- [`OutOfRangeError`](OutOfRangeError.md)
- [`InvalidJumpError`](InvalidJumpError.md)
- [`InvalidProofError`](InvalidProofError.md)
- [`AuthCallUnsetError`](AuthCallUnsetError.md)
- [`StackOverflowError`](StackOverflowError.md)
- [`InvalidJumpSubError`](InvalidJumpSubError.md)
- [`StackUnderflowError`](StackUnderflowError.md)
- [`CreateCollisionError`](CreateCollisionError.md)
- [`InvalidBeginSubError`](InvalidBeginSubError.md)
- [`RefundExhaustedError`](RefundExhaustedError.md)
- [`InvalidEofFormatError`](InvalidEofFormatError.md)
- [`InvalidKzgInputsError`](InvalidKzgInputsError.md)
- [`InvalidReturnSubError`](InvalidReturnSubError.md)
- [`InvalidCommitmentError`](InvalidCommitmentError.md)
- [`StaticStateChangeError`](StaticStateChangeError.md)
- [`BLS12381InputEmptyError`](BLS12381InputEmptyError.md)
- [`InvalidInputLengthError`](InvalidInputLengthError.md)
- [`InsufficientBalanceError`](InsufficientBalanceError.md)
- [`BLS12381FpNotInFieldError`](BLS12381FpNotInFieldError.md)
- [`InitcodeSizeViolationError`](InitcodeSizeViolationError.md)
- [`InvalidBytecodeResultError`](InvalidBytecodeResultError.md)
- [`BLS12381PointNotOnCurveError`](BLS12381PointNotOnCurveError.md)
- [`BLS12381InvalidInputLengthError`](BLS12381InvalidInputLengthError.md)
- [`ValueOverflowError`](ValueOverflowError.md)
- [`CommonMismatchError`](CommonMismatchError.md)
- [`EipNotEnabledError`](EipNotEnabledError.md)

## Constructors

### new ExecutionError()

> **new ExecutionError**(`message`, `args`?, `tag`?): [`ExecutionError`](ExecutionError.md)

Defined in: packages/errors/types/ethereum/ExecutionErrorError.d.ts:50

Constructs an ExecutionError.

#### Parameters

##### message

`string`

Human-readable error message.

##### args?

[`ExecutionErrorParameters`](../type-aliases/ExecutionErrorParameters.md)

Additional parameters for the BaseError.

##### tag?

`string`

Internal name/tag for the error.

#### Returns

[`ExecutionError`](ExecutionError.md)

#### Overrides

[`BaseError`](BaseError.md).[`constructor`](BaseError.md#constructors)

## Properties

### \_tag

> **\_tag**: `string`

Defined in: packages/errors/types/ethereum/BaseError.d.ts:40

More discriminated version of name. Can be used to discriminate between errors with the same name.

#### Inherited from

[`BaseError`](BaseError.md).[`_tag`](BaseError.md#_tag-1)

***

### cause

> **cause**: `any`

Defined in: packages/errors/types/ethereum/BaseError.d.ts:65

#### Inherited from

[`BaseError`](BaseError.md).[`cause`](BaseError.md#cause)

***

### code

> **code**: `number`

Defined in: packages/errors/types/ethereum/BaseError.d.ts:64

#### Inherited from

[`BaseError`](BaseError.md).[`code`](BaseError.md#code-1)

***

### details

> **details**: `string`

Defined in: packages/errors/types/ethereum/BaseError.d.ts:44

#### Inherited from

[`BaseError`](BaseError.md).[`details`](BaseError.md#details)

***

### docsPath

> **docsPath**: `undefined` \| `string`

Defined in: packages/errors/types/ethereum/BaseError.d.ts:48

Path to the documentation for this error.

#### Inherited from

[`BaseError`](BaseError.md).[`docsPath`](BaseError.md#docspath)

***

### message

> **message**: `string`

Defined in: node\_modules/.pnpm/typescript@5.8.2/node\_modules/typescript/lib/lib.es5.d.ts:1077

Human-readable error message.

#### Inherited from

[`BaseError`](BaseError.md).[`message`](BaseError.md#message)

***

### metaMessages

> **metaMessages**: `undefined` \| `string`[]

Defined in: packages/errors/types/ethereum/BaseError.d.ts:52

Additional meta messages for more context.

#### Inherited from

[`BaseError`](BaseError.md).[`metaMessages`](BaseError.md#metamessages)

***

### name

> **name**: `string`

Defined in: node\_modules/.pnpm/typescript@5.8.2/node\_modules/typescript/lib/lib.es5.d.ts:1076

The name of the error, used to discriminate errors.

#### Inherited from

[`BaseError`](BaseError.md).[`name`](BaseError.md#name)

***

### shortMessage

> **shortMessage**: `string`

Defined in: packages/errors/types/ethereum/BaseError.d.ts:56

#### Inherited from

[`BaseError`](BaseError.md).[`shortMessage`](BaseError.md#shortmessage-1)

***

### stack?

> `optional` **stack**: `string`

Defined in: node\_modules/.pnpm/typescript@5.8.2/node\_modules/typescript/lib/lib.es5.d.ts:1078

#### Inherited from

[`BaseError`](BaseError.md).[`stack`](BaseError.md#stack)

***

### version

> **version**: `string`

Defined in: packages/errors/types/ethereum/BaseError.d.ts:60

#### Inherited from

[`BaseError`](BaseError.md).[`version`](BaseError.md#version)

***

### code

> `static` **code**: `number`

Defined in: packages/errors/types/ethereum/ExecutionErrorError.d.ts:42

Error code, analogous to the code in JSON RPC error.

***

### prepareStackTrace()?

> `static` `optional` **prepareStackTrace**: (`err`, `stackTraces`) => `any`

Defined in: node\_modules/.pnpm/@types+node@22.13.10/node\_modules/@types/node/globals.d.ts:143

Optional override for formatting stack traces

#### Parameters

##### err

`Error`

##### stackTraces

`CallSite`[]

#### Returns

`any`

#### See

https://v8.dev/docs/stack-trace-api#customizing-stack-traces

#### Inherited from

[`BaseError`](BaseError.md).[`prepareStackTrace`](BaseError.md#preparestacktrace)

***

### stackTraceLimit

> `static` **stackTraceLimit**: `number`

Defined in: node\_modules/.pnpm/@types+node@22.13.10/node\_modules/@types/node/globals.d.ts:145

#### Inherited from

[`BaseError`](BaseError.md).[`stackTraceLimit`](BaseError.md#stacktracelimit)

## Methods

### walk()

> **walk**(`fn`?): `unknown`

Defined in: packages/errors/types/ethereum/BaseError.d.ts:71

Walks through the error chain.

#### Parameters

##### fn?

`Function`

A function to execute on each error in the chain.

#### Returns

`unknown`

The first error that matches the function, or the original error.

#### Inherited from

[`BaseError`](BaseError.md).[`walk`](BaseError.md#walk)

***

### captureStackTrace()

#### Call Signature

> `static` **captureStackTrace**(`targetObject`, `constructorOpt`?): `void`

Defined in: node\_modules/.pnpm/@types+node@22.13.10/node\_modules/@types/node/globals.d.ts:136

Create .stack property on a target object

##### Parameters

###### targetObject

`object`

###### constructorOpt?

`Function`

##### Returns

`void`

##### Inherited from

[`BaseError`](BaseError.md).[`captureStackTrace`](BaseError.md#capturestacktrace)

#### Call Signature

> `static` **captureStackTrace**(`targetObject`, `constructorOpt`?): `void`

Defined in: node\_modules/.pnpm/@types+node@22.14.1/node\_modules/@types/node/globals.d.ts:136

Create .stack property on a target object

##### Parameters

###### targetObject

`object`

###### constructorOpt?

`Function`

##### Returns

`void`

##### Inherited from

[`BaseError`](BaseError.md).[`captureStackTrace`](BaseError.md#capturestacktrace)
