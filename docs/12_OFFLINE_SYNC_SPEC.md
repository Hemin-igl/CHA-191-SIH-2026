# Offline and Synchronization Specification

## Requirement
Collector interface must support data capture when internet connectivity is unavailable or unreliable.

## Offline Data
The application should temporarily store:
- Collection data
- GPS
- Timestamp
- Collector ID
- Species
- Quantity
- Initial quality information

## Sync Flow
When connectivity returns:
Local data
   ↓
Sync queue
   ↓
Backend
   ↓
Validation
   ↓
Blockchain transaction
   ↓
Confirmation
   ↓
Local record marked synced

## Sync States
- PENDING
- SYNCING
- SYNCED
- FAILED
- RETRY

## Important
- Offline records must not be silently lost.
- Duplicate submissions must be detected.
