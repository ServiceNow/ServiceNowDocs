---
title: Outbound web services: Logging
description: Log requests and responses for outbound web services such as REST and SOAP.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Outbound web services, Web services, API implementation, API implementation and reference]
---

# Outbound web services: Logging

Log requests and responses for outbound web services such as REST and SOAP.

gOutbound request logging allows you to better understand what 3rd-party services your instance accesses and the volume of outbound requests. Additionally, logging can provide valuable information when debugging outbound integrations.

Outbound web services logging tracks outbound REST and SOAP requests, as well as outbound requests made using the GlideHTTPRequest and GlideHTTPClient APIs.

To view outbound web service logs, navigate to **System Logs** &gt; **Outbound HTTP Requests**.

All log information is read only.

-   **[Configure outbound logging](outbound-logging-configure.md#)**  
You can configure outbound request logging to log basic, elevated, or all HTTP request and response information for specific domains.
-   **[Outbound request logging exclusion domain requirements](../reference/outbound-logging-list-reqs.md#)**  
When you exclude outbound request logging for a domain, the value you enter in the Domain field must meet certain requirements.
-   **[Outbound web service logging properties](../reference/outbound-logging-properties.md)**  
These properties allow you to control the behavior of outbound web service request logging.

**Parent Topic:**[Outbound web services](outbound-web-services.md)

