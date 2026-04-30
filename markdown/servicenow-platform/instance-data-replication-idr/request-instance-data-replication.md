---
title: Request an Instance Data Replication subscription
description: The Instance Data Replication \(IDR\) plugin requires a separate subscription and must be activated by ServiceNow personnel.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Request an Instance Data Replication subscription

The Instance Data Replication \(IDR\) plugin requires a separate subscription and must be activated by ServiceNow personnel.

## Before you begin

Role required: admin

## About this task

Beginning with the New York release, IDR is supported. The IDR plugin ID is com.glide.idr. When purchasing an IDR subscription, ServiceNow, Inc. personnel also activate the following plugins that IDR depends upon:

-   com.snc.db.data\_replicate
-   com.glide.transform
-   com.glide.kmf

IDR runs in ServiceNow data centers only, which means there is no support for using IDR with on-premise instances.

To purchase a subscription, contact your ServiceNow account manager. The account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

    ![Admin view of the Application Manager interface with the Request plugin option highlighted.](../../../reuse/images/request-plugin.png)

3.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Select the name of the plugin to activate.

 **Note:** If the system doesn't list the plugin you want or if you're activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

    ![Admin view of the form requesting the Event Management plugin on a selected instance. For the text description, refer to the Activate Plugin form table.](../../../reuse/images/activate-plugin-form.png "Completed Activate Plugin form")

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


## What to do next

Plan your replication strategy. See [Preparing for Instance Data Replication](../concept/prepare-instance-data-replication.md).

**Parent Topic:**[Configuring Instance Data Replication](../concept/configuring-instance-data-replication.md)

**Related topics**  


[Preparing for Instance Data Replication](../concept/prepare-instance-data-replication.md)

[Preserving table hierarchy in Instance Data Replication](../concept/preserving-table-hierarchy.md)

[Upgrading legacy replication sets to V2 in Instance Data Replication](../concept/upgrading-legacy-replication-sets-v2.md)

[Upgrading your instance with Instance Data Replication enabled](../concept/upgrading-instance-with-idr.md)

[List of plugins \(Yokohama\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

