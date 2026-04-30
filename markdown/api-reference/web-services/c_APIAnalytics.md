---
title: Analyze REST and SOAP API usage
description: REST and SOAP API analytics allow you to track and analyze web service API usage.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Analyze REST and SOAP API usage

REST and SOAP API analytics allow you to track and analyze web service API usage.

Use analytics to help answer questions such as

-   Which APIs are used most?
-   Which API versions are being used? Can I deprecate older versions?
-   Which API methods are being used?
-   What resources are being accessed?
-   Who is using each API and resource?

The instance tracks analytics for all inbound web services, including platform web services such as the REST Table API or the SOAP API, and custom web services such as scripted REST APIs and scripted SOAP web services. Analytics are aggregated by each resource and HTTP action combination.

Outbound web services, such as REST Messages, are not tracked.

-   **[Collect analytics for an API](../task/api-analytics-whitelist-domain.md)**  
Select which APIs to collect analytics for and select if requestor information should be collected for each API.
-   **[View REST &amp; SOAP API analytics](c_APIAnalyticsReports.md)**  
View overall API analytics, analytics per API, or analytics per requesting user in the REST &amp; SOAP API Analytics dashboard.
-   **[REST and SOAP API analytics collection and cleanup](c_APIAnalyticsCollectClean.md#)**  
API analytics uses scheduled jobs to collect and clean up analytics data.
-   **[API analytics properties](../reference/api-analytics-properties.md)**  
Certain properties control the behavior of API analytics.

**Parent Topic:**[Additional integration resources](../../outbound-web-services/concept/additional-integration-resources.md)

