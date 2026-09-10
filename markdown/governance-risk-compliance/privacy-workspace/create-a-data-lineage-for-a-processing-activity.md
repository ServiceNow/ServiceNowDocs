---
title: Add relationships to a hierarchy for a processing activity
description: Define new relationships in a hierarchy directly on a processing activity to record how it connects to vendors, applications, systems, and other processing activities across regions. This enables you to track cross-border data transfers and generate a lineage map to visualize data consumption, sharing, and the associated risks for a processing activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/create-a-data-lineage-for-a-processing-activity.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Add relationships to a hierarchy for a processing activity

Define new relationships in a hierarchy directly on a processing activity to record how it connects to vendors, applications, systems, and other processing activities across regions. This enables you to track cross-border data transfers and generate a lineage map to visualize data consumption, sharing, and the associated risks for a processing activity.

## Before you begin

The processing activity must be in Discover state or later. If the processing activity is in New state, move it to Discover before proceeding.

Role required: Privacy analyst, Privacy manager

## About this task

Each processing activity involves multiple information objects classified as personal information. These objects exchange data with various other entities, making it essential to establish a hierarchy that describes how those entities interact and track where personal data is shared. Privacy Management then uses the relationships in a hierarchy to generate a data lineage map that visualizes how data moves across the processing activity. This helps mitigate privacy-related risks.

Adding hierarchy relationships is a two-step flow. In the first step you define the relationship, and in the second step you provide the relationship details.

A business user can also define such relationships as part of a privacy assessment. For details, see [Respond to privacy impact assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/respond-to-a-privacy-smart-assessment.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace**.

2.  Select the List icon \[Omitted image "ListsIcon.jpg"\] Alt text:.

3.  In the **Lists** tab, select **Processing activities** &gt; **All processing activities**.

4.  Open a processing activity that is in the Discover state.

5.  Create new relationships in one the following ways.

<table id="choicetable_y5d_d1q_hkc"><thead><tr><th align="left" id="d292288e138">

Choice

</th><th align="left" id="d292288e141">

Path

</th></tr></thead><tbody><tr><td id="d292288e147">

**From Hierarchy tab**

</td><td>

1.  Navigate to **Processing data inventory** &gt; **Hierarchy**.
2.  Select **Add**.


</td></tr><tr><td id="d292288e177">

**From Data lineage map**

</td><td>

1.  Select **View lineage map**.
2.  Select the **Primary record** card.
3.  In the record panel, select **Add relationship**.


</td></tr></tbody>
</table>    The New relationship dialog box opens to the **Define relationships** step.

6.  In the Define relationships form, fill in the fields.

    For detailed description of the fields, see [Define relationships form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/new-relationship-forms.md).

7.  Select **Next**.

8.  For each Related node in the Relationship details form, fill in the fields.

    For detailed description of the fields, see [Relationship details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/new-relationship-forms.md).

9.  To automatically apply the same relationship details to every related node, select **Copy details to all**.

10. Select **Add**.


## Result

The new relationship appears in the **Hierarchy** tab list. Select **View lineage map** for a graphical view of the new relationships added to the hierarchy. If a related node is itself a processing activity with existing relationships, those connections also appear in the map.

If the hierarchy relationship involves sending or receiving personal data from one node to another, data transfer records are generated to capture each movement. For more information, see [Manage data transfers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/data-transfers.md).

## What to do next

Manage the relationships from the **Processing data inventory** &gt; **Hierarchy** tab of the processing activity.

-   To edit a relationship, select the record, and select **Edit**.
-   To delete a relationship, select the record, and select **Remove**.

-   **[New hierarchy relationship forms in Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/new-relationship-forms.md)**  
When creating a new hierarchy relationship in Privacy Management, you first define how a node is related to another. Then, you provide details for each related node.

**Parent Topic:**[Using Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/using-privacy-mgmt.md)

