# Data Model

## CollectionEvent
Fields:
- eventId
- batchId
- speciesId
- collectorId
- quantity
- unit
- latitude
- longitude
- timestamp
- collectionZoneId
- initialQuality
- sustainabilityStatus
- validationStatus
- blockchainTxId

## ProcessingStep
Fields:
- processingId
- batchId
- facilityId
- processorId
- processType
- startTime
- endTime
- quantityBefore
- quantityAfter
- environmentalConditions
- timestamp
- blockchainTxId

## QualityTest
Fields:
- testId
- batchId
- laboratoryId
- moisture
- pesticideStatus
- dnaAuthentication
- certificateReference
- result
- testedAt
- blockchainTxId

## CustodyTransfer
Fields:
- transferId
- batchId
- fromActorId
- toActorId
- quantity
- timestamp
- location
- blockchainTxId

## ProductBatch
Fields:
- productBatchId
- formulationId
- manufacturerId
- sourceBatchIds
- productName
- quantity
- manufacturingDate
- expiryDate
- qrCodeId
- status
- blockchainTxId

## Recall
Fields:
- recallId
- productBatchId
- reason
- severity
- createdBy
- createdAt
- status
- blockchainTxId
