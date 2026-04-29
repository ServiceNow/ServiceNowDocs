---
title: Group issues in the Workspace
description: Group issues within your workspaces to organize and manage related issues. Grouping similar issues can streamline your workflow and save time.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage issues, Common GRC features, Governance, Risk, and Compliance]
---

# Group issues in the Workspace

Group issues within your workspaces to organize and manage related issues. Grouping similar issues can streamline your workflow and save time.

## Before you begin

Role required: risk\_admin, risk\_manager, or sn\_risk.user

## About this task

Grouping issues under a parent can streamline your workflow and save time. All child issues are managed under a single parent, making it easier to track and address them collectively. You can group different types of issues under a single parent when issues belong to the same project or audit to gain a holistic view of how different issues are managed. Grouping issues under a parent helps in organizing and prioritizing them, reducing the redundancy of solving similar issues, and ensuring that issues are addressed in a coordinated manner.

You can enable the **Advanced issue grouping functionality** property to use the advanced issue grouping features, such as management methods for issue grouping and making standalone issues into parents. For more information, see [Governance, Risk, and Compliance properties](../reference/grc-properties.md).

**Important:** When you group issues with confidentiality enabled, you can add confidential child issues only under a confidential parent issue.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace**.

    You can navigate to your specific workspace.

2.  Select the list ![List icon.](../image/lists-icon.png) icon and navigate to the issues.

3.  Select the check boxes next to the issues that you want to group.

4.  Select **Group**.

5.  On the form, fill in the fields.

<table id="table_m42_blm_kkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group type

</td><td>

Option to select the group type. The available options are as follows:-   **Create a group**: Option to create a new parent issue to form a group.
-   **Add to an existing group**: Option to create a group with an existing parent issue.
-   **Make standalone issue as a parent**: Option to select an existing standalone issue and make it as a parent to create a group.

**Note:** The **Make standalone issue as a parent** option is only available if the **Advanced issue grouping functionality** property is enabled. For more information, see [Governance, Risk, and Compliance properties](../reference/grc-properties.md).

</td></tr><tr><td>

Parent issue name

</td><td>

Name of the new parent issue. This field appears only when **Create a group** is selected from **Group type** field.

</td></tr><tr><td>

Parent issue

</td><td>

Option to select an existing parent issue or to select an existing standalone issue and make it as a parent. This field appears only when **Create a group** or **Make standalone issue as a parent** is selected from **Group type** field.

</td></tr><tr><td>

Management method

</td><td>

Option to specify whether the issue is managed from a parent issue or as an individual child issue. The available options are as follows:-   **Manage parent**: When you select the Management method as **Manage parent**, the child issues inherit the values of the **State**, **Response**, and **Explanation** fields from the parent issue.
-   **Manage child**: When **Manage child** is selected, the child issue maintains its own **State**, **Response**, and **Explanation** fields individually.
**Note:** The **Management method** field is only available if the **Advanced issue grouping functionality** property is enabled. For more information, see [Governance, Risk, and Compliance properties](../reference/grc-properties.md).

</td></tr><tr><td>

Description

</td><td>

Additional information about the issue group.

</td></tr></tbody>
</table>6.  Select **Group**.


**Parent Topic:**[Manage issues](../concept/manage-issues-common-core.md)

