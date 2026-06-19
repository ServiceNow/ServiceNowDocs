---
title: Using special characters in URIs
description: A REST function URI or function variable may use special characters, such as pipe \(\|\) characters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/c\_UsingSpecialCharactersInURIs.html
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a message, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# Using special characters in URIs

A REST function URI or function variable may use special characters, such as pipe \(\|\) characters.

When using these characters in a REST message, use URL encoding to escape these characters. For example, to use a parameter value of **user\|title**, enter `user%7Ctitle`. Entering special characters directly may cause the REST message to fail and display the response Invalid uri &lt;URI&gt;: Invalid query.

**Parent Topic:**[Create a REST message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/t_ConfiguringARESTMessage.md)

