---
title: Create an SLA definition for a CI or application service
description: You can create SLA definitions for CIs and application services just as you can for other task records in the instance.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SLAs for application services and CIs, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create an SLA definition for a CI or application service

You can create SLA definitions for CIs and application services just as you can for other task records in the instance.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **SLA** &gt; **SLA Definitions**.

2.  Click **New**.

3.  Fill out the fields on the SLA Definition form.

    For a description of each field, see [Create an SLA definition for a CI or application service](t_EMCreateSLADefForCI_BS.md).

4.  For the **Table** field, select **Event Management SLA \[em\_ci\_severity\_task\]**.

5.  Configure the **Start condition** filter by adding conditions, such as:

<table id="table_rmj_xpg_y5"><tbody><tr><td colspan="3">

For all CIs where the **Severity** is **Critical**

</td></tr><tr><td>

**Type**

</td><td>

**is**

</td><td>

**CI** **Note:** Event Management SLAs work only on CI classes from Service Instance \[cmdb\_ci\_service\_auto\].

</td></tr><tr><td>

**Severity**

</td><td>

**is**

</td><td>

**Critical**

</td></tr><tr><td colspan="3">

For a specific service, such as Email, when the **Severity** is **Critical**

</td></tr><tr><td>

**Application Service**

</td><td>

**is**

</td><td>

**Email**

</td></tr><tr><td>

**Severity**

</td><td>

**is**

</td><td>

**Critical**

</td></tr></tbody>
</table>6.  Configure pause, stop and reset conditions.

7.  Click **Submit**.


**Parent Topic:**[SLAs for application services and CIs](../concept/c_EMSLAsForBSAndCIs.md)

