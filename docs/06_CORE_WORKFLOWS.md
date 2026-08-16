# Core Workflows

## Workflow 1 — Collection
Collector logs in
    ↓
Selects species
    ↓
Captures GPS
    ↓
Captures timestamp
    ↓
Enters quantity
    ↓
Enters initial quality
    ↓
System validates GPS
    ↓
System validates season
    ↓
CollectionEvent created
    ↓
Blockchain transaction submitted
    ↓
Transaction confirmed
    ↓
Collection ID generated

## Workflow 2 — Processing
Processor receives collection/batch
    ↓
Custody transfer recorded
    ↓
Processor records processing step
    ↓
Processing event validated
    ↓
Blockchain transaction confirmed

## Workflow 3 — Laboratory
Laboratory receives sample
    ↓
Performs tests
    ↓
Records QualityTest
    ↓
System validates quality thresholds
    ↓
Result stored
    ↓
Blockchain transaction confirmed

## Workflow 4 — Manufacturing
Manufacturer receives validated material
    ↓
Creates formulation batch
    ↓
System verifies upstream provenance
    ↓
Product batch created
    ↓
Unique QR generated

## Workflow 5 — Consumer
Consumer scans QR
    ↓
QR identifies product batch
    ↓
Backend retrieves provenance
    ↓
System verifies blockchain records
    ↓
Consumer sees provenance timeline
    ↓
Consumer sees map
    ↓
Consumer sees quality results
    ↓
Consumer sees sustainability status

## Workflow 6 — Recall
Failed issue detected
    ↓
Batch marked for recall
    ↓
Recall transaction recorded
    ↓
QR status changes to RECALLED
    ↓
Consumer scanning QR sees warning
