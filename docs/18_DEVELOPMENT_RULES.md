# Development Rules

## Rule 1 — Single Source of Truth
The `/docs` directory is the single source of truth. All developers and AI assistants must follow these documents.

## Rule 2 — Discuss Architectural Changes
Do not make architectural changes without discussing them with the team.

## Rule 3 — Do Not Break Contracts
Do not change:
- API endpoints
- Database entities
- JSON structures
- Blockchain entities
- Authentication roles
without updating the relevant specification first.

## Rule 4 — Small Changes
Implement one feature at a time.
Do not rewrite unrelated parts of the application.

## Rule 5 — Explain Changes
Every major change must include:
- What changed
- Why it changed
- Files changed
- How to test it

## Rule 6 — No Fake Blockchain
The final system must use an actual permissioned blockchain prototype.
Do not simply create a database table called "blockchain."

## Rule 7 — No Fake AI
If AI functionality is demonstrated, it must actually execute an AI/analytics process.
Do not hard-code AI results.

## Rule 8 — No Hard-Coded Secrets
Never commit:
- API keys
- Passwords
- Private keys
- Blockchain credentials
- Database passwords

## Rule 9 — Git
Use feature branches.

Example:
- feature/collector
- feature/blockchain
- feature/lab
- feature/consumer-portal
- feature/ai

## Rule 10 — Integration
Before merging a feature:
1. Build
2. Run tests
3. Test API integration
4. Verify no existing functionality is broken

## Rule 11 — Source of Truth
The documentation in `/docs` is the source of truth.
If implementation conflicts with documentation:
STOP and resolve the conflict.

## Rule 12 — AI Is an Assistant
AI-generated code must be reviewed and understood by the team member responsible for that component.
