---
name: storecove-manage-administration
description: Create, retrieve, update, or delete an administration record for a legal entity.
api: openapi/storecove-openapi.yml
operations:
- create_administration
- get_administration
- update_administration
- delete_administration
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/storecove-openapi.yml ; every operationId checked against the contract
---

# storecove-manage-administration

Create, retrieve, update, or delete an administration record for a legal entity.

## Steps

1. 1. Create a new administration using `create_administration` with the legal_entity_id path parameter and administration data in the request body
2. 2. Retrieve an existing administration using `get_administration` with the legal_entity_id and id path parameters
3. 3. Update an administration using `update_administration` with the legal_entity_id and id path parameters and updated data in the request body
4. 4. Delete an administration using `delete_administration` with the legal_entity_id and id path parameters

## Rules

- All operations require bearerAuth authentication header
- All operations are DEPRECATED according to the documentation
- Operations use the base server URL https://api.storecove.com/api/v2
