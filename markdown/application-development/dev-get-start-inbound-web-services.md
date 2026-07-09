---
title: Inbound web services
description: Inbound web services enable external systems to read data from or write data to your custom application. External systems can query your data, create records, or exchange information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/dev-get-start-inbound-web-services.html
release: australia
topic_type: concept
last_updated: "2026-06-22"
reading_time_minutes: 2
keywords: [Integrations, low-code]
breadcrumb: [Integrations, Standard app development, Getting Started guide for developers, Building applications]
---

# Inbound web services

Inbound web services enable external systems to read data from or write data to your custom application. External systems can query your data, create records, or exchange information.

Inbound web services are the channel external systems use to pull data from your custom app or push data to it. An external system makes an HTTP request to your ServiceNow custom app, asking for data or submitting data to be stored. The request follows a specific format \(a protocol\) that your instance understands. Your instance processes the request, retrieves or stores the data from the app, and sends back a response. The external system receives the response and continues its workflow.

You can use inbound web services for any of the following scenarios:

-   A human resources system queries your custom app for a list of active employees.
-   A billing platform creates invoices in your custom app when purchase orders are approved.
-   A monitoring tool sends alert data to your custom app to create incidents automatically.

For more information about inbound web services, see [Inbound web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/inbound-web-services.md).

## Supported protocols on the ServiceNow AI Platform

The ServiceNow AI Platform supports several web service protocols for inbound communication. A protocol is a set of rules for how two systems exchange information. The following protocols can be integrated with almost any application:

-   **SOAP web service**

    SOAP is an XML-based protocol that uses formal message envelopes. SOAP is a traditional enterprise choice, commonly used by legacy systems and when strict data structure enforcement is required. For more information, see [SOAP web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_SOAPWebService.md).

-   **JSONv2 web service**

    JSONv2 uses JSON format for lightweight data exchange. JSONv2 is commonly used for cloud applications and when you want flexibility in the data structure. For more information, see [JSONv2 web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_JSONv2WebService.md).

-   **RSS web service**

    RSS is an XML feed format for publishing regularly changing data like news or alerts. Use RSS when the external system needs to subscribe to a live data feed from your custom app. For more information, see [RSS web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/p_RSS.md).

-   **Data export in complex formats**

    You can extract ServiceNow records and convert them to JSON, XML, PDF, CSV, XLS, and other formats for external systems that require certain data types. For more information, see [Exporting and converting records into complex data types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/store-retrieve-records-complex-data-type.md).


**Parent Topic:**[Integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-integrations.md)

