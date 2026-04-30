---
title: Request Zero Copy Connectors
description: Create zero copy connections and data fabric tables in Workflow Data Fabric Hub after requesting the Zero Copy Connectors app through the Now Support Service Catalog. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:If it isn't already installed, the app installs Workflow Data Fabric Hub.
locale: en-US
release: zurich
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Workflow Data Fabric Hub, Workflow Data Fabric]
---

# Request Zero Copy Connectors

Create zero copy connections and data fabric tables in Workflow Data Fabric Hub after requesting the Zero Copy Connectors app through the Now Support Service Catalog. If it isn't already installed, the app installs Workflow Data Fabric Hub.

## Before you begin

The Zero Copy Connectors app requires a separate subscription and must be activated by ServiceNow personnel.

To purchase a subscription, contact your ServiceNow account manager. The account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

**Important:** The Zero Copy Connectors app is only supported on production and non-production instances. The Zero Copy Connectors app is not supported on demo instances.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

3.  On the form, fill in the fields.

<table id="table_xhg_525_dfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Plugin Name

</td><td>

Enter: `Zero Copy Connectors (sn_data_fabric_zcc)`

</td></tr><tr><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


**Parent Topic:**[Configuring Workflow Data Fabric Hub](../concept/configuring-wdf.md)

