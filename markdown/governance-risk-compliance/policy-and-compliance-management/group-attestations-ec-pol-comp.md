---
title: Group assessments for similar assessments in Employee Center
description: Group the assessments that have the same entity or control objective based on metric type, and additionally the same entity, control objective, or category to provide response to similar assessments.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage GRC tasks from Employee Center, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Group assessments for similar assessments in Employee Center

Group the assessments that have the same entity or control objective based on metric type, and additionally the same entity, control objective, or category to provide response to similar assessments.

## Before you begin

Role required: sn\_grc.business\_user, sn\_grc.business\_user\_lite

## About this task

In Configurable Workspace, you can only group control attestations, and not risk assessments, vendor assessments, or privacy assessments. Such assessments and those assessments that can't be grouped by the selected **Group by** criterion are marked as invalid and are displayed in the **Group previews** of the Group assessment pop-up, with a link to view such assessments.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  Select **GRC tasks** in the **My active items** pane of the Home page.

3.  Select the Tasks ![Tasks icon.](../../grc-workspace-audit/image/TasksIcon.jpg) icon on the left pane.

4.  Select the attestation records in the list view of the Tasks page that you'd like to group.

    **Note:** You must select at least two and can select up to a maximum of 13 assessment records for grouping.

5.  Select the **Group assessments** button.

6.  Select a **Response type** in the Group assessments pop-up.

    For more information on the response types, see [Consolidate control attestations using the Same Response feature](../concept/c_Attestations.md#).

7.  Select a criterion to group the assessments in the **Group by** list.

    By default, assessments are grouped by the metric type template. You can group the assessments by Category, Entity, or Control objective. If the selected assessments have a common category, entity, or control objective then they're grouped accordingly based on your selection. However, if the assessments selected do t have any of the common criteria by which they can be grouped, then the assessments are not grouped at all.

    The **Group previews** section displays the grouping details, assessments with links, and an appropriate message information if they're grouped or can't be grouped based on the Group by criterion, status, assignee, or the evaluation method of the metric type.

    ![Grouping assessments based on category.](../image/group-attestation-ec-pc.png)

    ![Information message displaying that the assessments cannot be grouped based on control objective, as they are not the same for all the selected assessments.](../image/group-attest-ec-pc.png)

8.  Select the **Group** button.

    If the grouping of assessments is successful, then you get a message indicating that the assessment group has been created, followed by a link to the grouped assessments.

    If a few of the assessments among the selected assessments couldn’t be grouped by the selected criterion, then the **Group previews** pane displays the number of assessments that couldn’t be grouped. Nevertheless, as there are other assessments in your selection that could be grouped by the selected **Group by** criterion, the **Group** button is active for you to select and group the rest, where the grouping is successful.

    On the other hand, if all the assessments that you selected are invalid, for example, risk assessments or privacy assessments, then the **Group** button is inactive as grouping isn't possible for such assessments.

    ![UI message with link to the grouped assessments.](../image/group-assess-ui-message.png)

    **Note:** You can group the assessments that are in **Ready to take** or **In Progress** state, but not the assessments that are in **Complete** or **Canceled** state.

    If the status of a record that you’ve selected for grouping has changed and is being assessed before you select the **Group** button to group the assessments, then such a record can't be grouped.

    ![Error message indicating the assessments could not be grouped.](../image/group-assess-no-grouping-ui.png)

9.  Select the link to the grouped assessment in the UI message.

    The link takes you to the list view of the grouped assessments. Alternatively, you can also select the **Grouped attestations** on the left pane. The Assessment Instance page opens up, where you can take the assessment.


