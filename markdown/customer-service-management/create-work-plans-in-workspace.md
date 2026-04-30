---
title: Create a work plan in Customer Service Management \(CSM\) Configurable Workspace
description: Create a work plan in the Customer Service Management \(CSM\) Configurable Workspace so that your agents can fulfill and implement the maintenance requirements for an install base item.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using CSM Configurable Workspace in Customer Service Management, Manage cases, Using Customer Service Management, Customer Service Management]
---

# Create a work plan in Customer Service Management \(CSM\) Configurable Workspace

Create a work plan in the Customer Service Management \(CSM\) Configurable Workspace so that your agents can fulfill and implement the maintenance requirements for an install base item.

## Before you begin

Role required: sn\_customerservice\_agent and sn\_fsm\_planned\_wm.planned\_work\_admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, navigate to **Customer** &gt; **Accounts**.

3.  Open an account and navigate to the Install Base Items related list.

4.  Open an install base item from the list.

5.  On the **Planned Maintenance** tab, open **Work plans** and select **New**.

6.  On the form, fill in the fields.

<table id="table_qvk_hg2_cyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the work plan.

</td></tr><tr><td>

Type

</td><td>

Type of trigger that determines when work should be performed.-   **Model based:** Base the work plan on a specified model of a CI.
-   **General:** Base the work plan on a table and filter.
-   **Install base:** Base the work plan on specified models of install base items
 **Note:**

-   Model-based plans apply only to hardware models, specifically ones that have at least one model category defined.
-   The Install base plan type is available only if the Customer Service Install Base Management \(com.snc.install\_base\) plugin is activated.


</td></tr><tr><td>

Model

</td><td>

One or more product catalog items that you can select to identify the configuration items \(CIs\) or install base that require maintenance. When you select a model, the associated table appears in the Table field. For example, if you select a specific PC model, the **Table** field displays **Computer \[cmdb\_ci\_computer\]**. This field appears if you selected either the **Model based** or **Install base** type. For Install base type. The **Table** field automatically fills in an appropriate table based on the selected model.

</td></tr></tbody>
</table>7.  Select **Save**.


## Result

You created a work plan in Customer Service Management \(CSM\) Configurable Workspace.

