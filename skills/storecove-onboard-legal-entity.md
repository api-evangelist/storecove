---
name: onboard-legal-entity
description: Register a sender/receiver legal entity in Storecove and give it a Peppol identifier so it can exchange e-invoices.
api: Storecove API v2
generated: 2026-10-18
method: generated
source: openapi/storecove-openapi.yml
operations:
  - create_legal_entity
  - get_legal_entity
  - create_peppol_identifier
  - create_additional_tax_identifier
---
# Onboard a legal entity

Base URL `https://api.storecove.com/api/v2`, `Authorization: Bearer <API key>` (securityScheme `bearerAuth`).

1. `create_legal_entity` (POST /legal_entities) — create the company record; keep the returned `id`.
2. `get_legal_entity` (GET /legal_entities/{id}) — confirm the stored data.
3. `create_peppol_identifier` (POST /legal_entities/{legal_entity_id}/peppol_identifiers) — attach the Peppol identifier (superscheme/scheme/identifier) so the entity can receive over Peppol.
4. Optionally `create_additional_tax_identifier` for extra tax/VAT identifiers.

Errors declared in the spec: 401 (bad key), 403 (not allowed), 404 (unknown legal entity), 422 (validation — fix the body, do not retry unchanged). The spec declares no idempotency key, so do not blindly retry POSTs; read back with `get_legal_entity` first.
