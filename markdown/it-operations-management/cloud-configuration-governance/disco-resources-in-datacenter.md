---
title: Discover all resources in a datacenter on-demand
description: At any time, you can run Discovery on a datacenter to update the CMDB.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Additional Cloud Provisioning and Governance setup on day 2, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Discover all resources in a datacenter on-demand

At any time, you can run Discovery on a datacenter to update the CMDB.

## Before you begin

-   A cloud account must exist with service accounts and associated datacenters. You must run on-demand Discovery to discover datacenters before you can schedule Discovery.
-   Use the Cloud Discovery Workspace, and at least version 1.15 of Discovery and Service Mapping Patterns from the ServiceNow Store.

Role required: sn\_cmp.cloud\_admin

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Cloud Accounts**.

2.  Click a cloud account and, on the **Datacenters** tab, select a datacenter.

    The **Resources** tab lists the resources in the CMDB.

    ![Resources in the selected datacenter](../image/rsrcs-in-ldc-on-cloud-acct-page.png)

3.  Change the state to **Draft** and then click **Discover Now**.

    Note that **Discover Now** is disabled if neither CAPI or Patterns is installed. Follow these scenarios to proceed.

    **Note:** **Discover now** will also be disabled with an message suggesting you to install the latest Discovery and Service Mapping Patterns. This can be fixed by installing version 1.15.1 at least or by triggering the manual migration step.

<table id="choicetable_hz2_yzr_bcc"><thead><tr><th align="left" id="d516640e144">

Scenario

</th><th align="left" id="d516640e147">

Next steps

</th></tr></thead><tbody><tr><td id="d516640e153">

**__Discover Now__ is disabled for System Admin login**

</td><td>

-   The page suggests that you must install the latest patterns application to proceed.
-   The banner at the top of the page prompts you to visit **Go to Applications Manager** for installation


</td></tr><tr><td id="d516640e176">

**__Discover Now__ is disabled for sn\_cmp Cloud Admin login**

</td><td>

-   The page suggests that you must install the latest patterns application to proceed.
-   The page requests to contact the system admin for installation of patterns application.


</td></tr><tr><td id="d516640e196">

**Latest patterns application is installed**

</td><td>

Discover Now is activated.**Note:** Discovery will now use Patterns as the default mechanism.

</td></tr></tbody>
</table>4.  Run **Discover Now** and wait for Discovery to finish.

5.  Change the state of the cloud account to **Published**.

    **Discover now** will be disabled with the same message shown. This can be fixed by installing 1.15.1+ version or by triggering the manual migration step


## Result

Discovery populates the CMDB with the discovered resources and updates the information on the **Resources** tab. You can view Discovery results in the **Discovery Log** tab.

**Note:** By default, Discovery stores the discovered VM hardware types in the Hardware Type \[cmdb\_ci\_compute\_template\] table. If you notice an unusually large number of records in this table, use the Cloud Hardware Type \[cmdb\_ci\_cloud\_hardware\_type\] table to store the discovered VM hardware types. For more information, see [Enable the Cloud Hardware Type class extension](../../discovery/task/enable-hardware-type-class-extension.md). All Cloud Provisioning and Governance features, such as provisioning, quotas, and so on continue to work as is after you switch to the Cloud Hardware Type table.

**Parent Topic:**[Additional Cloud Provisioning and Governance setup on day 2](../concept/cloud-mgt-general-setup-day-2.md)

**Related topics**  


[View the Discovery Log](../../discovery/reference/r_DiscoveryLog.md#)

