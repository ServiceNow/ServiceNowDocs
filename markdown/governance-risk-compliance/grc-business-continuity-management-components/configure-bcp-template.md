---
title: Configure a business continuity plan template
description: Configure the business continuity plan \(BCP\) template to create and assign business continuity plans with standard object types. The object types can be business processes, applications, employees, hardware, software, and others.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [BCM in the Classic Workspace, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure a business continuity plan template

Configure the business continuity plan \(BCP\) template to create and assign business continuity plans with standard object types. The object types can be business processes, applications, employees, hardware, software, and others.

## Before you begin

Role required: sn\_bcm.admin

## About this task

By configuring the plan template, you can:

-   Define the primary object type that has to be recovered.
-   Define documentation sections that should be included right at the beginning of a plan.
-   Identify the loss scenarios and plan accordingly using the template.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Plan Configuration** &gt; **Plan Templates**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_k3d_xgj_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the plan template.

</td></tr><tr><td>

Description

</td><td>

Brief description about the plan template.

</td></tr><tr><td>

Primary Element Recovered

</td><td>

Primary object type or an element identified to be recovered in the plan.

</td></tr><tr id="plan-auth-type"><td>

Plan authoring type

</td><td>

Different phases or sections of a plan that are available as options when you create a continuity plan using this template. These options show as tabs in the BCP workspace as you proceed to complete the plan details.-   **All** \(Default\): All options like Documentation, Loss Scenarios, Recovery tasks, and Recovery teams are displayed in the plan that uses this template. You can view these options as tabs in the workspace.
-   **Documentation**: Plan that uses this template displays the documentation option along with selected dependencies. Documentation tab along with Recovery tasks and Recovery teams are available for view in the workspace.
-   **Loss Scenarios**: Displays the loss scenarios along with Recovery tasks, Recovery teams, and other selected dependencies in the plan that uses this template.
-   **Recovery tasks**: Displays recovery tasks and Recovery teams associated to the plan type that uses this template.


</td></tr><tr><td>

Group recovery tasks

</td><td>

Option to pre-group tasks in the Group column of the recovery task grid based on a group by value.

</td></tr><tr><td>

Group by

</td><td>

Field appears if the **Group recovery tasks** option is enabled. Group by value based on which the recovery tasks are pre-grouped in the Group column.

</td></tr></tbody>
</table>4.  Click **Submit**.


