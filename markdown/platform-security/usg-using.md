---
title: Using Unified Secrets Gateway
description: Use Unified Secrets Gateway \(USG\) to retrieve secrets through APIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/usg-using.html
release: brazil
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [unified secrets gateway, APIs, secret retrieval, Java API, Server API]
breadcrumb: [Unified Secrets Gateway, Encryption]
---

# Using Unified Secrets Gateway

Use Unified Secrets Gateway \(USG\) to retrieve secrets through APIs.

USG provides two methods to retrieve secrets:

-   Java API
-   Server API

All API methods include full authorization validation and comprehensive audit logging of every access attempt.

## Retrieve secrets using the Java API

Call SecretsAPI.getSecret\(\) or SecretsAPI.getSecrets\(\) from Java applications and server-side integrations to retrieve individual or batch secrets.

## Retrieve secrets using the Server API

Use the scriptable API to retrieve secrets from background scripts, business rules, flows, or other server-side scripts.

## Related API documentation

For detailed API specifications, parameters, and code examples, see [Secrets API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/SecretsAPI.md).

**Parent Topic:**[Unified Secrets Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-landing.md)

