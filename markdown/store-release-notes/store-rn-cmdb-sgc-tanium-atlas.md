---
title: Service Graph Connector for Tanium Atlas release notes
description: Version history for the ServiceNow Service Graph Connector for Tanium Atlas application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-cmdb-sgc-tanium-atlas.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# Service Graph Connector for Tanium Atlas release notes

Version history for the ServiceNow® Service Graph Connector for Tanium Atlas application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.0.0 - September 2026**
    -   The Service Graph Connector for Tanium Atlas automatically imports data from Tanium Atlas into the ServiceNow Configuration Management Database \(CMDB\), enabling service, operations, asset, and security management for all hardware or software items.  This easy-to-configure connection quickly begins collecting high-fidelity data, enriched with Tanium AI-driven context. Like all service graph connectors, the Tanium Atlas connector taps into the Identity and Reconciliation Engine \(IRE\) so that records aren't duplicated, and each data value is populated from its most trusted source.
    -   Unlike the Service Graph Connector for Tanium, this connector supports the new GraphQL API, so that ServiceNow connects with Tanium Atlas, the newest version of the platform, powered with an agentic AI layer. The new API allows the connector to perform delta \(incremental\) pulls for performance optimization and enables a variety of sensors and tags.
    -   The API that supports the Service Graph Connector for Tanium will eventually be deprecated, so you should plan to switch all downstream workflows to the new Service Graph Connector for Tanium Atlas \(or the Endpoints version\) at an appropriate time.
    -   The connector is easy to configure and can be managed at scale using SGC Central. It uses the dedicated workspace to transparently ingest, standardize, and integrate data from other connectors.

**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

