---
title: Emergency Alert template
description: Build an application in App Engine Studio \(AES\) using the Emergency Alert template to manage communications and track essential resources during an emergency.The following tables, experiences, automated workflows, and roles are included in the Emergency Alert template for App Engine Studio \(AES\).
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Available templates, Create your app using an application template, Create your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Emergency Alert template

Build an application in App Engine Studio \(AES\) using the Emergency Alert template to manage communications and track essential resources during an emergency.

To use the Emergency Alert template, install this application from the ServiceNow Store.

![Emergency Alert template](../image/template-emergency-alert.png)

An emergency alert app allows your organization to keep employees informed and connected during natural disasters and infectious diseases, such as COVID-19.

You can use the Emergency Alert template to create command center dashboards and a mobile app to monitor and notify employees about the latest news. Employees can self-report their status, request work-from-home or time off, and receive instructions during an emergency. Managers can assess the impact on their respective teams, approve or reject requests, request for status, and automatically receive instruction on actions to take during any emergency.

For more information on creating an application using a template, see [Create your app using an application template](../task/use-app-template.md).

**Parent Topic:**[Available templates](template-library.md)

## Emergency Alert template contents

The following tables, experiences, automated workflows, and roles are included in the Emergency Alert template for App Engine Studio \(AES\).

### Tables in the Emergency Alert app template

<table id="table_z3j_qls_j4b"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status Report Request Table\[x\_&lt;company&gt;\_&lt;my emergency\_alert\_app&gt;\_status\_report\_requests\]

</td><td>

Track the severity of an emergency reported by employees. For example, the status, the color associated with danger levels, and conditions.

</td></tr><tr><td>

Self Report Table\[x\_&lt;company&gt;\_&lt;my emergency\_alert\_app&gt;\_status\_report\]

</td><td>

Track reported emergencies created by employees or managers. For example, the emergency details, status, duration, and affected individuals.

</td></tr><tr><td>

Emergency Alert Table\[x\_&lt;company&gt;\_&lt;my emergency\_alert\_app&gt;\_emergency\_alert\]

</td><td>

Track emergency alerts for your company. For example, the emergency type, who created the alert, and who has read the alerts.

</td></tr><tr><td>

Work Status Request Task Table\[x\_&lt;company&gt;\_&lt;my emergency\_alert\_app&gt;\_work\_status\_request\_task\]

</td><td>

Track the work status request of an emergency. For example, the requester, the assignee, and the state of the work status.

</td></tr></tbody>
</table>### Experiences in the Emergency Alert app template

|Experience|Experience type|Description|
|----------|---------------|-----------|
|Emergency alert \| SendEmergency AlertWS|Form|Form to create a new emergency alert record.|
|Self Report \| Employee View|Form|Form for employees to report an emergency.|
|Self Report \| Default View|Form|Form for employees to report an emergency.|
|Emergency Alert - Portal|Portal|Portal where employees can view reported emergencies, the status of their team, and submit a self report.|
|Emergency Alert \| Default View|Form|Form to create a new emergency alert and connect knowledge resources to it.|
|Self Report \| Update Report|Form|Form for employees to self report their health status.|
|Self Report \| Activity View|Form|Form to add comments about a self report.|
|Self Report \| RequestReportWS|Form|Form to self report an emergency within a specific time frame.|
|Status Report Request \| Default View|Form|Form to send an update about an emergency with time and location details.|
|Self Report \| Update status report|Form|Form to add an update about an emergency.|
|*App name* Workspace|Workspace|Workspace where admins can set up and send notifications, view dashboards, and configure lists and forms.|
|Work Status Request Task \| Default view|Form|Form to update an employee about a work status request.|

### Automated workflows in the Emergency Alert app template

