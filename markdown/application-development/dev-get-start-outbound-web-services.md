---
title: Outbound web services
description: Outbound web services send data from your custom app to external systems. With outbound web services, your app can notify, request, or update external platforms in real time or on a schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/dev-get-start-outbound-web-services.html
release: australia
topic_type: concept
last_updated: "2026-06-22"
reading_time_minutes: 2
keywords: [Integrations, low-code]
breadcrumb: [Integrations, Standard app development, Getting Started guide for developers, Building applications]
---

# Outbound web services

Outbound web services send data from your custom app to external systems. With outbound web services, your app can notify, request, or update external platforms in real time or on a schedule.

Outbound web services are the channel custom apps use to push data outward. Outbound web services follow a trigger-and-send pattern. You define a message template that describes what data to send and where to send it. Then you attach that message to a trigger, such as a business rule, scheduled job, or script. When the trigger runs, your app packages the specified data into a message, sends it over HTTPS to the external system, and waits for a response. The external system processes the message and sends back a result, which your app can parse and act on.

You might use outbound web services for any of the following scenarios:

-   A business rule detects a new incident and triggers an alert to an external ticketing system.
-   A scheduled job syncs user records to an identity management platform every night.
-   A custom form submits survey responses to a third-party analytics tool.

For more information about outbound web services, see [Outbound web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/outbound-web-services.md).

## Supported protocols on the ServiceNow AI Platform

The ServiceNow AI Platform supports two main web service protocols \(set of rules for how two systems exchange information\) for outbound communication: REST and SOAP.

-   **REST**

    REST is a protocol that is lightweight and JSON-friendly. REST is preferred for cloud-to-cloud integrations and APIs. For more information, see [Outbound REST web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_OutboundRESTWebService.md).

-   **SOAP**

    SOAP is an enterprise protocol with strict message structure. Choose SOAP when your external system requires it or you need complex XML handling. For more information, see [Outbound SOAP web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_OutboundSOAPWebService.md).


## Logging

When communicating with external systems, you need visibility into what messages are actually sent and come back. Logging captures the full request and response messages so that you can debug integration failures, support compliance audits, and troubleshoot errors.

For more information about logging, see [Outbound web services: Logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/outbound-request-logging.md).

## Authentication

Depending on the type of data your app is exchanging, consider adding mutual authentication to establish trust between your instance and the external system. Mutual authentication is critical when both sides are protecting sensitive data. For more information, see [Outbound web service mutual authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_OutboundWebServicesMutualAuth.md).

**Parent Topic:**[Integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/dev-get-start-integrations.md)

