# API Contract

## Authentication
POST /api/auth/login
POST /api/auth/register

## Collection
POST /api/collections
GET /api/collections/:id
GET /api/collections

## Processing
POST /api/processing
GET /api/processing/:id

## Quality
POST /api/quality-tests
GET /api/quality-tests/:id

## Custody
POST /api/custody-transfers
GET /api/batches/:id/custody

## Products
POST /api/products/batches
GET /api/products/batches/:id

## QR
POST /api/products/batches/:id/qr
GET /api/verify/:qrCode

## Provenance
GET /api/provenance/:batchId

## Recall
POST /api/recalls
GET /api/recalls/:batchId

## Dashboard
GET /api/dashboard/overview
GET /api/dashboard/collections
GET /api/dashboard/quality
GET /api/dashboard/sustainability

## API Rules
- All APIs use JSON.
- Authentication is required for stakeholder operations.
- Consumer provenance verification does not require an account.
- API responses must use consistent error formats.
- API endpoints must not be renamed without updating this document.
