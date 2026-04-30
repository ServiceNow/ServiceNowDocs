---
title: Create demand to rationalize software applications
description: Create demands to rationalize SaaS and SSO applications by discontinuing software subscriptions, reducing software usage, and migrating users to approved software.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Overlapping usage view, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create demand to rationalize software applications

Create demands to rationalize SaaS and SSO applications by discontinuing software subscriptions, reducing software usage, and migrating users to approved software.

## Before you begin

Role required: sam\_admin or sam\_user

**Note:** The sam\_admin and sam\_user roles must have the it\_demand\_user role to create demand.

The PPM Standard \(com.snc.financial\_planning\_pmo\) plugin must be installed to create demands.

The Software Asset Management application includes the following demand actions that are ready for you to use:

-   Discontinue after expiration
-   Migrate to approved product
-   Discontinue immediately
-   Reclaim licenses
-   No action

## About this task

Use the Overlapping usage view to drive SaaS and SSO application rationalization by viewing the feature level usage of each application. For more information, see [Overlapping usage view](../concept/app-ration.md).

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **Overlapping usage**.

2.  Select the **Application feature usage** tab.

3.  Select the application in a category for which you want to create a demand.

4.  Select **Create demand**.

    The **Create demand** option is available only when you select an application that you want to create a demand for.

5.  On the form, fill in the fields.

<table id="table_xgh_pd2_4xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the demand.

</td></tr><tr><td>

Number

</td><td>

Unique auto-generated identification number for the demand.

</td></tr><tr><td>

Submission status

</td><td>

Stage of the demand record.-   Draft
-   Submitted
-   Screening
-   Qualified
-   Approved


</td></tr><tr><td>

Start date

</td><td>

Start date for the demand.The field name is replaced by **Planned start date** when the demand type is converted to a Project.

**Note:**

When you change the planned start date of a demand or project, the associated cost and resource plans also change.

</td></tr><tr><td>

Due date

</td><td>

Requested completion date for the demand.The field name is replaced by **Planned end date** when the demand type is converted to a Project.

</td></tr><tr><td>

Category

</td><td>

Software category of the demand.-   Strategic
-   Operational


</td></tr><tr><td>

Type

</td><td>

Type of demand.-   Enhancement
-   Project
-   Change
-   Defect
The **Category** field selection determines the selections available in this field.

</td></tr><tr><td>

Assessment required

</td><td>

Option for enabling the assessments for the demand.By default, the field is selected. When clear, the assessment questionnaire isn’t triggered for the demand.

When this field is clear, and you reset the demand to **Draft**, the value for the **Assessment Required** field is retained as clear.

</td></tr></tbody>
</table>6.  Select the **Demand Requirements** tab to view the details of the already-created requirements.

    You can also create a demand requirement. For more information, see [Create a demand requirement](create-demand-req.md).

7.  Select **Save**.


## Result

The demand is created with the **Submission status** field set to **Submitted**.

## What to do next

Use the ServiceNow® Demand Management application to approve and complete the demand. For more information, see [Demand Management](https://www.servicenow.com/docs/access?context=c_DemandManagement&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

You can create a project for the demand by selecting the **Create Project** related link. A project enables you to track the status, percent complete, and duration of the work required to accomplish the demand. You can also create project tasks to define the work items that are required to complete the project. For more information, see [Project Management](https://www.servicenow.com/docs/access?context=c_ProjectApplicationOverview&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

To view all Software Asset Management demands, navigate to **Software Asset** &gt; **Software Asset Demand** &gt; **Demands**.

To view all Software Asset Management demand requirements, navigate to **Software Asset** &gt; **Software Asset Demand** &gt; **Demand Requirements**.

