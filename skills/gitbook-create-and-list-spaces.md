---
name: gitbook-create-and-list-spaces
description: Create a new space in an organization and then list all spaces in that organization.
api: openapi/gitbook-spaces-api-openapi.yml
operations:
- createSpaceInOrganization
- listSpacesInOrganization
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/gitbook-spaces-api-openapi.yml ; every operationId checked against the contract
---

# gitbook-create-and-list-spaces

Create a new space in an organization and then list all spaces in that organization.

## Steps

1. 1. Use `createSpaceInOrganization` with the required request body fields (unspecified) and the `Authorization: Bearer <token>` header.
2. 2. Use `listSpacesInOrganization` with the `Authorization: Bearer <token>` header and optional `page` query parameter for pagination.

## Rules

- Auth: Include `Authorization: Bearer <token>` header (bearerAuth).
- Pagination: Use `page` query parameter on list operations.
- Rate limit: No explicit limit; on exhaustion the API returns no specific HTTP status.
