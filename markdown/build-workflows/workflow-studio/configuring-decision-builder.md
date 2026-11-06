---
title: Configuring decision tables
description: Workflow Studio is installed automatically with each family upgrade. By updating to the latest version of Workflow Studio, you have the latest updates to decision tables. Configure Workflow Studio and assign roles to your staff based on the permission level they require.Learn about the personas who use decision tables in Workflow Studio, including roles and permissions required for certain tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/configuring-decision-builder.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Workflow Studio, Build workflows]
---

# Configuring decision tables

Workflow Studio is installed automatically with each family upgrade. By updating to the latest version of Workflow Studio, you have the latest updates to decision tables. Configure Workflow Studio and assign roles to your staff based on the permission level they require.

For more information, see [Update to the latest version of Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/update-to-the-latest-version-of-workflow-studio.md).

**Parent Topic:**[Configuring Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/configuring-workflow-studio.md)

## Decision tables roles and permissions

Learn about the personas who use decision tables in Workflow Studio, including roles and permissions required for certain tasks.

### Personas

Review the personas and roles used in decision tables in Workflow Studio.

-   **Decision table admin**

    The decision table admin can create and edit any part of a decision table. The admin may make high-level decisions about when a decision table is needed, create the table, and then pass on the work of authoring the rules in the table to someone else. Decision table admins are the only persona who can create inputs and decision table columns and values.

-   **Decision table reader**

    The decision table reader has read-only access to decision tables. They can't add or delete inputs, conditions, or results, but they can export a decision table to Excel.

-   **Decision rule author**

    The decision rule author has the most access to update decision tables after the decision table admin. The admin may create a table with inputs and table columns and then pass on the rest of the work to the decision rule author. The decision rule author can add, rearrange, and delete decision rows and edit condition and result values in all rows and columns.

-   **Decision result editor**

    The decision result editor can only edit result values in existing decision rows. The decision result editor may change a value based on a new business decision or policy.

-   **Delegated developer**

    A delegated developer can create, read, edit, and delete decision tables that belong to an application they have delegated developer access to. A delegated developer can't access decision tables in other applications or scopes.


<table id="table_bvq_s5d_qqb"><thead><tr><th>

Role

</th><th>

Tasks

</th></tr></thead><tbody><tr><td>

admin and decision\_table\_admin

</td><td>

Create, read, edit, and delete inputs and decision table columns and values.

</td></tr><tr><td>

decision\_table\_reader

</td><td>

Read-only access to inputs and decision table columns and values.

 In decision tables, users with this role can export decision tables to Excel.

</td></tr><tr><td>

decision\_rule\_author

</td><td>

Read-only access to inputs and decision table columns.

 In decision tables, users with this role can do the following:

-   Add new decision rows
-   Rearrange decision rows
-   Delete decision rows
-   Edit condition and result values in all rows and columns

</td></tr><tr><td>

decision\_result\_editor

</td><td>

Read-only access to inputs, decision table columns, and conditions.

 In decision tables, users with this role can edit result values in existing decision rows.

</td></tr><tr><td>

delegated\_developer

</td><td>

Create, read, edit, and delete decision tables in applications that the user has delegated developer access to.

</td></tr></tbody>
</table>