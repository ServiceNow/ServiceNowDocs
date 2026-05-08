---
title: Expense Pre-Approval template
description: Build an application in App Engine Studio \(AES\) using the Expense Pre-Approval template to create, track, and manage planned expenses in your organization.The following tables, experiences, automated workflows, and roles are included in the Expense Pre-Approval template for App Engine Studio \(AES\).
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Available templates, Use an app template, Create your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Expense Pre-Approval template

Build an application in App Engine Studio \(AES\) using the Expense Pre-Approval template to create, track, and manage planned expenses in your organization.

To use the Expense Pre-Approval template, install this application from the ServiceNow Store.

Employees can easily submit their planned expenses for multiple levels of approval using the Expense Pre-Approval application. Managers can then review every submitted request. Approved requests are assigned to the budget review group, which can approve or reject the request. The employee receives a notification with the final status of the request.

To ensure compliance and improved financial planning, admins can customize the existing flow and levels of approval using decision tables. For more information, see Exploring Decision Tables.

For more information on creating an application using a template, see [Create your app using an application template](../task/use-app-template.md).

**Parent Topic:**[Available templates](template-library.md)

## Expense Pre-Approval template contents

The following tables, experiences, automated workflows, and roles are included in the Expense Pre-Approval template for App Engine Studio \(AES\).

### Tables in the Expense Pre-Approval app template

<table id="table_wdl_14z_xrb"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Budget definition\[x\_&lt;company-code&gt;\_&lt;expense\_approval\_app&gt;\_budget\_definition\]

</td><td>

The description of all budgets.

</td></tr><tr><td>

Expense request\[x\_&lt;company-code&gt;\_&lt;expense\_approval\_app&gt;expense\_request\]

</td><td>

The expense requests submitted by employees.

</td></tr><tr><td>

Expense line item\[x\_&lt;company-code&gt;\_&lt;expense\_approval\_app&gt;\_expense\_line\_item\]

</td><td>

Each expense line item in an expense request.

</td></tr></tbody>
</table>### Experiences in the Expense Pre-Approval app template

<table id="table_mph_l4z_xrb"><thead><tr><th>

Experience

</th><th>

Experience type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expense request \| Default view

</td><td>

Form

</td><td>

Form to create a new expense request.

</td></tr><tr><td>

Budget definition \| Default view

</td><td>

Form

</td><td>

Form to define budgets for a specified time frame.

</td></tr><tr><td>

Budget Reviewer

</td><td>

Mobile experience

</td><td>

Way to define what the mobile experience for budget reviewers looks like.

</td></tr><tr><td>

Expense request \| Workspace

</td><td>

Form

</td><td>

Form to create a new expense request.

</td></tr><tr><td>

Expense request \| Cost Approval

</td><td>

Form

</td><td>

Form to create a new expense request from an admin.

</td></tr><tr><td>

Manager

</td><td>

Mobile experience

</td><td>

Way to define what the mobile experience for managers looks like.

</td></tr><tr><td>

Budget definition \| Workspace

</td><td>

Form

</td><td>

Form in the workspace view to define budgets for a specified time frame.

</td></tr><tr><td>

*App name* - Budget workspace

</td><td>

Workspace

</td><td>

Way to configure a high-level view of all budget requests.

</td></tr><tr><td>

Expense request

</td><td>

Record producer

</td><td>

Way for employees to submit an expense request.

</td></tr><tr><td>

Expense line item \| Default view

</td><td>

Form

</td><td>

Form to add an expense line item to an expense request.

</td></tr><tr><td>

Expense Request SLA \| Default view

</td><td>

Form

</td><td>

Form to create an expense request based on a breach of service level agreement \(SLA\).

</td></tr><tr><td>

Budget definition \| Cost Approval

</td><td>

Form

</td><td>

Form in the cost approval view to define budgets for a specified time frame.

</td></tr><tr><td>

*App name* - Manager workspace

</td><td>

Workspace

</td><td>

Workspace where managers can approve or reject the expense requests assigned to them.

</td></tr><tr><td>

Cost Approval Mobile App

</td><td>

Mobile experience

</td><td>

iOS or Android app used for the following actions:-   Approving or rejecting expense requests.
-   Viewing dashboards that display historical data to compare budget and expense requests.
-   Creating or modifying budgets by budget reviewers.

</td></tr><tr><td>

Cost Approval Workspace - Budget Reviewer

</td><td>

Workspace

</td><td>

Budget reviewers can use the workspace for the following actions:-   Approving or rejecting expense requests.
-   Creating or modifying budgets.
-   Viewing the data on the budget funds allocated, spent, available, and allocated for the future.
-   Viewing dashboards that display historical data to compare the budget and expense requests.

