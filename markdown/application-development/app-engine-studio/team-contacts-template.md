---
title: Team Contacts template
description: Build an application in App Engine Studio \(AES\) using the Team Contacts template to manage contact information for the people in your organization.The following tables, experiences, automated workflows, and roles are included in the Team Contacts template for App Engine Studio \(AES\).
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Available templates, Create your app using an application template, Create your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Team Contacts template

Build an application in App Engine Studio \(AES\) using the Team Contacts template to manage contact information for the people in your organization.

To use the Team Contacts template, install this application from the ServiceNow Store.

![Team Contacts App template](../image/template-team-contacts.png)

A team contacts app uses a mobile experience to view employee contact information, tag favorites, and add privacy notes. The app displays report information by default and lets an employee search for employees, view employee profiles, and create a list of favorite employee contacts.

For more information on creating an application using a template, see [Create your app using an application template](../task/use-app-template.md).

**Parent Topic:**[Available templates](template-library.md)

## Team Contacts template contents

The following tables, experiences, automated workflows, and roles are included in the Team Contacts template for App Engine Studio \(AES\).

### Tables in the Team Contacts app template

<table id="table_sfc_wck_g4b"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Relationship Contact Table\[x\_&lt;company-code&gt;\_&lt;team\_contact&gt;\_relationship\_contact\]

</td><td>

Tracks employee contact information. For example, contact names, date created, favorites, and updates.

</td></tr><tr><td>

Reminder Table\[x\_&lt;company-code&gt;\_&lt;team\_contact&gt;\_relationship\_contact\_reminders\]

</td><td>

Tracks reminders created by your team. For example, when to send a reminder and the subject of a reminder.

</td></tr><tr><td>

Relationship Notes Table\[x\_&lt;company-code&gt;\_&lt;team\_contact&gt;\_relationship\_notes\]

</td><td>

Tracks the notes that employees create for each other. For example, the employee name, reason for contact, HTML notes, and option to mark the contact as a favorite.

</td></tr></tbody>
</table>### Experiences in the Team Contacts app template

|Experience|Experience type|Description|
|----------|---------------|-----------|
|Employees Mobile experience|Mobile experience|Provides employees access to an employee directory and relationship notes using your organization's iOS or Android app.|
|Team contact|Portal|Portal where employees and managers can view employee profiles, mark favorite contacts, and add relationship notes using a website. The team contacts portal includes a sign-in page, a home page, and a page to add relationship notes.|
|Note \| Default view|Form|Form to add notes to contact information.|
|Relationship contact|Form|Form to view contact information.|
|Reminder \| Portal|Form|Form for employees and managers to set reminders.|
|Reminder \| Default view|Form|Form for employees and managers to set reminders.|
|Note \| Portal|Form|Form for managers and employees to add notes to contacts.|

### Automated workflows in the Team Contacts app template

|Workflow name|Workflow type|Description|
|-------------|-------------|-----------|
|Team Contact Reminder Push|Email|Sends a reminder push to employees.|
|Notify Contact Reminder|Flow - record|Sends a notification about a reminder that an employee sets up in a relationship note. The notification contains details from the relationship note.|
|Team Contact Reminder Notification|Email|Sends a reminder to employees.|
|Team Contact Reminder Ackn Notification|Email|Sends employees a reminder to acknowledge a notification.|

### Roles in the Team Contacts app template

<table id="table_zdj_jyz_l4b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Manager\[x\_&lt;company-name&gt;\_ &lt;app-name&gt;.manager\]

</td><td>

Managers can view profile info, add relationship notes, and see their direct reports.

</td><td>

Create, Read \(own\), Update \(own\), Delete \(own\)

</td></tr><tr><td>

Admin\[x\_&lt;company-name&gt;\_ &lt;app-name&gt;.admin\]

</td><td>

Managers can configure the team contacts app and grant access to the app.

</td><td>

Read \(all\), Update \(all\), Delete

</td></tr><tr><td>

Employee\[x\_&lt;company-name&gt;\_ &lt;app-name&gt;.employee\]

</td><td>

Employees can view information on their team, search for employees, view employee profiles, and mark favorite contacts.

</td><td>

Create, Read \(own\), Update \(own\), Delete \(own\)

</td></tr><tr><td>

Canvas user

</td><td>

User role for Canvas Core application

</td><td>

 

</td></tr></tbody>
</table>