---
name: api-docs
description: Writes reference documentation for REST API endpoints from the
  route handlers and types, with parameters, request and response examples,
  and errors. Use when the user asks to document an API, an endpoint or a
  route.
---

# API docs

For each endpoint, read the handler, its validation and its types, then
write:

1. **Heading**: method and path, for example `POST /v1/invoices`.
2. **Summary**: one sentence on what it does.
3. **Auth**: what is required, or "None".
4. **Parameters**: table with name, where (path, query, body), type,
   required, and description. Include defaults and limits from the code.
5. **Example request**: a curl command with realistic values.
6. **Example response**: the success JSON, trimmed to the important fields.
7. **Errors**: table of status code, error code and when it happens.

Only document behavior you can see in the code. If something is unclear,
such as a rate limit, add a "To confirm" note instead of guessing.
