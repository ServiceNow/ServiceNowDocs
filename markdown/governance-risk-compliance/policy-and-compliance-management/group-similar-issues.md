---
title: Group similar issues under a new parent issue
description: When you are creating an issue, you have the option of grouping the issue with other similar issues.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manually create issues, Manage issues, Classic UI, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Group similar issues under a new parent issue

When you are creating an issue, you have the option of grouping the issue with other similar issues.

## Before you begin

Role required: \(per product\)

-   In Policy and Compliance Management: compliance\_admin, compliance\_manager, or sn\_compliance.user
-   In Risk Management: risk\_admin, risk\_manager, or sn\_risk.user
-   In Audit Management: audit\_admin, audit\_manager, audit\_admin, or sn\_audit.user

## About this task

Grouping issues under a parent can save you valuable time. For example, assume you have an issue related to patching Windows servers. Since each server is a separate entity, all controls associated with "Windows servers should be patched every Tuesday" will have the same issue. Therefore, the issue can be resolved once for all of the Windows servers by applying the relevant patch one time. So, this feature can be used to group similar issues and resolve them all at the parent level.

## Procedure

1.  Navigate to one of the following locations:

    -   **Policy and Compliance** &gt; **Issues** &gt; **Create New**.
    -   **Risk** &gt; **Issues** &gt; **Create New**.
    -   **Audit** &gt; **Issues** &gt; **Create New**.
2.  On the form, locate the **Parent issue** field.

    ![Parent field](../image/parent-no-num.png)

3.  Click the bulb icon \(![bulb icon](../image/bulb.png)\) to view similar issues that you may want to assign to this parent issue.

    ![Similar issue suggestions](../image/similar-issue-suggestion.png)

    **Note:** Standalone issues are similar to the current issue, but that are not assigned to a parent issue group. The Confidence score is calculated using a similarity definition included in the GRC: Predictive Intelligence application base system.

4.  You can click the Information icon to view details for any similar issues in order to help determine whether they should be grouped with the current issue.

5.  Select the similar issues you want to group with the current issue, and click **Group**.

    ![Group issues](../image/group-ssues.png)

6.  On the form, fill in the fields.

<table id="table_ynl_yjz_dv"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group

</td><td>

To group the selected issues and assign them to a new group, select **Create a new group**.To add the selected issues to an existing group, select the group.

</td></tr><tr><td>

New group

</td><td>

This field displays only if you selected **Create a new group**. Type the name of the new group.

</td></tr><tr><td>

Description

</td><td>

This field displays only if you selected **Create a new group**. Type a description of the group.

</td></tr><tr><td>

Assigned to

</td><td>

This field displays only if you selected **Create a new group**. Select the user to whom the group is assigned.

</td></tr></tbody>
</table>7.  Click **OK**.

    The selected issues are added to a new or existing group.

8.  You can view the issue in the group by clicking the **Issues** tab.


**Parent Topic:**[Manually create GRC issues](../../grc-common/task/t_CreateAnIssue.md)

