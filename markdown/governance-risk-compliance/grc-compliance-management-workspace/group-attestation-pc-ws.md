---
title: Group assessments for similar assessments in the Tasks page
description: Provide response to similar assessments by grouping the assessments based on metric type, and additionally the same entity, control objective, or category in the Tasks page of the Compliance Workspace.
locale: en-US
release: zurich
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage controls, Use, GRC Compliance Workspace, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Group assessments for similar assessments in the Tasks page

Provide response to similar assessments by grouping the assessments based on metric type, and additionally the same entity, control objective, or category in the Tasks page of the Compliance Workspace.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_manager or sn\_compliance\_ws.corporate\_compliance\_analyst

## About this task

In Configurable Workspace, you can only group control attestations, and not risk assessments, vendor assessments, or privacy assessments. Such assessments and those assessments that can’t be grouped by the selected **Group by** criterion are marked as invalid and are displayed in the **Group previews** of the Group assessment pop-up, with a link to view such assessments.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  Select the Tasks ![Tasks icon](../../grc-workspace-audit/image/TasksIcon.jpg) icon on the left pane.

3.  Select the attestation records in the My pending tasks tab that you'd like to group.

    **Note:** You must select at least two and can select up to a maximum of 13 assessment records for grouping.

4.  Select the **Group assessments** button.

5.  Select a **Response type** in the Group assessments pop-up.

    For more information on the response types, see [Group attestations using Same Response](../../grc-policy-and-compliance/concept/c_Attestations.md#).

6.  Select a criterion to group the assessments in the **Group by** list.

    By default, assessments are grouped by the metric type template. You can group the assessments by Category, Entity, or Control objective. If the selected assessments have a common category, entity, or control objective then they're grouped accordingly based on your selection. However, if the assessments selected don't have any of the common criteria by which they can be grouped, then the assessments aren’t grouped.

    The **Group previews** section displays the grouping details, assessments with links, and an appropriate message information if they’re grouped or cannot be grouped based on the Group by criterion, status, assignee, or the evaluation method of the metric type.

    ![Grouping assessments based on category.](../../grc-policy-and-compliance/image/group-attestation-ec-pc.png)

    ![Information message displaying that the assessments cannot be grouped based on reasons displayed in the Group previews.](../../grc-policy-and-compliance/image/group-attest-ec-pc.png)

7.  Select the **Group** button.

    If the grouping of assessments is successful, then you get a message indicating that the assessment group has been created, followed by a link to the grouped assessments.

    If a few of the assessments among the selected assessments couldn’t be grouped by the selected criterion, then the **Group previews** displays the number of assessments that couldn’t be grouped. Nevertheless, as there are other assessments in your selection that could be grouped by the selected **Group by** criterion, the **Group** button is active for you to select and group the rest, where the grouping is successful.

    On the other hand, if all the assessments that you selected are invalid, for example, risk assessments or privacy assessments, then the **Group** button is inactive as grouping isn’t possible for such assessments.

    ![UI message with link to the grouped assessments.](../../grc-policy-and-compliance/image/group-assess-ui-message.png)

    **Note:** You can group the assessments that are in **Ready to take** or **In progress** state, but not the assessments that are in **Complete** or **Canceled** state.

    If the status of a record that you’ve selected for grouping has changed and is being assessed before you select the **Group** button to group the assessments, then such a record can’t be grouped.

    ![Error message indicating the assessments could not be grouped.](../../grc-policy-and-compliance/image/group-assess-no-grouping-ui.png)

8.  Select the link to the grouped assessment in the UI message.

    The link takes you to the list view of the grouped assessments. Alternatively, you can also select the **Grouped attestations** on the left pane. The Assessment Instance page opens up, where you can take the assessment.


