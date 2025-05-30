[**tevm**](../../README.md)

***

[tevm](../../modules.md) / [blockchain](../README.md) / Chain

# Type Alias: Chain

> **Chain**: `object` & `BaseChain` & `object`

Defined in: packages/blockchain/types/Chain.d.ts:14

Blockchain

## Type declaration

### consensus

> **consensus**: `Consensus`

### deepCopy()

> **deepCopy**: () => `Promise`\<[`Chain`](Chain.md)\>

#### Returns

`Promise`\<[`Chain`](Chain.md)\>

### events?

> `optional` **events**: [`AsyncEventEmitter`](../../utils/classes/AsyncEventEmitter.md)\<`BlockchainEvents`\>

Optional events emitter

### shallowCopy()

> **shallowCopy**: () => [`Chain`](Chain.md)

Returns a shallow copy of the blockchain that may share state with the original

#### Returns

[`Chain`](Chain.md)

### delBlock()

Deletes a block from the blockchain. All child blocks in the chain are
deleted and any encountered heads are set to the parent block.

#### Parameters

##### blockHash

`Uint8Array`

The hash of the block to be deleted

#### Returns

`Promise`\<`void`\>

### getBlock()

Returns a block by its hash or number.

#### Parameters

##### blockId

`number` | `bigint` | `Uint8Array`\<`ArrayBufferLike`\>

#### Returns

`Promise`\<[`Block`](../../block/classes/Block.md)\>

### getBlockByTag()

Gets block given one of the following inputs:
- Hex block hash
- Hex block number (if length is 32 bytes, it is treated as a hash)
- Uint8Array block hash
- Number block number
- BigInt block number
- BlockTag block tag
- Named block tag (e.g. 'latest', 'earliest', 'pending')

#### Parameters

##### blockTag

`number` | `bigint` | `` `0x${string}` `` | `Uint8Array`\<`ArrayBufferLike`\> | [`BlockTag`](../../index/type-aliases/BlockTag.md)

#### Returns

`Promise`\<[`Block`](../../block/classes/Block.md)\>

#### Throws

- If the block is not found

#### Throw

- If the block tag is invalid}

### getCanonicalHeadBlock()

Returns the latest full block in the canonical chain.

#### Returns

`Promise`\<[`Block`](../../block/classes/Block.md)\>

### getIteratorHead()

Returns the specified iterator head.

#### Parameters

##### name?

`string`

Optional name of the iterator head (default: 'vm')

#### Returns

`Promise`\<[`Block`](../../block/classes/Block.md)\>

### getTotalDifficulty()?

Gets total difficulty for a block specified by hash and number

#### Parameters

##### hash

`Uint8Array`

##### number?

`bigint`

#### Returns

`Promise`\<`bigint`\>

### iterator()

Iterates through blocks starting at the specified iterator head and calls
the onBlock function on each block.

#### Parameters

##### name

`string`

Name of the state root head

##### onBlock

`OnBlock`

Function called on each block with params (block: Block,

##### maxBlocks?

`number`

optional maximum number of blocks to iterate through
reorg: boolean)

##### releaseLockOnCallback?

`boolean`

#### Returns

`Promise`\<`number`\>

### putBlock()

Adds a block to the blockchain.

#### Parameters

##### block

[`Block`](../../block/classes/Block.md)

The block to be added to the blockchain.

#### Returns

`Promise`\<`void`\>

### setIteratorHead()

Set header hash of a certain `tag`.
When calling the iterator, the iterator will start running the first child block after the header hash currently stored.

#### Parameters

##### tag

`string`

The tag to save the headHash to

##### headHash

`Uint8Array`

The head hash to save

#### Returns

`Promise`\<`void`\>

### validateHeader()

Validates a block header, throwing if invalid. It is being validated against the reported `parentHash`.

#### Parameters

##### header

[`BlockHeader`](../../block/classes/BlockHeader.md)

header to be validated

##### height?

`bigint`

If this is an uncle header, this is the height of the block that is including it

#### Returns

`Promise`\<`void`\>
