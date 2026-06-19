---
title: Encryption rule actions
description: An encryption rule maps fields in a client request to fields in a table on your instance and identifies fields marked for encryption.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/edge-encryption/c\_EncryptionRuleActions.html
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Encryption rule actions

An encryption rule maps fields in a client request to fields in a table on your instance and identifies fields marked for encryption.

An encryption rule action only runs when the encryption rule condition returns true. An encryption rule identifies the data to be encrypted in your request payload. Because the rule iterates over the content in the request object, you must understand the form and structure of your request body and determine what in the request must be encrypted. The data to be encrypted might be located within:

-   A [POST or URL parameter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/param-apis.md).
-   JSON or XML content within a [POST or URL parameter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/param-apis.md).
-   A [JSON](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/json-overview.md) payload.
-   An [XML](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/xml-overview.md) payload.

Before writing an encryption rule action, be sure to:

-   [Inspect the client request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/request-type.md).
-   Identify where the sensitive data is located in the [request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_requestAPI.md) object.
-   Determine the field and table name to insert data into, or understand how to [dynamically pull this from the request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/param-apis.md).

[Encryption rule objects and APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/api-overview.md) are available to encryption rule actions and conditions.

**Parent Topic:**[Define a custom encryption rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_EncryptionRules.md)

