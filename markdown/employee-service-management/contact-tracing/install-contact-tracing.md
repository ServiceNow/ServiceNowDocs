---
title: Install Contact Tracing
description: You can install Contact Tracing if you have the admin role.Several types of components are installed with Contact Tracing, including tables and user roles.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Install Contact Tracing

You can install Contact Tracing if you have the admin role.

## Before you begin

The following applications are also installed when you install the Contact Tracing application:

-   ServiceNow® Emergency Exposure Management
-   ServiceNow® Employee Readiness Core

You can also install and activate the following applications to use all Contact Tracing features:

-   ServiceNow® Emergency Outreach
-   ServiceNow® Emergency Self Report
-   ServiceNow® Safe Workplace Dashboard

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
</table>The Contact Tracing application requires the ServiceNow® Performance Analytics - Premium application. If you're not already subscribed to Performance Analytics - Premium, you must install it before installing Contact Tracing.

If you've subscribed to the Safe Workplace suite and you already have some of the apps installed, refer to the following order of installation for the remaining apps.

-   Emergency Outreach \(sn\_imt\_checkin\)
-   Employee Health Screening \(sn\_imt\_monitoring\)
-   Workplace PPE Inventory Management \(sn\_imt\_ppe\)
-   Employee Readiness Surveys \(sn\_imt\_readiness\)
-   COVID-19 Global Health Data Set \(sn\_imt\_c19datafeed\)
-   Contact Tracing \(sn\_imt\_tracing\)
-   Emergency Self Report \(sn\_imt\_quarantine\)
-   Workplace Core \(sn\_wsd\_core\)
-   Safe Workplace Dashboard \(sn\_imt\_dashboard\)
-   Emergency Response Management for Now Mobile \(sn\_imt\_mobile\)
-   Employee Travel Safety \(sn\_imt\_travel\)
-   Health and Safety Testing \(sn\_imt\_health\_test\)
-   Vaccination Status \(sn\_imt\_vaccine\)

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for `Contact Tracing`.

3.  Click **Install**.

4.  In the Application installation dialog box, click **Install**.

5.  When the installation is complete, click **Close**.

6.  Control access to the application by creating a group and assigning roles to the group or individual users.

    For more information, see [Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).


**Parent Topic:**[Contact Tracing](../concept/contact-tracing.md)

## Components installed with Contact Tracing

Several types of components are installed with Contact Tracing, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Contact Tracing admin\[sn\_imt\_tracing.admin\]

</td><td>

Application-specific admin for Contact Tracing and has administrative privileges.

</td><td>

-   sn\_imt\_tracing.case\_manager
-   sn\_imt\_tracing.badge\_admin
-   sn\_imt\_tracing.contact\_tracing\_user

</td></tr><tr><td>

Contact tracing user\[sn\_imt\_tracing.contact\_tracing\_user\]

</td><td>

Can submit daily contacts log and privacy consent preference, and access contact tracing cases when added to the case watch list.

</td><td>

-   sn\_imt\_checkin.dailylog\_user
-   sn\_imt\_tracing.privacy\_consent\_user

</td></tr><tr><td>

Badge admin\[sn\_imt\_tracing.badge\_admin\]

</td><td>

Can create, update, delete, and import badge data.

</td><td>

sn\_imt\_tracing.badge\_manager

</td></tr><tr><td>

Badge manager\[sn\_imt\_tracing.badge\_manager\]

</td><td>

Can create, update, and import badge data.

</td><td>

-   sn\_imt\_tracing.badge\_reader
-   import\_admin

</td></tr><tr><td>

Badge reader\[sn\_imt\_tracing.badge\_reader\]

</td><td>

Can view badge access register data.

</td><td>

None

</td></tr><tr><td>

Case manager\[sn\_imt\_tracing.case\_manager\]

</td><td>

Can create and manage outreach cases, run diagnostic requests to identify potentially exposed contacts. Can create, assign, and supervise tasks.

</td><td>

-   sn\_imt\_diagnosis.diagnostics\_admin
-   sn\_imt\_tracing.contact\_tracer

</td></tr><tr><td>

Contact tracer\[sn\_imt\_tracing.contact\_tracer\]

</td><td>

Can work on assigned case tasks to follow up on the health status of potentially exposed contacts, as per the predefined instructions.

</td><td>

-   task\_editor
-   survey\_reader

</td></tr><tr><td>

Privacy consent user\[sn\_imt\_tracing.privacy\_consent\_user\]

</td><td>

Can submit and update the user policy consent for themselves.

</td><td>

None

</td></tr><tr><td>

Tracing user\[sn\_imt\_tracing.dailylog\_user\]

</td><td>

Can fill in the daily contacts log to submit a list of users that they interacted with at the workplace.

</td><td>

None

</td></tr><tr><td>

Wi-Fi admin\[sn\_imt\_tracing.wifi\_admin\]

</td><td>

Can create, update, delete, and import Wi-Fi access logs.

</td><td>

sn\_imt\_tracing.wifi\_manager

</td></tr><tr><td>

Wi-Fi manager\[sn\_imt\_tracing.wifi\_manager\]

</td><td>

Can create, update, and import Wi-Fi access Logs.

</td><td>

-   import\_admin
-   sn\_imt\_tracing.wifi\_reader

</td></tr><tr><td>

Wi-Fi reader\[sn\_imt\_tracing.wifi\_reader\]

</td><td>

Can view Wi-Fi access logs.

</td><td>

None

</td></tr><tr><td>

Wearable admin\[sn\_imt\_tracing.wearable\_admin\]

</td><td>

