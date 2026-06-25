---
title: MID-less integrations for Health Log Analytics
description: Health Log Analytics \(HLA\) supports integrations that stream log data directly to your ServiceNow instance without a MID Server. Use these integrations to simplify your deployment and reduce infrastructure overhead.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-mid-less-integrations-concept.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-05-04"
reading_time_minutes: 4
keywords: [Health Log Analytics, HLA, OpenTelemetry, OTel, MID-less log streaming, integration, ITOM Gateway, JSON Web Token \(JWT\)]
breadcrumb: [Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# MID-less integrations for Health Log Analytics

Health Log Analytics \(HLA\) supports integrations that stream log data directly to your ServiceNow instance without a MID Server. Use these integrations to simplify your deployment and reduce infrastructure overhead.

## Role of the MID Server in Health Log Analytics

A Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs on a server in your network. In a standard HLA deployment, the MID Server acts as a relay between your log data sources and your ServiceNow instance. It collects, filters, and forwards log data on behalf of the instance.

While MID Servers provide flexibility and support a wide range of integrations, they introduce additional infrastructure to deploy, maintain, and monitor. Organizations with high log volumes may also have to scale MID Server capacity over time.

## How MID-less integrations work

MID-less integrations bypass the MID Server entirely. Log data streams from your third-party source directly to ServiceNow over HTTPS, where it is queued and processed by HLA.

This architecture relies on two components:

-   **ITOM Gateway**

    A lightweight, cloud-native component that receives incoming log data and routes it to your ServiceNow instance. You deploy ITOM Gateway based on your expected log volume. For more information, including deployment options and prerequisites, see [MID-less log streaming via ITOM Gateway in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming.md).

-   **JSON Web Token \(JWT\)**

    A secure, time-limited token used to authenticate the data stream between your log source and the ServiceNow datacenter. JWT authentication removes the requirement to store credentials such as AWS keys directly on your ServiceNow instance. For more information, see [Configure a JSON Web Token \(JWT\) provider and token for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-jwt-token-config.md).


## Supported MID-less integrations

The following integrations support MID-less log streaming to Health Log Analytics.

-   [AWS Firehose](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-firehose.md)
-   [Microsoft Azure Event Hubs \(MID-less\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-eventhubs-midless.md)

MID-less integrations using the OpenTelemetry \(OTLP\) protocol:

-   [Cribl Stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-cribl-stream.md)
-   [OpenTelemetry Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-otel-collector.md)
-   [Splunk OpenTelemetry Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-splunk-otel.md)

**Note:**

-   OTLP uses a standardized, vendor-neutral protocol to send application and system logs to HLA. It enables logs to be easily collected, processed, and correlated regardless of their origin or destination.
-   The MID-less OpenTelemetry integrations all use the same transport model and share a common setup procedure in the Integrations Launchpad.

## When to use MID-less integrations

Consider MID-less integrations when your organization wants to:

-   Reduce infrastructure by eliminating the requirement to deploy and maintain a MID Server
-   Simplify onboarding with a guided setup in the Integrations Launchpad
-   Stream log data from cloud-native sources, such as Amazon Data Firehose or Microsoft Azure Event Hubs, where a MID Server intermediary adds unnecessary complexity
-   Avoid storing third-party credentials on the ServiceNow instance

## Considerations

Before choosing a MID-less integration, review the following:

-   MID-less integrations require ITOM Gateway. You must set up and configure ITOM Gateway before activating any MID-less integration. For more information, see [MID-less log streaming via ITOM Gateway in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming.md).
-   If your deployment requires on-premises data collection, bidirectional communication, or integration types not yet supported in MID-less mode, a MID Server based integration may be more appropriate.

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-implement.md)

