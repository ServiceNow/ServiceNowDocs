---
title: Encryption rule objects and APIs
description: Use encryption rule APIs to parse and encrypt values in requests moving through the Edge Encryption proxy server to the instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/edge-encryption/api-overview.html
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-06-21"
reading_time_minutes: 1
breadcrumb: [Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Encryption rule objects and APIs

Use encryption rule APIs to parse and encrypt values in requests moving through the Edge Encryption proxy server to the instance.

The APIs available for your encryption rule depend on the format of the request object. For example, if the contentType parameter of the request object is XML, you can use the [XML APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/xml-overview.md) to parse and encrypt values in the payload. After you determine the type of object in your request, you can build an encryption rule using the available APIs.

Encryption rule APIs are available in both encryption rule condition and action scripts.

-   **[request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_requestAPI.md)**  
The request object is a global object available in Edge Encryption rule action and condition scripts.
-   **[POST and URL parameter APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/param-apis.md)**  
POST and URL parameters can be accessed as properties of the request object using `request.postParams` and `request.urlParams`.
-   **[XML APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/xml-overview.md)**  
XML APIs can be used after calling getAsXmlContent\(\) on either the request object or a ParameterValue property.
-   **[JSON APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/json-overview.md)**  
JSON APIs can be used after calling getAsJsonContent\(\) on either the request object or a ParameterValue property.
-   **[print\(String message\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/r_GLBL-print_S.md)**  
Prints a message to the wrapper log file: `<proxy server directory>/logs/wrapper_<date>.log`.
-   **[Prohibited keywords](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/r_ProhibitedKeywords.md)**  
The Edge Encryption proxy validates encryption rule scripts before saving the rule. Many JavaScript keywords aren’t allowed in encryption rule scripts.

**Parent Topic:**[Define a custom encryption rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/edge-encryption/c_EncryptionRules.md)

