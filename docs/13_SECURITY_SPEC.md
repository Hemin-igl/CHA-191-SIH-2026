# Security Specification

## Authentication
Stakeholder users must authenticate.

## Authorization
Use role-based access control (RBAC).

Roles:
- COLLECTOR
- PROCESSOR
- LAB
- MANUFACTURER
- ADMIN

## Security Requirements
- Passwords must never be stored in plain text.
- Secrets must be stored in environment variables.
- API authorization must be enforced server-side.
- Users must not be able to modify unauthorized records.
- Blockchain identity must correspond to authorized participants.
- Consumer APIs must not expose sensitive personal information.
- Validate all user inputs.
- Prevent duplicate transactions.
- Log important security events.

## Privacy Rules
Do not expose:
- Personal phone numbers
- Private addresses
- Authentication credentials
- Private blockchain identities
- Sensitive farmer information
to consumers unless explicitly required.
