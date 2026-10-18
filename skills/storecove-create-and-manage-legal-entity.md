---
name: storecove-create-and-manage-legal-entity
description: Create and manage a legal entity in Storecove's system.
api: openapi/storecove-openapi.yml
operations:
- create_legal_entity
- get_legal_entity
- update_legal_entity
- delete_legal_entity
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/storecove-openapi.yml ; every operationId checked against the contract
---

# storecove-create-and-manage-legal-entity

Create and manage a legal entity in Storecove's system.

## Steps

1. 1. Create a new legal entity using `create_legal_entity` operation with the required fields in the request body
2. 2. Retrieve the created legal entity using `get_legal_entity` operation with the `id` path parameter
3. 3. Update the legal entity using `update_legal_entity` operation with the `id` path parameter and fields to update in the request body
4. 4. Delete the legal entity using `delete_legal_entity` operation with the `id` path parameter

## Rules

- Authentication uses bearerAuth scheme with Authorization header
- All operations use the base server URL https://api.storecove.com/api/v2
- Resource identification uses `id` path parameter for GET, PATCH, and DELETE operations
