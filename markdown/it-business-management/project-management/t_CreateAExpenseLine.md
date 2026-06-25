---
title: Create an expense line
description: A project expense line is cost associated with a specific source, such as a user, fixed asset, or a CI. Expense lines are part of project cost plans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/t\_CreateAExpenseLine.html
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Starting a project, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create an expense line

A project expense line is cost associated with a specific source, such as a user, fixed asset, or a CI. Expense lines are part of project cost plans.

## Before you begin

Role required: it\_project\_manager

Application required: Project Portfolio Management with Financials

## About this task

Only processed expense lines are considered for projects, project tasks, and demands. You can create multiple expense lines for a project or demand.

## Procedure

1.  Open the project form.

2.  In the related lists, select **Cost Plans**.

3.  Right-click on a cost plan.

4.  Select **Create Expense Line**.

5.  On the form, fill in the details.

    For more information, see [Expense line form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/expense-line-form.md).

6.  Select **Submit**.

    **Note:**

    -   Imported processed expense lines are not rolled up to the Total actual cost field in Cost Plans.
    -   If you change the **Amount** of a Pending expense line and change the state to Processed, the latest value is captured in expense line and the same is rolled up to Total actual costs in Cost Plans.

## Result

Once the expense line is processed, the actual amount incurred becomes part of the cost plan.

The actual amount spent is recorded against the project cost plan under the appropriate expense type: **Capex** or **Opex**. Not providing a cost plan reference when creating an expense line, the actual cost is recorded at the project level in the cost plan related list.

If you create an expense line without populating the **Cost Plan** field, a [system-generated cost plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/cost-plan-breakdown.md) is created.

**Parent Topic:**[Starting a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/t_CreateAProject.md)

**Related topics**  


[Create a project task from a project]()

[Create a parent-child relationship on the Project Task form]()

[Create a monetary benefit plan for a project]()

[Create a non-monetary benefit plan for a project]()

[Associate monetary and non-monetary benefit plans]()

[Create a project cost plan]()

[Recalculating costs of all resource plans in a project]()

[Create and manage waterfall projects]()

[Update a project]()

[Copy a project]()

[Assign a project schedule]()

[Create baseline of a project]()

[Create a milestone]()

[Activate project task email notifications]()

[Change the planned start date of a project]()

[Create a cost type definition]()

[Costing add-on in Project Management]()

[Generate labor costs]()

[Create a project status report]()

[Allocate budget to a project]()

[Migrate budget of active projects to Next Experience]()

[Migrate financial baselines of projects to Next Experience]()

