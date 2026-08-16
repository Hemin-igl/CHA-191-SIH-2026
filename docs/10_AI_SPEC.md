# AI Specification

AI is an assisting layer.
AI does NOT replace blockchain validation.

## AI Feature 1 — Anomaly Detection
Identify suspicious patterns such as:
- Unusually large harvest quantities
- Repeated collection from suspicious locations
- Unusual collection frequency
- Duplicate records
- Abnormal supply-chain behavior

Output:
- anomalyDetected
- riskScore
- reasons
- severity

## AI Feature 2 — Geo Anomaly Detection
Analyze collection GPS against:
- Approved harvesting zones
- Historical collection patterns
- Species distribution

Important:
Official geo-fence validation must be performed deterministically by the system/smart contract.

AI may flag suspicious patterns but must not override deterministic rules.

## AI Feature 3 — Demand Forecasting
Use:
- Consumer QR scans
- Historical product activity
- Batch information
to estimate future demand.

## AI Requirements
AI outputs must be:
- Explainable
- Logged
- Versioned where applicable
- Clearly separated from authoritative blockchain records

AI failures must not prevent basic traceability functionality.
