---
title: Exploring Unified Secrets Gateway
description: Learn the core concepts of Unified Secrets Gateway and how the three main components work together to control access to secrets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/usg-exploring.html
release: brazil
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [unified secrets gateway, alias groups, identity groups, consumer grants, access control]
breadcrumb: [Unified Secrets Gateway, Encryption]
---

# Exploring Unified Secrets Gateway

Learn the core concepts of Unified Secrets Gateway and how the three main components work together to control access to secrets.

By default, Unified Secrets Gateway \(USG\) denies access to all secrets. To grant access, you configure three linked components that work together:

-   **Alias Groups** \(which secrets\)
-   **Identity Groups** \(who can access\)
-   **Consumers** \(the link between them\)

\[Omitted image "usg-diagram.png"\] Alt text: Unified Secrets Gateway core components diagram showing Alias Groups and Identity Groups connecting through Consumers to produce Access Control Results.

Alias Groups organize your secrets by purpose and define where they're stored in ServiceNow. Identity Groups define which members \(MID Servers, services, or other authorized consumers\) should have access. Consumers connect identity groups to alias groups, establishing the access relationship.

You can create multiple Consumers to give different identity groups different access rights. For instance, one Consumer might let production MID Servers access database credentials while another lets integration services access API keys. Each Consumer has its own access policy, so access rules can vary across different secret groups.

## Security and Authorization

The API validates the member through multiple authorization steps before returning any secret. Caller identity is resolved from execution context, preventing unauthorized callers from spoofing requests. Every access attempt is logged, whether granted or denied, for auditing purposes.

## API Support

Unified Secrets Gateway can be accessed through the following APIs:

-   Java API
-   Server API

To retrieve secrets through USG, call the appropriate API with the alias group name and alias to request. The API validates the member through multiple authorization steps against the Consumer rules. If access is allowed, the API returns the secret. If access is denied, the API denies the request. All access attempts are logged for auditing purposes.

For detailed API specifications, parameters, and code examples, see [Secrets API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/server-api-reference/SecretsAPI.md).

**Parent Topic:**[Unified Secrets Gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/usg-landing.md)

