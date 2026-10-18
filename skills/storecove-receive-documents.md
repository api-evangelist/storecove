---
name: receive-documents
description: Pull pending Storecove webhook instances, download each received document, and acknowledge by deleting the webhook instance.
api: Storecove API v2
generated: 2026-10-18
method: generated
source: openapi/storecove-openapi.yml
operations:
  - get_webhook_instances
  - get_received_document
  - get_received_document_in_format
  - delete_webhook_instance
---
# Receive documents

1. `get_webhook_instances` (GET /webhook_instances/) — fetch the next pending event; 204 means nothing is queued.
2. `get_received_document` (GET /received_documents/{guid}) or `get_received_document_in_format` (GET /received_documents/{guid}/{format}) — download the document referenced by the event.
3. `delete_webhook_instance` (DELETE /webhook_instances/{guid}) — remove the event only after the document is stored; it returns 204.

Errors: 400 (bad format), 401/403 auth, 404 unknown guid. Deleting is destructive: never delete before persisting the document.
