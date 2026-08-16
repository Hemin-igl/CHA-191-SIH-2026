# CHA-191 — Project Overview

## Project
Blockchain-Based Botanical Traceability System for Ayurvedic Herbs

## Problem ID
CHA-191

## Category
Blockchain & Cybersecurity

## Domain
Ayurvedic Herbal Supply Chain

## Project Goal
Build a proof-of-concept permissioned blockchain-based system that provides end-to-end traceability of Ayurvedic herbs from collection to final consumer product.

The system must capture and verify:
- Origin of the herb
- Collector identity
- GPS location
- Collection date and time
- Species information
- Initial quality information
- Chain of custody
- Processing events
- Laboratory quality tests
- Sustainability compliance
- Final formulation/batch information

A unique QR code should allow a consumer to retrieve the provenance of the final product.

## Pilot
The initial demonstration will focus on one botanical species:
Ashwagandha.

The architecture should remain extensible to other medicinal plants.

## Main Supply Chain
Collector/Farmer
        ↓
Collection Event
        ↓
Processor
        ↓
Processing Events
        ↓
Testing Laboratory
        ↓
Quality Tests
        ↓
Manufacturer
        ↓
Finished Product Batch
        ↓
QR Code
        ↓
Consumer

## Main Technologies
The proposed system will use:
- Permissioned blockchain
- Hyperledger Fabric
- Smart contracts / chaincode
- REST APIs
- Web dashboard
- Mobile/offline collection interface
- GPS/geolocation
- QR codes
- Database for off-chain data
- AI/analytics for anomaly detection and forecasting

## Core Principles
1. Blockchain stores trusted supply-chain events.
2. Large files are stored off-chain.
3. Every important event must have a traceable relationship to a batch.
4. Consumer information must be readable without requiring a specialized app.
5. Rural users must be able to capture data with poor connectivity.
6. Smart contracts must validate important compliance rules.
7. AI must assist the system but must not replace authoritative blockchain records.
8. The architecture must remain modular and extensible.
