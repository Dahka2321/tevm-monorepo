[**@tevm/utils**](../README.md)

***

[@tevm/utils](../globals.md) / AbiParametersToPrimitiveTypes

# Type Alias: AbiParametersToPrimitiveTypes\<abiParameters, abiParameterKind\>

> **AbiParametersToPrimitiveTypes**\<`abiParameters`, `abiParameterKind`\>: `Pretty`\<`{ [key in keyof abiParameters]: AbiParameterToPrimitiveType<abiParameters[key], abiParameterKind> }`\>

Defined in: node\_modules/.pnpm/abitype@1.0.8\_typescript@5.8.3\_zod@3.24.3/node\_modules/abitype/dist/types/utils.d.ts:86

Converts array of AbiParameter to corresponding TypeScript primitive types.

## Type Parameters

• **abiParameters** *extends* readonly `AbiParameter`[]

Array of AbiParameter to convert to TypeScript representations

• **abiParameterKind** *extends* `AbiParameterKind` = `AbiParameterKind`

Optional AbiParameterKind to narrow by parameter type

## Returns

Array of TypeScript primitive types
