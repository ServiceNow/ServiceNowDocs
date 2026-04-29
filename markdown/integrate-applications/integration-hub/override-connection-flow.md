---
title: Override a connection in a flow
description: Override a connection for a flow, subflow, or action.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Supporting multiple connections, Manage connections, Integration Hub, Workflow Data Fabric]
---

# Override a connection in a flow

Override a connection for a flow, subflow, or action.

## Before you begin

For details about flow overrides, including how they affect actions with dynamic inputs and how multiple overrides are applied, see [Supporting multiple connections](../concept/support-multiple-connections.md).

Role required: flow\_designer or admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the flow or subflow that has the connection you want to modify.

3.  Click the More actions icon \(![More actions icon](../images/more-actions-menu-icon.png)\), and select **Configure connections**.

4.  In the Configure Connections window, identify the alias associated with the connection that you want to override and select a new connection from the list.

5.  Click **Update**.

    **Note:** If the option is enabled, you can also override a connection at the action level. Click **Advanced Options** below the action. Choose the new connection from the list, then click **Done**. This option is only available if the action has an overridable connection.


## What to do next

Test the flow.

