---
name: send-document
description: Check a recipient's Peppol capabilities, submit an e-invoice/document through Storecove, and fetch delivery evidence.
api: Storecove API v2
generated: 2026-10-18
method: generated
source: openapi/storecove-openapi.yml
operations:
  - discovery_receives
  - discovery_exists
  - create_document_submission
  - show_document_submission_evidence
  - show_document_submission_evidence_by_type
---
# Send a document

1. `discovery_receives` (POST /discovery/receives) — check the recipient can receive the document type over the network; `discovery_exists` (POST /discovery/exists) checks only that the participant exists.
2. `create_document_submission` (POST /document_submissions) — submit the document on behalf of a legal entity; keep the returned `guid`. (The older `create_invoice_submission` is deprecated in the spec — do not use it.)
3. `show_document_submission_evidence` (GET /document_submissions/{guid}/evidence) or `show_document_submission_evidence_by_type` — retrieve delivery evidence.

Errors: 401/403 auth, 404 unknown guid, 422 validation. No idempotency key is declared: on a timeout, do not resubmit until you have checked evidence/webhooks for the first attempt, or the recipient may get a duplicate invoice.
