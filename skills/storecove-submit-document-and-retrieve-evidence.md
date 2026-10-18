---
name: storecove-submit-document-and-retrieve-evidence
description: Submit a document and retrieve its evidence from Storecove's DocumentSubmissions API.
api: openapi/storecove-openapi.yml
operations:
- create_document_submission
- show_document_submission_evidence
- show_document_submission_evidence_by_type
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/storecove-openapi.yml ; every operationId checked against the contract
---

# storecove-submit-document-and-retrieve-evidence

Submit a document and retrieve its evidence from Storecove's DocumentSubmissions API.

## Steps

1. 1. Submit a new document using `create_document_submission` with the required document fields in the request body
2. 2. Retrieve all evidence for the submitted document using `show_document_submission_evidence` with the `guid` path parameter from the submission response
3. 3. Retrieve specific evidence types using `show_document_submission_evidence_by_type` with both `guid` and `evidence_type` path parameters

## Rules

- Use bearerAuth authentication scheme with HTTP bearer token
- All operations use the base server URL: https://api.storecove.com/api/v2
- Document submissions require a `guid` path parameter for evidence retrieval operations
