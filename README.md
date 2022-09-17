# A Sample Organization: ASO

Welcome! We are the sample organization ASO!

## What is ASO?

ASO is a sample organization that is used to demonstrate the block data of [Simperby](https://github.com/postech-dao/simperby).

## Differences from the Actual Simperby Data

For the sake of simplicity, we present a simplified version of the actual Simperby data.

### Crypto

We use the following format for any crypto-related data:

1. Public key: `<key:name>`
2. Signature: `<signature>`
3. Hash: `<hash>`

Empty data is represented by `<empty>`.

### Header

We omit some fields in the block header which is recorded in the commit message and the gensis info.

```rust
// INCLUDED
pub author: PublicKey,
pub height: BlockHeight,
pub timestamp: Timestamp,
pub validator_set: Vec<(PublicKey, VotingPower)>,
pub version: String,
// OMITTED
pub prev_block_finalization_proof: FinalizationProof,
pub previous_hash: Hash256,
pub tx_merkle_root: Hash256,
pub state_merkle_root: Hash256,
pub delegation_state_hash: Hash256,
```

### Member

The minimum number of members is 7 (1/6 BFT), but we present only 3 members in this sample.
