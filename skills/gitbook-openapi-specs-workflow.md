---
name: gitbook-openapi-specs-workflow
description: Upload a new OpenAPI specification, then retrieve it and list all specifications for an organization.
api: openapi/gitbook-openapi-specs-api-openapi.yml
operations:
- listOpenAPISpecs
- uploadOpenAPISpec
- getOpenAPISpec
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/gitbook-openapi-specs-api-openapi.yml ; every operationId checked against the contract
---

# gitbook-openapi-specs-workflow

Upload a new OpenAPI specification, then retrieve it and list all specifications for an organization.

## Steps

1. 1. `listOpenAPISpecs` – provide the `organizationId` path parameter and optional `page` query parameter for pagination.
2. 2. `uploadOpenAPISpec` – provide the `organizationId` path parameter and the OpenAPI specification in the request body (e.g., JSON or YAML).
3. 3. `getOpenAPISpec` – provide the `organizationId` and `specSlug` path parameters to retrieve the uploaded specification.

## Rules

- All requests require an `Authorization: Bearer <token>` header (bearerAuth).
- Pagination is controlled via the `page` query parameter on `listOpenAPISpecs`.
- No rate‑limit information is provided; assume standard HTTP error handling on exhaustion.
