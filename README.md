# 🌿 AyurTrace — Blockchain-Based Ayurvedic Herb Traceability

> **Smart India Hackathon 2026 | Problem Statement: CHA-191**

A blockchain-powered traceability platform for tracking Ayurvedic medicinal herbs from **collection to final formulation**, providing verifiable provenance, geo-tagging, quality assurance, sustainability compliance, and consumer transparency.

---

## 📌 Problem Statement

The Ayurvedic herbal supply chain in India involves farmers, wild collectors, aggregators, processors, laboratories, manufacturers, and retailers.

Because the supply chain is highly fragmented, several challenges exist:

* ❌ Lack of transparent provenance
* ❌ Manual and unreliable record keeping
* ❌ Risk of herb adulteration and mislabeling
* ❌ Difficulty verifying geographical origin
* ❌ Over-harvesting of vulnerable medicinal plants
* ❌ Limited visibility into laboratory testing
* ❌ Difficulties in auditing the complete supply chain
* ❌ Lack of transparency for consumers

**CHA-191** proposes a permissioned blockchain system that creates a tamper-resistant record of an Ayurvedic herb's complete journey.

---

## 💡 Our Solution

**AyurTrace** creates a digital chain of custody for medicinal herbs.

Every important event in the supply chain is recorded and linked together:

```text
Farmer / Wild Collector
        ↓
Geo-Tagged Collection
        ↓
Aggregation
        ↓
Processing
        ↓
Laboratory Testing
        ↓
Manufacturer
        ↓
Ayurvedic Formulation
        ↓
QR Code Generation
        ↓
Consumer Verification
```

Each event is digitally signed and stored on a **permissioned blockchain**, allowing authorized stakeholders to verify the authenticity and history of a product.

---

## 🎯 Key Features

### 1. 🌍 Geo-Tagged Collection

Collectors can record:

* GPS coordinates
* Collection timestamp
* Collector ID
* Plant species
* Quantity collected
* Initial quality information
* Collection conditions

The system can verify whether the collection location falls within an approved harvesting region.

---

### 2. ⛓️ Permissioned Blockchain

The platform uses a permissioned blockchain to maintain a trusted supply-chain ledger.

Potential implementation:

* Hyperledger Fabric
* Smart Contracts / Chaincode
* Role-based network participants
* Immutable transaction history

Example participants:

```text
Farmer Cooperative
      │
      ├── Collector
      │
      ├── Laboratory
      │
      ├── Processor
      │
      └── Manufacturer
```

---

### 3. 🤖 Smart Contract Validation

Smart contracts automatically validate supply-chain rules before accepting transactions.

Examples:

```text
Is collection location approved?
          ↓
        YES
          ↓
Is harvesting season valid?
          ↓
        YES
          ↓
Is species allowed?
          ↓
        YES
          ↓
Record Collection Event
```

Possible validations include:

* Geo-fencing
* Seasonal harvesting restrictions
* Species-specific limits
* Quantity limits
* Quality thresholds
* Sustainability requirements

---

### 4. 🧪 Quality Testing

Laboratories can add verified quality-test records to a batch.

Example:

```json
{
  "batchId": "ASH-2026-001",
  "moisture": "8.2%",
  "pesticideStatus": "PASS",
  "dnaAuthentication": "PASS",
  "laboratory": "LAB-001",
  "timestamp": "2026-08-16T10:30:00Z"
}
```

The results become part of the product's traceability history.

---

### 5. ⚙️ Processing Traceability

Every major processing stage can be recorded.

Examples:

* Drying
* Cleaning
* Grinding
* Storage
* Packaging
* Formulation

Each stage records:

* Processing facility
* Operator
* Timestamp
* Batch ID
* Processing conditions
* Previous event hash

---

### 6. 📱 QR-Based Consumer Verification

Every finished product receives a unique QR code.

```text
                ┌───────────────┐
                │  PRODUCT QR   │
                └───────┬───────┘
                        ↓
                 Scan QR Code
                        ↓
                 AyurTrace API
                        ↓
               Blockchain Ledger
                        ↓
        ┌───────────────┴───────────────┐
        ↓                               ↓
 Collection Information          Quality Reports
        ↓                               ↓
 Processing History              Sustainability
        ↓                               ↓
      Manufacturer                 Authenticity
```

Consumers can view:

* Origin of the herb
* Collection location
* Harvest date
* Supply-chain history
* Laboratory results
* Processing history
* Sustainability information
* Manufacturer information

---

## 🗺️ Interactive Provenance Map

The platform provides a geographical visualization of the herb's journey.

Example:

```text
📍 Collection Point
       ↓
📍 Aggregation Center
       ↓
📍 Processing Facility
       ↓
📍 Laboratory
       ↓
📍 Manufacturing Facility
```

The map can display relevant supply-chain events while protecting sensitive information where necessary.

---

## 📊 Stakeholder Dashboard

Different users receive role-specific dashboards.

