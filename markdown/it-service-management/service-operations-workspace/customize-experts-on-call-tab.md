---
title: Configure the experts On-call panel for an incident
description: Configure the Experts on-call panel for an incident.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring record pages in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM to improve your experience, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the experts On-call panel for an incident

Configure the **Experts on-call** panel for an incident.

## Before you begin

Role required: admin

To configure the Experts On-call panel, ensure that you have added an implementation for the **sn\_sow\_on\_call.ExpertsOnCallTabConfig** extension point.

**Note:**

-   Incident table extension point implementation is added by default. To customize it, edit the script to include **ExpertsOnCallTabConfigForIncident**.
-   Example: If you want to display only the assignment group in the Experts On-call panel, then update the **getRecommendedFieldWatchList** in the script.

## About this task

To add Experts On-call for Problem table, follow the steps:

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Select and open the **sn\_sow\_on\_call.ExpertsOnCallTabConfig** extension point.

3.  Select **Create implementation** from the related links section.

4.  Modify the **Script** as required:

<table id="table_sqq_cwx_dcc"><thead><tr><th>

Method

</th><th>

Inputs

</th><th>

Return

</th></tr></thead><tbody><tr><td>

**getTableName**

</td><td>

None

</td><td>

String – Table name for which an extension point is implemented

</td></tr><tr><td>

**getRecommendedFieldWatchList**

</td><td>

None

</td><td>

Array – List of fields that you want to show on the Experts On-call recommended groups panel.For example: **\[“assignment\_group”, “cmdb\_ci”\]**

</td></tr><tr><td>

**getRecommendedGroups**

</td><td>

-   recordGr – GlideRecord reference
-   fieldWatchList – Object containing all the fields and their respective values.
 For example: **\{ "assignment\_group": &lt;assignment\_group\_sys\_id&gt; \}**

</td><td>

Array – List of objects containing recommended group, sys\_id, and the respective message.For example: **\[ \{ : "Recommended based on assignment group" \} \]**

</td></tr><tr><td>

**isExpertOnCallTabSupported**

</td><td>

None

</td><td>

Boolean – return true to enable the Expert On-call for this table.

</td></tr></tbody>
</table>5.  Select **Update**.


**Parent Topic:**[Configuring record pages in Service Operations Workspace for ITSM](../concept/configuring-record-pages-sow-itsm.md)