</td></tr></tbody>
</table>### Automated workflows in the Expense Pre-Approval app template

<table id="table_knw_4qz_xrb"><thead><tr><th>

Workflow name

</th><th>

Workflow type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expense request approved - reviewer

</td><td>

Email

</td><td>

Notifies users that an expense request has been approved.

</td></tr><tr><td>

Expense Request Assigned

</td><td>

Email

</td><td>

Notifies users that an expense request has been assigned.

</td></tr><tr><td>

Expense request - SLA breached

</td><td>

Email

</td><td>

Notifies users that a service level agreement \(SLA\) has been breached.

</td></tr><tr><td>

Budget Creation

</td><td>

Flow - record

</td><td>

Executed when a budget reviewer creates a budget. It checks the start date of an expense request and associates the request to a budget with corresponding time frame.

</td></tr><tr><td>

Expense request - SLA- close to due

</td><td>

Email

</td><td>

Notifies users that a service level agreement \(SLA\) is close to due.

</td></tr><tr><td>

Expense Request Reassigned

</td><td>

Email

</td><td>

Notifies users that their request was reassigned.

</td></tr><tr><td>

Expense request comment added - Assigned

</td><td>

Email

</td><td>

Notifies users about a comment that has been added to their request.

</td></tr><tr><td>

New Expense Request or manager approval

</td><td>

Email

</td><td>

Notifies users about a new expense request.

</td></tr><tr><td>

Expense request reject

</td><td>

Email

</td><td>

Notifies users that their request was rejected.

</td></tr><tr><td>

Budget state update

</td><td>

Flow

</td><td>

Updates each budget record by priority.

</td></tr><tr><td>

Expense Request Inserted - Requestor

</td><td>

Email

</td><td>

Notifies users that their request was successfully created.

</td></tr><tr><td>

Expense Request Approved

</td><td>

Email

</td><td>

Notifies users that their request was approved.

</td></tr><tr><td>

Expense request work note added

</td><td>

Email

</td><td>

Notifies users a work note was added to their request.

</td></tr><tr><td>

Notify Team - Work note added

</td><td>

Email

</td><td>

Notifies a team that a work note was added to a request.

</td></tr><tr><td>

Expense request comment added - Employee

</td><td>

Email

</td><td>

Notifies users a comment was added to a request.

</td></tr><tr><td>

Expense Request Rejected

</td><td>

Email

</td><td>

Notifies users that their request was rejected.

</td></tr><tr><td>

Budget Updation

</td><td>

Flow - record

</td><td>

Executed when a budget reviewer modifies the budget. After a budget is modified, this flow updates the **Budget** field in the corresponding expense requests.

</td></tr><tr><td>

Notify Requestor - Comments added

</td><td>

Email

</td><td>

Notifies users that a comment was added to a request.

</td></tr><tr><td>

SLA Notification - Expense Request - warning

</td><td>

Flow - record

</td><td>

Warns admins about a potential service level agreement \(SLA\) issue.

</td></tr><tr><td>

Budget Approval Process

</td><td>

Flow - record

</td><td>

Executed to obtain expense approvals in the following scenarios:-   When an employee submits an expense request for the manager's approval.
-   Upon the manager's approval, the expense request is sent to the budget reviewer for the final level of approval.

</td></tr><tr><td>

Budget Calculations

</td><td>

Flow

</td><td>

Recalculates the budget spent and the available budget when a budget reviewer performs any of the following actions:-   Creates a budget
-   Modifies an existing budget
-   Approves an expense request

</td></tr></tbody>
</table>### Roles in the Expense Pre-Approval app template

<table id="table_gkr_zqz_xrb"><thead><tr><th>

Role label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Budget Reviewer\[x\_&lt;company-code&gt;\_&lt;expense\_approval\_app&gt;.Budget reviewer\]

</td><td>

Budget reviewers can create or modify budgets and provide the final level of approval on expense requests.

</td></tr><tr><td>

Manager\[x\_&lt;company-code&gt;\_&lt;expense\_approval\_app&gt;.Manager\]

</td><td>

Managers can submit, view, and approve or reject expense requests at the first level.

</td></tr><tr><td>

Employee\[x\_&lt;company-code&gt;\_&lt;expense\_approval\_app&gt;.Employee\]

</td><td>

Employees can submit and track expense requests.

</td></tr><tr><td>

Admin

</td><td>

The System Administrator role. This role has access to all system features, functions, and data, regardless of security constraints.

</td></tr></tbody>
</table>