### 👨‍🌾 Farmer / Collector

* Register collection
* Capture GPS coordinates
* Record harvested quantity
* View collection history
* Offline data capture

### 🧪 Laboratory

* Receive batch
* Upload test results
* Verify sample
* Submit quality certificate

### 🏭 Processor

* Record processing events
* Update batch status
* Track inventory

### 🏢 Manufacturer

* Track complete provenance
* Create formulations
* Generate QR codes
* Monitor batches

### 🛡️ Regulator

* Monitor supply chains
* Verify compliance
* Investigate suspicious batches
* Generate reports

### 👤 Consumer

* Scan QR code
* Verify authenticity
* View product journey
* View quality information

---

# 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │     Consumers       │
                    │   QR Verification   │
                    └──────────┬──────────┘
                               │
                               ↓
                    ┌─────────────────────┐
                    │   Consumer Portal   │
                    └──────────┬──────────┘
                               │
                               ↓
┌─────────────┐       ┌─────────────────────┐       ┌──────────────┐
│   Farmers   │──────→│                     │←──────│ Laboratories │
└─────────────┘       │      Backend API    │       └──────────────┘
                      │                     │
┌─────────────┐──────→│ Authentication/RBAC │←──────┌──────────────┐
│  Processors │       └──────────┬──────────┘       │ Manufacturers│
└─────────────┘                  │                  └──────────────┘
                                 ↓
                      ┌─────────────────────┐
                      │ Permissioned        │
                      │ Blockchain Network   │
                      │   Hyperledger        │
                      │      Fabric          │
                      └──────────┬──────────┘
                                 │
                                 ↓
                      ┌─────────────────────┐
                      │ Off-chain Storage   │
                      │ Documents / Reports │
                      └─────────────────────┘
```

---

# 🧩 Technology Stack

## Frontend

* React.js
* Next.js
* Tailwind CSS
* Leaflet / Mapbox
* QR Scanner

## Backend

* Node.js
* Express.js
* REST APIs
* JWT Authentication
* Role-Based Access Control

## Blockchain

* Hyperledger Fabric
* Fabric Chaincode
* Fabric CA
* Permissioned Network

## Database

* PostgreSQL
* Redis *(optional)*

## Storage

* IPFS / Object Storage for certificates and documents

## Maps & Geo-Location

* GPS
* OpenStreetMap
* Leaflet / Mapbox

## QR

* QR Code Generator
* QR Scanner

## Deployment

* Docker
* Docker Compose
* GitHub
* Cloud infrastructure

---

# 🔄 Supply Chain Workflow

## Step 1 — Collection

The collector opens the mobile/web application.

```text
Species → Quantity → GPS → Timestamp → Collector ID
```

A `CollectionEvent` is created.

---

## Step 2 — Blockchain Validation

The smart contract checks:

```text
✓ Authorized collector
✓ Approved geographical region
✓ Valid harvesting season
✓ Allowed species
✓ Sustainable quantity
```

If all conditions pass, the transaction is recorded.

---

## Step 3 — Processing

The processor receives the batch and records processing events.

```text
Collection
    ↓
Drying
    ↓
Cleaning
    ↓
Grinding
    ↓
Storage
```

---

## Step 4 — Laboratory Testing

The laboratory records:

```text
Moisture
Pesticide Test
DNA Authentication
Other Quality Parameters
```

The test result is attached to the batch.

---

## Step 5 — Formulation

The manufacturer uses verified herbs to create the final Ayurvedic formulation.

A new finished-product batch is created.

---

## Step 6 — QR Generation

The platform generates a unique QR code.

```text
Product ID
     +
Batch ID
     +
Blockchain Record
     ↓
Unique QR Code
```

---

## Step 7 — Consumer Verification

The consumer scans the QR code and receives a simplified provenance report.

```text
AUTHENTIC PRODUCT ✓

Origin: Gujarat
Species: Ashwagandha
Harvest: July 2026

Quality:
✓ DNA Authentication
✓ Pesticide Test
✓ Moisture Test

Supply Chain:
✓ Collector
✓ Processor
✓ Laboratory
✓ Manufacturer
```

---

# 🔐 Security

Security is a core component of AyurTrace.

### Authentication

JWT-based authentication with role-based access control.

### Blockchain Integrity

Supply-chain transactions are recorded on a permissioned ledger.

### Digital Signatures

Authorized participants digitally sign important transactions.

### Data Validation

Smart contracts validate submitted events.

### Privacy

Sensitive information such as private farmer information can be restricted based on user role.

---

# 📡 Offline & Low-Connectivity Support

Many herb collection locations may have poor internet connectivity.

Our system therefore supports:

```text
              NO INTERNET
                   ↓
             Mobile Device
                   ↓
            Store Locally
                   ↓
             Connection
              Restored
                   ↓
             Sync Queue
                   ↓
            Backend API
                   ↓
             Blockchain
