---
title: Metadata collector deployment models
description: Choose how to deploy metadata collectors based on your network accessibility and security needs. Deploy on a MID Server you host, or use ServiceNow-managed cloud infrastructure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/metadata-collector-deployment-models.html
release: australia
topic_type: concept
last_updated: "2026-08-19"
reading_time_minutes: 2
keywords: [metadata collectors, deployment models, MID Server, cloud collectors, on-premises]
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Metadata collector deployment models

Choose how to deploy metadata collectors based on your network accessibility and security needs. Deploy on a MID Server you host, or use ServiceNow-managed cloud infrastructure.

Metadata collectors harvest metadata — schemas, tables, columns, and lineage — from your data sources and upload it to your ServiceNow instance for cataloging and governance. You can deploy collectors in two ways: on a MID Server within your network, or in ServiceNow-managed cloud infrastructure. The choice depends on your source's network accessibility and whether you want to manage your own infrastructure.

## Deployment model selection

Select a deployment model using the toggle on the metadata collector setup screen: **Use MID Server**.

-   **Toggle on:** The collector connects to the source system through a MID Server. The system automatically selects an available MID Server.
-   **Toggle off:** The collector connects to the source system without requiring a MID Server. \[Omitted image "dc-metadata-collector-mid-server.png"\] Alt text: Select deployment model

## MID Server collectors \(on-premises\)

The collector runs as a job on a MID Server you host, inside your network. The MID Server reaches the source directly, then pushes the harvested metadata back to your ServiceNow instance over the existing MID Server connection.

For system requirements and configuration guidelines, see [MID Server for metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/mid-server-for-metadata-collectors-dc.md).

## ServiceNow-hosted collectors \(cloud\)

The collector runs in ServiceNow-managed infrastructure. There is no host to provision or patch on your side. You register the connection and credentials, and ServiceNow runs the collector job.

Use this option if you do not want to provision or maintain a MID Server just for cataloging.

Requirements:

-   Source system reachable from ServiceNow's cloud through direct internet access.
-   Service account credentials with read access to the source's metadata APIs or system catalogs
-   No local infrastructure to size or maintain

## Deployment model comparison

|Consideration|MID Server \(on-premises\)|ServiceNow-hosted \(cloud\)|
|-------------|--------------------------|---------------------------|
|Who runs the process|You, on your infrastructure|ServiceNow|
|Network exposure needed|None inbound; MID Server reaches out|Source must be reachable from ServiceNow's cloud|
|Best for|Sources behind a firewall or VPN, strict data residency requirements|Internet-reachable or cloud-native sources, no appetite for hosting infrastructure|
|Ongoing maintenance|You patch and size the MID Server|None|

## What gets harvested

The deployment model doesn't change what's cataloged. Either way, the collector harvests schemas, tables, columns, and lineage from the source, then uploads them to the ServiceNow instance for cataloging, governance, and AI-ready workflows.

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-metadata-collectors-dc.md)

