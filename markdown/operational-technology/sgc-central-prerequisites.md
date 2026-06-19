---
title: SGC Central prerequisites
description: Get started with SGC Central and set up the prerequisites for the Service Graph Connector for ServiceNow OT Discovery
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/sgc-central-prerequisites.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-05-19"
reading_time_minutes: 1
breadcrumb: [SGC Central, Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# SGC Central prerequisites

Get started with SGC Central and set up the prerequisites for the Service Graph Connector for ServiceNow OT Discovery

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the **All** menu and type in search field **service graph connector**.

    You can also access SGC Central by navigating to the CMDB Workspace.

2.  In the results, under ServiceNow OT Discovery, the **Setup Using SGC Central** option displays.

    \[Omitted image "result-drop-down-2.png"\] Alt text: Setup Using SGC Central

3.  Select the **SGC Central** tab.

4.  There are two prerequisites you much complete before you can create connections for the Service Graph Connector for ServiceNow OT Discovery:

5.  The first prerequisite is download and install the OT Discovery components.

    \[Omitted image "downloadpage2-sgcc.png"\] Alt text: OT Discovery Downloads

    1.  Download and install the Discovery Console for OT package.
    2.  Download and install the Discovery Sensor for OT package \(ISO and OVR\).
    3.  Download and install the OT Discovery Collector package that's compatible with your OS.
    **Note:** If you want to download and install the Console and Collector containerized packages, see [Air-gapped networks and OT Discovery installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/air-gapped-networks-installation.md) for more information.

6.  The second prerequisite is to configure the MID Server.

    Configure the MID Server using the MID Server Guided Setup. Select the link to review the MID Server certificate check policies.

    \[Omitted image "sgcc-configure-mid-server2.png"\] Alt text: Configure the MID Server

7.  Verify that the prerequisites are complete and select **Continue**.


