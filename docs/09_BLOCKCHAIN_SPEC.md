# Blockchain Specification

## Blockchain
Hyperledger Fabric is the preferred permissioned blockchain.

## Purpose
Blockchain provides:
- Immutable audit trail
- Provenance
- Supply-chain event integrity
- Participant accountability
- Verification

## On-Chain Entities
The blockchain should contain references/records for:
- CollectionEvent
- ProcessingStep
- QualityTest
- CustodyTransfer
- ProductBatch
- Recall

## Smart Contract Rules

### Collection
Reject collection if:
- GPS is outside approved zone
- Collection occurs outside permitted season
- Species is not authorized
- Required metadata is missing

### Quality
Reject/flag quality result if required tests are missing.

### Processing
Processing must reference an existing valid batch.

### Manufacturing
Product batch must reference valid upstream material.

### Recall
A recalled batch must be reflected in consumer verification.

## Blockchain Rule
Do not store large binary files directly on-chain.

For certificates/images/documents:
Off-chain file
    ↓
Hash
    ↓
Blockchain record
