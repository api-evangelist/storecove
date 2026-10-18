---
name: storecove-receive-and-retrieve-document
description: Receive a document and then retrieve it in the desired format.
api: openapi/storecove-openapi.yml
operations:
- receive_document
- get_received_document
- get_received_document_in_format
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/storecove-openapi.yml ; every operationId checked against the contract
---

# storecove-receive-and-retrieve-document

Receive a document and then retrieve it in the desired format.

## Steps

1. 1. Use `receive_document` to post a new document to `/legal_entities/{legal_entity_id}/received_documents`
2. 2. Use `get_received_document` to retrieve the document from `/received_documents/{guid}`
3. 3. Use `get_received_document_in_format` to retrieve the document in specific format from `/received_documents/{guid}/{format}`

## Rules

- Use bearerAuth authentication scheme
- The server base URL is https://api.storecove.com/api/v2
- Document retrieval requires the guid parameter from the receive operation
- Format-specific retrieval requires both guid and format parameters
