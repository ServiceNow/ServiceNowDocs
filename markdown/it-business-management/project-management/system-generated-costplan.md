---
title: System-generated cost plans
description: When an expense line is created without populating the Cost Plan field, system-generated cost plans are created automatically.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a project cost plan, Define a project, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# System-generated cost plans

When an expense line is created without populating the **Cost Plan** field, system-generated cost plans are created automatically.

The orphan expense lines are associated to the system-generated cost plans. This association ensures that the project actuals shown on the widgets or the total actuals are the same as the aggregate of the cost plan actuals on the grid shown on the Project Financials page and Investment Portal.

**Note:** System-generated cost plans are created only when the project has a minimum of one cost plan.

System-generated cost plans are created for any of the following reasons:

-   When you create an expense line without populating the **Cost Plan** field.
-   When you create a time card and approve it.

There are two system-generated cost plans, CapEx and OpEx. Depending on the type of expense selected while creating an expense line, the type of system-generated cost plan is created. The following are the name formats for the system-generated cost plans:

-   &lt;project number&gt; System generated CapEx costplan
-   &lt;project number&gt; System generated OpEx costplan

When you create a time card and approve it, an expense line of type CapEx is created and then the orphan expense line is associated to the system-generated cost plan of type CapEx. The system-generated cost plans are created to ensure that none of the expense lines are left without being associated to a cost plan. The system-generated cost plans are read-only.

For customers upgrading to Xanadu, you can run the project diagnostics, **Associate orphan expense lines to the system generated cost plan**, to associate orphan expense lines to a system-generated cost plan. The diagnostic scan lists the expense lines that are not associated to any cost plan. When you run the fix script, system-generated cost plans are created, and the orphan expense lines are associated to the system-generated cost plans.

**Parent Topic:**[Create a project cost plan](../task/t_CreateAProjectCostPlan.md)

