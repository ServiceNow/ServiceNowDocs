---
title: Install Employee Readiness Core
description: You can install Employee Readiness Core if you have the admin role.Several types of components are installed with Employee Readiness Core, including user roles, tables, and scheduled jobs.
locale: en-US
release: zurich
product: Employee Readiness Core
classification: employee-readiness-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Employee Readiness Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Install Employee Readiness Core

You can install Employee Readiness Core if you have the admin role.

## Before you begin

Employee Readiness Core version 1.1.0 and later requires the following plugins.

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   Workflow Studio Action Step - Payload Builder \(com.glide.hub.action\_step.payload\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)

These plugins must be requested through the Now Support Service Catalog. For instructions, see [Request a plugin](https://www.servicenow.com/docs/access?context=t_RequestAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Role required: admin

<table id="table_kxr_yz3_blb"><thead><tr><th>

Type

</th><th>

Instructions

</th></tr></thead><tbody><tr><td>

Commercial on-premise

</td><td>

Visit the ServiceNow® Store to download and install the application.

</td></tr><tr><td>

Federal hosted

</td><td>

See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

Federal on-premise

</td><td>

If you are a federal on-premise customer and you would like to install this application, reach out to your sales representative or open a Now Support or HIWAVE ticket. In the ticket, request to be routed to the SHOT team.

 See the [Federal downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030260\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030260) article in the Store Help Center for more information.

</td></tr><tr><td>

On-premise

</td><td>

See the [Commercial downloads for the Emergency Response Management and Safe Workplace suite apps \[KB0030258\]](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030258) article in the Store Help Center for more information.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for `Employee Readiness Core`.

3.  Click **Install**.

    The Application installation dialog box opens.

4.  Load the demo data by selecting the **Load demo data** check box.

    For information about how to install or reinstall demo data after the initial installation, see the [Work around to install demo data if application is already installed \[KB0722909\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0722909) article in the Now Support Knowledge Base.

5.  Click **Install**.

6.  When the installation is complete, click **Close**.


**Parent Topic:**[Employee Readiness Core](../concept/employee-readiness-core.md)

## Components installed with Employee Readiness Core

Several types of components are installed with Employee Readiness Core, including user roles, tables, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Employee Readiness Core admin\[sn\_imt\_core.admin\]

</td><td>

Can create and manage health and safety users, health requirements,privacy consent templates and policies, and Safe Workplace audiences.

 Can read non-required health and safety records.

</td><td>

-   sn\_imt\_core.reader
-   flow\_operator
-   sn\_imt\_core.privacy\_consent\_user
-   sn\_imt\_core.safe\_workplace\_audience\_admin

</td></tr><tr><td>

Employee Readiness Core reader\[sn\_imt\_core.reader\]

</td><td>

Can view health and safety requirement statuses in the View Employee and Visitor Status module.

</td><td>

None

</td></tr><tr><td>

Safe Workplace audience admin\[sn\_imt\_core.safe\_workplace\_audience\_admin\]

</td><td>

Can create and manage Safe Workplace audiences.

 Can read non-required health and safety records.

</td><td>

None

</td></tr><tr><td>

External web service user\[sn\_imt\_core.api\_logging\_user\]

</td><td>

External service user that can make table API calls to insert log entries.

</td><td>

None

</td></tr><tr><td>

Privacy consent user\[sn\_imt\_core.privacy\_consent\_user\]

</td><td>

Can submit and update the user privacy consent for themselves.

</td><td>

None

</td></tr><tr><td>

Health and safety approver\[sn\_imt\_core.health\_and\_safety\_approver\]

</td><td>

Can review the requests and responses of all users in the Approval Portal such as vaccine exemption requests, vaccine responses, and health test results.

</td><td>

None

</td></tr><tr><td>

Approval Portal manager\[sn\_imt\_core.approval\_portal\_manager\]

</td><td>

Can review the requests and responses of their direct reports in the Approval Portal when the appropriate application-specific property is enabled for the corresponding record type. For example, you can enable a property in Vaccination Status to allow managers to review vaccine responses.

</td><td>

None

</td></tr></tbody>
</table>### Tables installed

<table id="table_udb_2hn_2mb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety User\[sn\_imt\_core\_health\_and\_safety\_user\]

</td><td>

List of users and visitors and their progress toward completing all applicable active requirements.

</td></tr><tr><td>

Health and Safety Requirement\[sn\_imt\_core\_health\_and\_safety\_requirement\]

</td><td>

List of all health and safety requirements.

</td></tr><tr><td>

Employee Health and Safety Requirement\[sn\_imt\_core\_employee\_health\_and\_safety\_requirement\]

</td><td>

List of user and visitor statuses for all active requirements.

</td></tr><tr><td>

Health and Safety Visitor\[sn\_imt\_core\_visitor\]

</td><td>

List of visitors.

</td></tr><tr><td>

Health and Safety Visitor Invitation\[sn\_imt\_core\_visitor\_invitation\]

</td><td>

List of visitor invitations, including information about their reason for visiting and the location they are invited to visit.

</td></tr><tr><td>

Location Privacy Configuration\[sn\_imt\_core\_location\_privacy\_configuration\]

</td><td>

Configuration for the location-based privacy policy, such as the privacy statement for a location and whether a particular location requires privacy consent.

</td></tr><tr><td>

Privacy Consent Template\[sn\_imt\_core\_privacy\_consent\_template\]

</td><td>

Template for storing the privacy statement for a location that is used in the location privacy configuration.

</td></tr><tr><td>

User Privacy Notice and Consents\[sn\_imt\_core\_user\_privacy\_notice\_and\_consent\]

</td><td>

Responses of employees to the privacy consent.

</td></tr><tr><td>

Safe Workplace Audiences\[sn\_imt\_core\_safe\_workplace\_audience\]

</td><td>

Collections of users based on one or more criteria, such as groups, departments, and locations. Use Safe Workplace audiences to organize lists of users for sending outreach notifications.

</td></tr><tr><td>

Data Retention Policies\[sn\_imt\_core\_data\_retention\]

</td><td>

Configuration for country-specific data retention policies for Health and Safety Testing and Vaccination Status. Users with the sn\_imt\_core.admin, sn\_imt\_health\_test.admin, or sn\_imt\_vaccine.admin roles can configure these policies.

</td></tr></tbody>
</table>### Scheduled jobs installed

<table id="table_isr_rmn_1mb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mark expired user requirements as not\_cleared

</td><td>

Runs every 30 minutes to update user requirement statuses to **Not Cleared** if they have exceeded the time limit they are valid for.**Note:** The scheduled job only runs for requirements that have the **Use duration** field selected.

</td></tr><tr><td>

Collect Safe Workplace users

</td><td>

Runs weekly to create health and safety user records for users \[sys\_user\] with activity or an assigned role in any of the following Safe Workplace suite and Emergency Response Management applications.-   Contact Tracing
-   Emergency Outreach
-   Employee Health Screening
-   Employee Readiness Core
-   Employee Travel Safety
-   Health and Safety Testing
-   Safe Workplace Dashboard
-   Vaccination Status
-   Workplace PPE Inventory Management
-   Workplace Core

Health and safety user records are also created for visitors who are invited through the Employee Readiness Core app.

</td></tr><tr><td>

Recalculate audiences for requirements

</td><td>

Runs every hour to recalculate audiences for health and safety requirements when users are added or removed from the audience. This job handles when their status would be changed to or from **Not Required** due to their status in or out of an audience.

</td></tr><tr><td>

Recalculate All Employee Health and Safety Requirement Status'

</td><td>

A scheduled job that can be run as a one-time fix script once your organization provides users with their relevant roles and upgrades to the latest version of Employee Readiness Core. This job recalculates each users' Healthy and Safety requirement statuses based on the \[sn\_imt\_core.use\_not\_required\] property and their requirements.

</td></tr><tr><td>

Ensure Approval Portal Manager

</td><td>

Runs weekly by default or may be manually executed to ensure managers are assigned or unassigned the Approval Portal manager \[sn\_imt\_core.approval\_portal\_manager\] role based on whether they are currently a manager and one of three Approval Portal-related properties are active.-   Allow managers the ability to update health test results \[sn\_imt\_health\_test.allow\_managers\_ability\_to\_update\_test\_result\_records\]
-   Allow managers the ability to update vaccine response records \[sn\_imt\_vaccine.allow\_managers\_ability\_to\_update\_vaccine\_response\_records\]
-   Allow managers the ability to update vaccine exemption requests \[sn\_imt\_vaccine.allow\_managers\_ability\_to\_update\_vaccine\_exemption\_records\]

 Each property provides managers access to the Approval Portal, however, managers are able to see and interact with only records associated with the activated property. Activating multiple properties grants additional capabilities to the reviewing managers.

</td></tr></tbody>
</table>