---
title: Create a connection Alias for third-party provider
description: Create a connection Alias for your third-party provider to enable external routing on your instance.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [External routing overview, Work item queues, Work items, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a connection Alias for third-party provider

Create a connection Alias for your third-party provider to enable external routing on your instance.

## Before you begin

Role required: admin

-   Plugins to be installed:
    -   Advanced Work Assignment plugin \(com.glide.awa\)
    -   External Routing Support plugin \(com.glide.awa-external\)

        **Note:** Load the demo data while installing the plugin.

-   Role required: admin

## Procedure

1.  On your ServiceNow instance, navigate to **Connection and Credential Aliases** and select the required type of connection record.

    For example, **ServiceNow\_Basic** record.

2.  Create a connection from the **Connections** tab.

    1.  Set up Credentials for the Connection record.

    -   In the Credentials record, provide the **Name**, **User name**, and **Password**.
    -   Select **Submit** and select that credential.
    -   For the Connection URL, provide an active URL \(of any third-party provider\).
    -   Select **Save**.

**Parent Topic:**[External routing overview](../concept/awa-external-routing-overview.md)

