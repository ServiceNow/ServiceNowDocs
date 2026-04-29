---
title: Time Off template
description: Build an application in App Engine Studio \(AES\) using the Time Off Requests template to schedule employee vacations and time-off.The following tables, experiences, automated workflows, and roles are included in the Time Off template for App Engine Studio \(AES\).
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Available templates, Use an app template, Create your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Time Off template

Build an application in App Engine Studio \(AES\) using the Time Off Requests template to schedule employee vacations and time-off.

To use the Time Off template, install this application from the ServiceNow Store.

Create a time off application to streamline the process for employees to request time off through a single mobile or web-based form. Managers are notified via email when a request is submitted. They can use a mobile app or a web-based portal to view historical and pending requests by month or year for an employee or their entire team. This allows the manager to make informed decisions, improve planning for upcoming work, or identify where shifts must be covered. Employees are automatically notified when their requests are approved or rejected and why. If plans change and updates to an approved request are required, the employee can edit and resubmit their requests for approval through the portal.

For more information on creating an application using a template, see [Create your app using an application template](../task/use-app-template.md).

**Parent Topic:**[Available templates](template-library.md)

## Time Off template contents

The following tables, experiences, automated workflows, and roles are included in the Time Off template for App Engine Studio \(AES\).

### Tables in the Time Off app template

<table id="table_y5c_3dt_j4b"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Time Off Request Table\[x\_&lt;company-code&gt;\_&lt;my\_time\_off\_request\_app&gt;\_request\]

</td><td>

Track time off requests that employees create using the Time Off Request app. For example, the employee name, creation date, manager, requested days off, and state of the time off request.

</td></tr></tbody>
</table>### Experiences in the Time Off app template

|Experience|Experience type|Description|
|----------|---------------|-----------|
|Time Off Request \| Default view|Form|Form for managers and admins to use as a template for time off requests.|
|Time Off Request \| Workspace|Form|Workspace where managers can view, submit, and approve or reject time off requests. The workspace also contains historical records which can be viewed by team, employee, and time.|
|*App name* \| Portal|Portal|Portal for managers and admins to view, submit, and approve or reject time off requests and for employees to view, edit, review, or cancel their time off requests.|
|*App name* \| Workspace|Workspace|Workspace where managers and admins can use view, submit, and approve or reject time off requests.|
|Time Off Request \| Record|Form|Form that managers can use to view, submit, and approve or reject time off requests.|
|Time Off Request \| New|Form|Users can create new \(save, submit, or cancel\), update \(save, submit, delete, or cancel\), and review \(approve or reject\) time off requests.|
|Mobile app|Mobile experience|Employees can request time off and access their requests. Managers can submit, view, update, approve or reject time off requests using your organization's iOS or Android app.|
|Dashboard|Mobile experience|Managers and admins can view time off requests using your organization's iOS or Android app.|

### Automated workflows in the Time Off app template

|Workflow name|Workflow type|Description|
|-------------|-------------|-----------|
|Time off request - Send comments|Flow - record|Sends a notification to an employee or manager when a comment has been added to a time off request.|
|Daily Time Off inactivating records|Flow|Updates the remaining time off on Time off request records until the remaining days is set to 0.|
|Time Off Req Approved|Email|Notifies an employee of an approved time off request.|
|Time Off Req Updated/resubmitted|Email|Notifies managers of updated/resubmitted time off requests.|
|Time Off Comments|Email|Notifies an employee or manager of a comment added to a time off request.|
|Time Off requests - Send notifications|Flow - record|Sends a notification to an employee or manager when a time off request state changes. The notification contains details from the time off request.|
|Time Off Request Cancelled|Email|Notifies an employee or manager of a cancelled time off request.|
|Time Off Request Rejected|Email|Notifies an employee of a rejected time off request.|
|Time Off Request - updated/resubmitted|Flow - record|Sends a notification to an employee or manager that a time off request is updated/resubmitted.|
|Time Off Req Submitted|Email|Notifies a manager when a time off request is submitted.|
|Time Off Request|Email|Employees can draft, request, approve, reject, and cancel time off requests.|

### Roles in the Time Off app template

<table id="table_ygm_m2t_j4b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Manager\[x\_&lt;company-name&gt;\_ &lt;my time\_off\_request\_app&gt;.manager\]

</td><td>

Managers can submit, view, approve, and reject time off requests

</td><td>

Create, Read \(all\), Edit \(all\)

</td></tr><tr><td>

Employee\[x\_&lt;company-name&gt;\_ &lt;my time\_off\_request\_app&gt;.employee\]

</td><td>

Employees can submit, view, edit, and cancel time off requests

</td><td>

Create, Read \(own\), Edit \(own\), Delete \(own\)

</td></tr><tr><td>

Admin\[x\_&lt;company-name&gt;\_ &lt;my time\_off\_request\_app&gt;.admin\]

</td><td>

Admins can manage the time off app and view all records

</td><td>

Create, Read \(all\), Edit \(all\), Delete \(all\)

</td></tr><tr><td>

Public

</td><td>

Public users require no login to access features or functions within the application.

</td><td>

Role contains no access by default.

</td></tr></tbody>
</table>