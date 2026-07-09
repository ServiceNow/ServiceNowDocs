---
title: Reverse Tunnel Relay release notes
description: Version history for the ServiceNow Reverse Tunnel Relay application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-wdf-rn-reverse-tunnel-relay.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Workflow Data Fabric release notes, ServiceNow Store release notes]
---

# Reverse Tunnel Relay release notes

Version history for the ServiceNow® Reverse Tunnel Relay application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version - July 2026**
    -   Relay enables private, outbound-only connectivity between the customer's VPC and the ServiceNow platform, requiring no inbound firewall changes or exposed ports.
        -   A lightweight relay agent deployed within the customer's VPC initiates all outbound connectivity &amp;mdash; no inbound firewall rule changes needed.
        -   ServiceNow Gateway acts as the secure tunnel endpoint, routing data requests between the platform and the customer's private network with zero exposed ports.
        -   Once connected, Zero Copy Connectors \(ZCC\) can query on-premises data sources within the Workflow Data Fabric.
-   **Version 1.2.0 - June 2026**

    Relay is a lightweight agent deployed within the customer's VPC that initiates an outbound connection to ServiceNow Gateway, establishing a secure private connectivity tunnel to the ServiceNow platform.


**Parent Topic:**[ServiceNow Store - Workflow Data Fabric release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-workflow-data-fabric-highlights.md)

