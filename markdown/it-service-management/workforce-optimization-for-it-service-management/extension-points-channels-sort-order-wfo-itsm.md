---
title: Channel Management extension point in Workforce Optimization for ITSM
description: Use extension points to call scripts to configure the list sort order in Channel Management.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Channels, Channels, Workforce Optimization for ITSM, IT Service Management]
---

# Channel Management extension point in Workforce Optimization for ITSM

Use extension points to call scripts to configure the list sort order in Channel Management.

To see a list of extension points that you can use for Workforce Optimization for ITSM, navigate to **System Extension Points** &gt; **Scripted Extension Points**. Use scripted extension points to integrate customizations without altering the core components in the application code. When customizing a base application, you implement the scripted extension points by creating the custom script includes and registering them against the scripted extension points. For detailed information on implementing extension points, see [Using scripted extension points in server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/scripted-extension-points.md).

<table id="table_lm4_cr2_wwb"><thead><tr><th>

Extension script

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_channel\_mgmt.ChannelMgmtExtensionPoint**

</td><td>

Add or modify the columns and sort directions in the `vardata` section to configure the sorting mechanism for the All Agents and All Queues lists in Channel Management. As an example, The Presence State column with **ASC** as a sort direction in the extension script displays the Presence State records in an ascending order in the All Agents list.

**Note:** You can create multiple implementations; however, the implementation with the lowest order number is executed.

</td></tr><tr><td>

**sn\_channel\_mgmt.AgentListColumns**

</td><td>

Add or update the `getColumns` to modify the current implementation to configure the columns for the All agents list in Channel Management.

</td></tr><tr><td>

**sn\_channel\_mgmt.QueueListColumns**

</td><td>

Add or update the `getColumns` to configure the columns in the All queues list for Channel Management.

</td></tr></tbody>
</table>**Parent Topic:**[Setting up Channels in Workforce Optimization for ITSM](../concept/setup-channels-configurable-workforce-optimization-itsm.md)

