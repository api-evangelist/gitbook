---
name: gitbook-collection-management
description: Create a collection, retrieve it, list collections in the organization, and delete the collection.
api: openapi/gitbook-collections-api-openapi.yml
operations:
- createCollection
- getCollection
- listCollectionsInOrganization
- deleteCollection
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/gitbook-collections-api-openapi.yml ; every operationId checked against the contract
---

# gitbook-collection-management

Create a collection, retrieve it, list collections in the organization, and delete the collection.

## Steps

1. 1. `createCollection` – provide the `organizationId` path parameter and the request body fields for the new collection.
2. 2. `getCollection` – supply the `collectionId` path parameter to retrieve the created collection.
3. 3. `listCollectionsInOrganization` – supply the `organizationId` path parameter and optional `page` query parameter for pagination.
4. 4. `deleteCollection` – supply the `collectionId` path parameter to remove the collection.

## Rules

- All requests require an `Authorization: Bearer <token>` header (bearerAuth).
- Pagination for listing uses the `page` query parameter.
- No specific rate‑limit headers are defined; exhaustion returns an HTTP status without a custom code.