```

This allows collectors to record information even without continuous connectivity.

---

# 📦 Standardized Data Model

The platform uses structured event models.

### CollectionEvent

```json
{
  "eventType": "CollectionEvent",
  "batchId": "ASH-001",
  "species": "Withania somnifera",
  "collectorId": "COL-001",
  "latitude": 22.3072,
  "longitude": 73.1812,
  "quantity": 25,
  "timestamp": "2026-08-16T08:30:00Z"
}
```

### ProcessingStep

```json
{
  "eventType": "ProcessingStep",
  "batchId": "ASH-001",
  "process": "Drying",
  "facilityId": "FAC-001",
  "timestamp": "2026-08-17T10:00:00Z"
}
```

### QualityTest

```json
{
  "eventType": "QualityTest",
  "batchId": "ASH-001",
  "laboratoryId": "LAB-001",
  "moisture": 8.2,
  "pesticideStatus": "PASS",
  "dnaStatus": "PASS"
}
```

---

# 🗃️ Project Structure

```text
ayurtrace/
│
├── frontend/
│   ├── src/
│   ├── components/
│   ├── pages/
│   └── services/
│
├── backend/
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── middleware/
│   └── services/
│
├── blockchain/
│   ├── chaincode/
│   ├── network/
│   ├── organizations/
│   └── config/
│
├── mobile/
│   ├── screens/
│   ├── components/
│   └── services/
│
├── database/
│   └── migrations/
│
├── docs/
│   ├── architecture/
│   ├── api/
│   └── diagrams/
│
├── docker-compose.yml
├── .env.example
└── README.md
```

---

# 🚀 MVP Scope

For the SIH prototype, the following workflow will be demonstrated:

```text
Ashwagandha Collection
        ↓
GPS Capture
        ↓
Blockchain Registration
        ↓
Processing Event
        ↓
Laboratory Test
        ↓
Manufacturer
        ↓
QR Generation
        ↓
Consumer Scan
        ↓
Complete Provenance
```

### MVP Features

* [x] User authentication
* [x] Role-based access
* [x] Herb/batch registration
* [x] GPS collection
* [x] Blockchain transaction
* [x] Processing records
* [x] Quality-test records
* [x] QR generation
* [x] QR verification
* [x] Provenance timeline
* [x] Interactive map
* [x] Stakeholder dashboard
* [ ] Advanced IoT integration
* [ ] SMS-based synchronization
* [ ] ERP integration

---

# 📈 Future Scope

The platform can be expanded with:

* IoT environmental sensors
* AI-based adulteration detection
* Satellite-based harvesting verification
* Demand forecasting
* Carbon-footprint tracking
* Automated recall management
* National-level medicinal plant registry integration
* ERP integration
* Export certification automation
* Advanced analytics
* Mobile applications for Android/iOS

---

# 🎯 Expected Impact

AyurTrace aims to create a more transparent and trustworthy Ayurvedic supply chain.

### For Farmers

* Better visibility of verified produce
* Potential premium pricing
* Digital collection records

### For Manufacturers

* Reliable provenance
* Faster audits
* Better batch management

### For Regulators

* Transparent supply-chain monitoring
* Easier compliance verification
* Improved conservation monitoring

### For Consumers

* Product authenticity verification
* Transparent sourcing
* Access to quality information

### For Biodiversity

* Better monitoring of medicinal plant harvesting
* Reduced over-harvesting
* Incentives for sustainable sourcing

---

# 🏆 SIH 2026 Alignment

| Requirement             | AyurTrace Implementation         |
| ----------------------- | -------------------------------- |
| Permissioned Blockchain | Hyperledger Fabric               |
| Geo-tagged Collection   | GPS-enabled application          |
| Smart Contracts         | Chaincode validation             |
| Sustainability          | Geo-fencing & harvesting rules   |
| Quality Testing         | Digital laboratory records       |
| Traceability            | Immutable supply-chain events    |
| QR Verification         | Consumer QR portal               |
| Low Connectivity        | Offline-first data capture       |
| Standardized Metadata   | Event-based data models          |
| Dashboards              | Stakeholder analytics            |
| Compliance              | Automated validation & reporting |

---

# 👥 Team

**Team Name:** `Corruption.exe`

### Team Members

| Role                  | Responsibility                            |
| --------------------- | ----------------------------------------- |
| Team Leader           | Architecture & Integration                |
| Frontend Developer    | Web Dashboard & Consumer Portal           |
| Backend Developer     | APIs & Authentication                     |
| Blockchain Developer  | Hyperledger Fabric & Chaincode            |
| AI/IoT Developer      | Sensors, Analytics & Intelligent Features |
| UI/UX & Documentation | Design, Testing & Presentation            |

---

# 📜 License

This project is developed as a prototype for **Smart India Hackathon 2026**.

---

## 🌿 AyurTrace

**From the field to the formulation — verify every step.**

> **Trust the herb. Trace the journey.**
