---
title: Create SLA breakdown definitions
description: You can define an SLA breakdown to capture, store, and relay detailed task ownership information and duration for all task SLA records related to a specific task \(incident\). SLA breakdown is configurable and you can configure it on the basis of a specific SLA definition.
locale: en-US
release: australia
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Service Level Management, Service Level Management, IT Service Management]
---

# Create SLA breakdown definitions

You can define an SLA breakdown to capture, store, and relay detailed task ownership information and duration for all task SLA records related to a specific task \(incident\). SLA breakdown is configurable and you can configure it on the basis of a specific SLA definition.

## Before you begin

Role required: admin

## About this task

SLA breakdown data includes:

-   Task SLA
-   SLA Definition
-   Assigned to
-   Assignment Group
-   Start time
-   End time
-   Business time during this period
-   Total % of allocated SLA Duration
-   Whether the Task SLA is breached during this period

**Note:** SLA breakdown is on a per task-type basis. For example, once you define a breakdown definition for Incident that uses the breakdown table \[SLA Breakdown by Assignment\], you cannot define another breakdown definition for this task type.

![sla breakdown by assignment](../image/sla-breakdown-by-assignment.png "SLA breakdown by assignment")

## Procedure

1.  Navigate to **All** &gt; **Service Level Management** &gt; **Breakdowns** &gt; **Breakdown definitions**, and click **New**.

2.  On the form, fill in the fields.

<table id="table_jsh_knd_ndb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the SLA breakdown.

</td></tr><tr><td>

Task table

</td><td>

Task table on which the definition is applicable.

</td></tr><tr><td>

SLA breakdown table

</td><td>

Table where the SLA breakdown data is stored.**Note:** For the Madrid release, only a single breakdown table is available: \[SLA Breakdown by Assignment\].

</td></tr><tr><td>

Active

</td><td>

Check box to select if the SLA breakdown definition is active.

</td></tr></tbody>
</table>3.  Click **Submit**.

    The SLA Breakdown Definition Fields and the SLA Definitions related lists appear.

4.  Under the **SLA Breakdown Definition Fields** tab, click **New** and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Breakdown field name|Field in the breakdown table that is mapped with the field that you select in the source field.|
    |Source field name|Field in the task record table which is mapped to the breakdown field.|

5.  Click **Submit**.

    The breakdown field and the associated source field appears under the **SLA Breakdown Definitions Field** tab.

6.  Under the **SLA Definitions** tab, click **Edit** to relate one or more SLA definitions to the breakdown definition.

7.  In the slush bucket, under Collection, select SLA Definitions to related to SLA Breakdown Definition.

    The breakdown is applied on this task record.

8.  Click **Save**.

    The selected SLA Definitions appear.


**Parent Topic:**[Configuring Service Level Management](../concept/configuring-service-level-management.md)