|Workflow name|Workflow type|Description|
|-------------|-------------|-----------|
|Emergency report/update state for managers|Email|Notifies managers to update an emergency report if the source is empty.|
|Emergency Alert App - Please report or update status|Flow - record|Requests a status update on work.|
|Emergency Alert App - Status request for employees from manager|Flow - record|Notifies employees that a status request is made by their manager.|
|Self report submitted without manager|Email|Notifies that an employee submitted an expense request without listing their manager.|
|Emergency Alert App - Create Work Status Task When Self Report is created|Flow - record|Starts the work status task when a self report emergency is submitted.|
|Emergency Alert App - Create Status Report Requests for Affected|Flow|Creates or updates status report requests.|
|Emergency alert app - Create App Self Reports|Flow - record|Sends a notification when a report request is created or updated.|
|Emergency Alert App - Request for WFH/Time off submitted|Flow - record|Starts the work from home or time off request approval flow.|
|Emergency instructions for employees|Email|Notifies users if a status update is requested.|
|Emergency Alert App - Employee emergency report changes to submitted|Flow - record|Sends a notification when an employee self report has been submitted.|
|Emergency Alert App - Request for WFH/Time off approved/denied|Flow - record|Sends a notification to an employee when a WFH or Time off request is approved or denied.|
|Emergency Alert App - Employee emergency report request response submitted|Flow - record|Sends a notification when an employee emergency report has been submitted.|
|Request for WFH approved|Email|Notifies an employee that their request to work from home was approved.|
|Emergency alert app - Emergency instructions for employees|Flow - record|Sends employees instructions to follow during an emergency.|
|Please report/update status of employee|Email|Requests information about the status of an employee.|
|Self-report submitted for manager|Email|Notifies a manager that an emergency alert has been created and needs review.|
|Emergency Instructions for managers|Email|Notifies managers that their request was created and that their team will receive information about it.|
|Please report/update status|Email|Sends a notification when a status change has been committed.|
|Request for WFH/Time off submitted|Email|Notifies an employee that their work from home or time off request was successfully submitted.|
|Employee Emergency report submitted|Email|Notifies an employee that their emergency report was successfully submitted.|
|Emergency Alert App - Manager emergency request submitted|Flow - record|Sends a notification when a manager emergency report has been submitted.|
|Emergency Alert App - Employee emergency report submitted|Flow - record|Sends a notification when an employee submits changes to an emergency report.|
|Create KB article|Flow - record|Creates a knowledge base article when a new emergency alert is created.|
|Employee emergency report request submit|Email|Notifies an employee that their request for status was submitted and that their manager will be notified.|
|Emergency Alert App - Cancel work status task if self report closed|Flow - record|Cancels a work status request if the self report is closed.|
|Manager emergency request submitted|Email|Notifies managers that the emergency report was sent.|
|Please report/update status of employee|Email|Notifies employees of action needed on their self report.|
|Request for WFH denied|Email|Notifies the employee that their work from home request was denied.|
|Emergency Alert App - Emergency report/update state for managers|Flow - record|Sends a notification based on changes in an emergency alert report.|

### Roles in the Emergency Alert app template

<table id="table_okv_fps_j4b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Emergency alert admin\[x\_&lt;company-code&gt;\_ &lt;my emergency\_alert\_app&gt;.emergency\_alert\_admin\]

</td><td>

Admins manage the app and configure the dashboard

</td><td>

Create, Read \(all\), Edit \(all\), Delete

</td></tr><tr><td>

Emergency alert manager\[x\_&lt;company-code&gt;\_ &lt;my emergency\_alert\_app&gt;.manager\]

</td><td>

Managers can approve or reject requests, access dashboards, and send notifications

</td><td>

Create, Read \(all\), Edit \(all\)

</td></tr><tr><td>

Emergency alert employee\[x\_&lt;company-name&gt;\_ &lt;my emergency\_alert\_app&gt;.emergency\_alert\_employee\]

</td><td>

Self-report emergency alerts

</td><td>

Create, Read \(own\), Edit \(own\)

</td></tr><tr><td>

Admin

</td><td>

The System Administrator role. This role has access to all system features, functions, and data regardless of security constraints.

</td><td>

Create, Read \(all\), Edit \(all\), Delete

</td></tr><tr><td>

Public

</td><td>

No login is required to access features or functions with the public role.

</td><td>

No access by default.

</td></tr></tbody>
</table>