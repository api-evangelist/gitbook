---
name: gitbook-manage-docs-sites
description: Create, view, update, list, and delete a GitBook docs site within an organization.
api: openapi/gitbook-docs-sites-api-openapi.yml
operations:
- createDocsSite
- listDocsSites
- getDocsSite
- updateDocsSite
- deleteDocsSite
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/gitbook-docs-sites-api-openapi.yml ; every operationId checked against the contract
---

# gitbook-manage-docs-sites

Create, view, update, list, and delete a GitBook docs site within an organization.

## Steps

1. 1. Use `createDocsSite` – send a POST request with a JSON body containing the site details and include the `Authorization: Bearer <token>` header.
2. 2. Use `listDocsSites` – send a GET request with the `Authorization: Bearer <token>` header and optional `page` query parameter for pagination.
3. 3. Use `getDocsSite` – send a GET request with the `Authorization: Bearer <token>` header, specifying `organizationId` and `siteId` in the path.
4. 4. Use `updateDocsSite` – send a PATCH request with a JSON body of fields to modify, the `Authorization: Bearer <token>` header, and `organizationId`/`siteId` in the path.
5. 5. Use `deleteDocsSite` – send a DELETE request with the `Authorization: Bearer <token>` header, specifying `organizationId` and `siteId` in the path.

## Rules

- All requests require the `Authorization: Bearer <token>` header (bearerAuth).
- Pagination for `listDocsSites` uses the `page` query parameter.
- No explicit rate‑limit headers are documented; exhaustion results in an HTTP error with no specific status code provided.
