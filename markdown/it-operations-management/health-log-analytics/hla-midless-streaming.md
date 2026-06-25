---
title: MID-less log streaming via ITOM Gateway in Health Log Analytics
description: Health Log Analytics \(HLA\) can receive log data from external sources directly through the ITOM Gateway, without routing data through a MID Server. This architecture supports cloud-native log sources such as Amazon Data Firehose, Cribl, and OpenTelemetry, and is required for high-volume HLA deployments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-midless-streaming.html
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-05-04"
reading_time_minutes: 3
keywords: [MID-less log streaming, configuration, ITOM Gateway, gRPC, Hermes Messaging Service, log source streaming, HLA infrastructure scaling, AI Engine, JWT provider token]
breadcrumb: [MID-less integrations, Set up integrations from Integrations Launchpad, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# MID-less log streaming via ITOM Gateway in Health Log Analytics

Health Log Analytics \(HLA\) can receive log data from external sources directly through the ITOM Gateway, without routing data through a MID Server. This architecture supports cloud-native log sources such as Amazon Data Firehose, Cribl, and OpenTelemetry, and is required for high-volume HLA deployments.

## How log streaming via ITOM Gateway works

External log sources send data to the ITOM Gateway over gRPC. The ITOM Gateway forwards the data to the  Hermes  Messaging Service, which delivers it to the AI Engine, the HLA processing back-end. This design separates log streaming from ingestion, enabling higher throughput than direct MID Server streaming.

## Deployment scenarios

The setup path depends on your expected log volume.

<table id="table_vsg_4xy_djc"><thead><tr><th>

Deployment type

</th><th>

Setup

</th></tr></thead><tbody><tr><td>

Standard

</td><td>

For typical log volumes, enable ITOM Gateway and the  Hermes  Messaging Service on your instance, configure a JSON Web Token \(JWT\) provider and token, and set up your log source from Integrations Launchpad. For more information, see [Configure a JSON Web Token \(JWT\) provider and token for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-jwt-token-config.md) and [Set up log streaming via ITOM Gateway for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming-setup.md).

</td></tr><tr><td>

High-volume

</td><td>

For deployments requiring 30,000 or more log events per second, you must scale the HLA infrastructure before enabling ITOM Gateway. This process involves resizing the AI Engine and Elasticsearch nodes and coordinating a cross-team migration.Contact ServiceNow Support to request infrastructure scaling. For details and the required information to provide, see [Set up log streaming via ITOM Gateway for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming-setup.md)

**Note:** Infrastructure scaling requires a 6-hour change window and involves expected downtime of 2–6 hours for HLA functions only.

</td></tr></tbody>
</table>## Supported log sources

Currently, the following log sources can stream data to HLA via ITOM Gateway:

-   [AWS Firehose](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/il-connector-hla-firehose.md)
-   Cribl Stream
-   OpenTelemetry Collector

Each source has a dedicated tile in Integrations Launchpad for configuration.

## Authentication

Log sources authenticate to HLA using a JWT token. You must configure a JWT provider and generate a token on the ServiceNow instance before activating an ITOM Gateway integration.

## Key components

|Component|Description|
|---------|-----------|
|ITOM Gateway|Receives incoming log data from external sources over gRPC and forwards it to the  Hermes  Messaging Service.|
|Hermes  Messaging Service|Message broker that routes data from ITOM Gateway to the HLA back-end.|
|AI Engine|HLA back-end component that processes and analyzes ingested log data.|
|Integrations Launchpad|ServiceNow interface for configuring log source integrations. Each supported log source has a dedicated tile.|

**Parent Topic:**[Set up Health Log Analytics on your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-implement.md)

**Related topics**  


[Configure a JSON Web Token \(JWT\) provider and token for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-jwt-token-config.md)

[Set up log streaming via ITOM Gateway for Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-midless-streaming-setup.md)