Can create, update, delete, and import handheld or wearable devices access logs.

</td><td>

sn\_imt\_tracing.wearable\_manager

</td></tr><tr><td>

Wearable manager\[sn\_imt\_tracing.wearable\_manager\]

</td><td>

Can create, update, and import handheld or wearable devices access logs.

</td><td>

sn\_imt\_tracing.wearable\_reader

</td></tr><tr><td>

Wearable reader\[sn\_imt\_tracing.wearable\_reader\]

</td><td>

Can view handheld or wearable device access logs.

</td><td>

None

</td></tr></tbody>
</table>### Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data Retention Job For Contact Tracing

</td><td>

Deletes contact tracing data after the retention period is over from the last updated date for the records related to contact tracing. The data includes badge swipes, Wi-Fi access register data,employee daily contact logs, daily log notes, and daily log acknowledgements, cases and associated case tasks, exposed contacts, diagnostic requests, diagnostic jobs, and workplace reservations.

**Note:** The data retention policy doesn't apply to user privacy consent data.

</td></tr><tr><td>

Devvio

 Integration

</td><td>

Runs daily at 00:00:00 instance time and populates the Devvio Users Risk Report for organizations that use Devvio wearables and the DevvTrace platform.

</td></tr><tr><td>

Load Mist Systems

</td><td>

Runs daily at 00:00:00 and populates the sites for the organizations that use Wi-Fi logs from Mist Systems.

</td></tr></tbody>
</table>### Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Badge Access Register\[sn\_imt\_tracing\_badge\_access\_register\]

</td><td>

Badge swipe records of all users.

</td></tr><tr><td>

Badge Access Register Stage\[sn\_imt\_tracing\_badge\_access\_register\_stage\]

</td><td>

The Import Set table for importing the badge access data from an Excel spreadsheet. When you load data from the Excel file into the application, the imported records are first saved in this import set table. After you run the transform, or execute the scheduled import script, the records are copied from this table to the Badge Access Register table.

</td></tr><tr><td>

Badge Reader\[sn\_imt\_tracing\_badge\_reader\]

</td><td>

User ID badge reading devices installed in a location.

</td></tr><tr><td>

User Badge\[sn\_imt\_tracing\_user\_badge\]

</td><td>

Users and their ID badge information.

</td></tr><tr><td>

Case\[sn\_imt\_tracing\_case\]

</td><td>

Outreach cases for affected users to help minimize potential exposure to others.

</td></tr><tr><td>

Case Task\[sn\_imt\_tracing\_case\_task\]

</td><td>

Case tasks in outreach cases to follow up with the potentially exposed users to track health status.

</td></tr><tr><td>

Exposed Contacts\[sn\_imt\_tracing\_exposed\_contact\]

</td><td>

Potentially exposed users that might have interacted with a user who has been diagnosed with an infectious disease. The records in this table are stored when the case manager adds all impacted users to the case. Impacted users are identified through the diagnostic request using multiple data input.

</td></tr><tr><td>

Daily Contact Logs\[sn\_imt\_tracing\_daily\_contact\_log\]

</td><td>

The names of users submitted using daily contact logs by another user.

</td></tr><tr><td>

Daily Log Acknowledgements\[sn\_imt\_tracing\_daily\_log\_acknowledgement\]

</td><td>

Acknowledgement status to identify which users have responded to the notification to submit the daily contacts log.

</td></tr><tr><td>

Daily Log Notes\[sn\_imt\_tracing\_daily\_log\_note\]

</td><td>

Names of users outside of the organization, such as visitors and contractors submitted using daily contact logs by another user.

</td></tr><tr><td>

Devvio Users Risk Report

 \[sn\_imt\_tracing\_devvio\_users\_risk\_report\]

</td><td>

Devvio users and their risk scores captured by Devvio wearables. The records in this table are imported from the DevvTrace platform and updated daily.

</td></tr><tr><td>

Location Privacy Configuration\[sn\_imt\_tracing\_location\_privacy\_config\]

</td><td>

Configuration for the location-based privacy policy, such as the privacy statement for a location and whether a particular location requires privacy consent.

</td></tr><tr><td>

Privacy Consent Template\[sn\_imt\_tracing\_privacy\_consent\_template\]

</td><td>

Template to store the privacy statement for a location and is used in the location privacy configuration.

</td></tr><tr><td>

User Privacy Notice and Consents\[sn\_imt\_tracing\_user\_privacy\_consent\]

</td><td>

Responses of users to the privacy consent.

</td></tr><tr><td>

Sites\[sn\_imt\_tracing\_site\]

</td><td>

Sites in the building of your organization. Each floor is considered as a site. Each site can be further divided into zones. Each zone can have multiple Wi-Fi routers installed, called as Wi-Fi access points.

</td></tr><tr><td>

Wi-Fi Diagnostic Preferences\[sn\_imt\_tracing\_wifi\_diagnostic\_preference\]

</td><td>

Type of Wi-Fi data used for contact tracing. For example, you might have real-time data for a location collected through the integration with a network system, such as Mist Systems. For other locations, you might manually upload data from a spreadsheet.

</td></tr><tr><td>

Wi-Fi Access Register\[sn\_imt\_tracing\_wifi\_access\_register\]

</td><td>

Entry and exit time records of users who have connected to the office Wi-Fi access pointsor using the BLE enabled devices.

</td></tr><tr><td>

Wearable Access Register\[sn\_imt\_tracing\_wearable\_access\_register\]

</td><td>

User interaction records captured using the proximity sensing data via their handheld or wearable devices when they are in the close proximity for more than the permissible time.

</td></tr></tbody>
</table>