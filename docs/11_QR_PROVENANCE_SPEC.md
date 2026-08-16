# QR and Provenance Specification

## QR Purpose
Every finished product batch must have a unique QR identifier.

Example:
CHA191-ASH-2026-000001

## QR Content Rule
QR must NOT contain the entire provenance record.
QR should contain only a unique identifier or verification URL.

Example:
/verify/CHA191-ASH-2026-000001

## Verification Flow
QR
 ↓
Backend
 ↓
ProductBatch
 ↓
Source batches
 ↓
Collection events
 ↓
Processing events
 ↓
Quality tests
 ↓
Custody transfers
 ↓
Blockchain verification

## Consumer View
Consumer should see:
- Product name
- Batch number
- Verification status
- Collection region
- Collection date
- Processing history
- Laboratory results
- Sustainability status
- Manufacturer
- Recall status

Sensitive personal information must not be exposed.
