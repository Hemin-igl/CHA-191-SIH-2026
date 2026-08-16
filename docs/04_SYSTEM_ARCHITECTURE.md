# System Architecture

## High-Level Architecture

Users
  |
  +--> Collector Mobile/Web App
  |
  +--> Processor Dashboard
  |
  +--> Laboratory Dashboard
  |
  +--> Manufacturer Dashboard
  |
  +--> Admin Dashboard
  |
  +--> Consumer QR Portal
              |
              v
        API Gateway / Backend
              |
       +------+------+
       |             |
       v             v
   Blockchain      Off-chain
   Network         Database
       |             |
       v             v
   Hyperledger     PostgreSQL
   Fabric
       |
       v
   Chaincode
       |
       +--> CollectionEvent
       +--> ProcessingStep
       +--> QualityTest
       +--> CustodyTransfer
       +--> ProductBatch
       +--> Recall


AI/Analytics Layer
       |
       +--> Anomaly Detection
       +--> Geo Anomaly Detection
       +--> Demand Forecasting


QR Service
       |
       +--> Product Batch QR
