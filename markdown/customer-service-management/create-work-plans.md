---
title: Create a work plan with Customer Service Management \(CSM\)
description: Create a work plan so that you can plan and delegate field service agents to fulfill the planned maintenance operations for an install base item on the Customer Service Management \(CSM\) \(CSM\) application and CSM Configurable Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install base work plans, Manage schedules and sites, Using Customer Service Management, Customer Service Management]
---

# Create a work plan with Customer Service Management \(CSM\)

Create a work plan so that you can plan and delegate field service agents to fulfill the planned maintenance operations for an install base item on the Customer Service Management \(CSM\) \(CSM\) application and CSM Configurable Workspace.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Products** &gt; **Install base item**.

2.  Open an install base item.

3.  Open the Work Plans related list and select **New**.

4.  On the form, fill in the fields.

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

Type of trigger that determines when work should be performed:-   **Model based:** Base the work plan on a specified model of a configuration item \(CI\).
-   **General:** Base the work plan on a table and filter.
-   **Install base:** Base the work plan on specified models of the install base items.
 **Note:**

-   Model-based plans apply only to hardware models, specifically ones that have at least one model category defined.
-   The install base plan type is available only if the Customer Service Install Base Management \(com.snc.install\_base\) plugin is activated.


</td></tr><tr><td>

Model

</td><td>

One or more product catalog items that you can select to identify the configuration items \(CIs\) or install base that requires maintenance. When you select a model, the associated table appears in the **Table** field. For example, if you select a specific PC model, the **Table** field displays **Computer \[cmdb\_ci\_computer\]**. This field appears if you selected either **Model based** or **Install base** type. For Install base type, the **Table** field automatically fills in an appropriate table that is based on the selected model.

</td></tr></tbody>
</table>5.  Right-click the form and select **Save**.


## Result

A draft of the work plan is created. Next, you can create a planned work schedule to make the work plan active and ready for an agent. To configure a planned work schedule, see [Configure a work schedule](https://www.servicenow.com/docs/access?context=configure-work-plan&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US).

