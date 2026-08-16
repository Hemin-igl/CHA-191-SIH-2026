# Testing Requirements

## Collection
Test:
- Valid GPS
- Invalid GPS
- Missing GPS
- Invalid species
- Invalid quantity
- Duplicate collection
- Offline collection
- Offline sync

## Blockchain
Test:
- Valid transaction
- Invalid transaction
- Unauthorized actor
- Duplicate transaction
- Invalid batch reference

## Quality
Test:
- Passing result
- Failed result
- Missing test
- Invalid laboratory

## QR
Test:
- Valid QR
- Invalid QR
- Expired/nonexistent QR
- Recalled product
- Tampered identifier

## Security
Test:
- Unauthorized API access
- Role escalation
- Invalid tokens
- Input injection
- Sensitive information exposure

## Integration
Test complete flow:
Collection → Processing → Laboratory → Manufacturing → QR → Consumer

## Recall
Test:
Quality failure → Batch recall → Consumer QR → Recall warning
