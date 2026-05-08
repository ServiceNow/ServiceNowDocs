---
title: Create table cleanup jobs for Service Graph Connector for Infoblox
description: Create table cleanup jobs to automate the cleanup of retired CIs from Service Graph Connector for Infoblox version 1.4.0 and earlier based on your organization's data retention requirements and integration dependencies.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Infoblox, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create table cleanup jobs for Service Graph Connector for Infoblox

Create table cleanup jobs to automate the cleanup of retired CIs from Service Graph Connector for Infoblox version 1.4.0 and earlier based on your organization's data retention requirements and integration dependencies.

## Before you begin

**Note:** Creating table cleanup jobs for deleting outdated data is an optional procedure.

Dependencies and requirements:

-   Upgrade to Service Graph Connector for Infoblox version 1.5.0.
-   Verify that the initial full data load is complete after upgrading to Service Graph Connector for Infoblox version 1.5.0.
-   Verify that active integrations do not use any of the old data and that the retired CIs can be safely deleted.

Role required: admin

## Procedure

1.  Set the application scope to **CMDB CI Class Models** by using the application picker.

    The IPAM tables \(Managed Network, IP Pool, Subnet, and Allocated IP Address\) belong to the CMDB CI Class Models scope. For more information, see Application picker.

2.  Navigate to **All** &gt; **System Maintenance** &gt; **Table Cleanup**.

3.  Select **New** to create a new table cleanup job.

4.  Configure a table cleanup job for the IPAM tables.

<table id="table_bc4_ntb_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table name

</td><td>

Enter the name of the IPAM table from which outdated data is to be cleaned up.You can create table cleanup jobs for the following IPAM tables:

-   cmdb\_ci\_managed\_network
-   cmdb\_ci\_ip\_pool
-   cmdb\_ci\_ip\_network\_subnet
-   cmdb\_ci\_allocated\_ip\_address


</td></tr><tr><td>

Age in seconds

</td><td>

Set the value to either `0` or `86400` \(24 hours\).-   `0`: All records updated from now are deleted \(immediate cleanup\).
-   `86400`: Records older than 24 hours are cleaned up \(recommended\).
**Note:** Setting this value to less than 24 hours \(86400 seconds\) could result in missing session statistics data.

</td></tr></tbody>
</table>5.  Add filters for the table cleanup job.

    1.  Select **Discovery source** is **SG-Infoblox**.

    2.  Select **AND**.

    3.  Select **Operational status** is **retired**.

    **Important:** Incorrect configuration of these filters might delete operational CIs or CIs from other discovery sources.

6.  Select **Submit**.

    The job runs automatically in the next available maintenance window.

7.  Repeat step [4](sgc-infoblox-create-table-cleanup-jobs.md#step_kts_bvb_m3c) to step [6](sgc-infoblox-create-table-cleanup-jobs.md#step_lhc_dvb_m3c) for the remaining IPAM tables.

8.  Configure a table cleanup job for the Detailed Network \[sn\_infoblox\_integ\_sg\_infoblox\_detailed\_subnetwork\] table.

    1.  Switch the application scope to **Service Graph Connector for Infoblox** by using the application picker.

    2.  Navigate to **All** &gt; **System Maintenance** &gt; **Table Cleanup**.

    3.  Select **New**.

    4.  Configure a table cleanup job for the Detailed Network \[sn\_infoblox\_integ\_sg\_infoblox\_detailed\_subnetwork\] table.

<table id="table_xnv_rvb_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table name

</td><td>

Enter `sn_infoblox_integ_sg_infoblox_detailed_subnetwork` as the table name.

</td></tr><tr><td>

Age in seconds

</td><td>

Set the value to either `0` or `86400` \(24 hours\).-   `0`: All records updated from now are deleted \(immediate cleanup\).
-   `86400`: Records older than 24 hours are cleaned up \(recommended\).
**Note:** Setting this value to less than 24 hours \(86400 seconds\) could result in missing session statistics data.

</td></tr></tbody>
</table>    5.  Select **Operational status** is **retired**.

        **Important:** Incorrect configuration of this filter might delete operational CIs or CIs from other discovery sources.

    6.  Select **Submit**.


