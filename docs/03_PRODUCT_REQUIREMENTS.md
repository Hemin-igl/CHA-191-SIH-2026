# Product Requirements

## Roles & User Types
- Collector / Farmer
- Processor
- Laboratory
- Manufacturer
- Administrator
- Consumer

## Functional Requirements

### 1. User Management & Authentication
- Stakeholders must authenticate securely.
- Role-Based Access Control (RBAC) enforced for all system interactions.

### 2. Collection Event
A collector must be able to record:
- Species
- Collector ID
- Quantity
- Latitude
- Longitude
- Timestamp
- Collection area
- Initial quality information

### 3. Geo Validation
The system must determine whether the collection location is within an approved harvesting zone.

### 4. Processing Event
A processor can record:
- Batch ID
- Processing type
- Facility
- Start time
- End time
- Conditions
- Quantity

Examples:
- Drying
- Grinding
- Storage
- Packaging

### 5. Quality Test
A laboratory can record:
- Moisture result
- Pesticide result
- DNA authentication result
- Laboratory ID
- Certificate/reference
- Timestamp
- Pass/Fail status

### 6. Batch Creation
A manufacturer can combine validated upstream material into a final product batch.

### 7. QR Code
Each finished product batch receives a unique QR code.

### 8. Consumer Portal
Consumer scans QR and sees:
- Product
- Batch
- Origin
- Collection location
- Collection date
- Processing history
- Laboratory results
- Sustainability status
- Manufacturer
- Verification status

### 9. Recall
Administrator/manufacturer can mark a batch as recalled.
Consumers scanning the QR code must see the recall warning.

### 10. Dashboard
Stakeholders can see:
- Active batches
- Collection volume
- Failed tests
- Processing status
- Suspicious events
- Sustainability metrics
- Recall status
