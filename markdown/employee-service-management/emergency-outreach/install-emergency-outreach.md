---
title: Install Emergency Outreach
description: You can install Emergency Outreach if you have the admin role.You can install Employee Readiness Surveys if you have the admin role. Installing Employee Readiness Surveys adds notification options to the Emergency Outreach app. A default health readiness survey is provided as an example.Several types of components are installed with Emergency Outreach, including tables and user roles.
locale: en-US
release: zurich
product: Emergency Outreach
classification: emergency-outreach
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Emergency Outreach, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Install Emergency Outreach

You can install Emergency Outreach if you have the admin role.

## Before you begin

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
</table>## About this task

After you install Emergency Outreach, no additional administration configuration is required. Optionally, you can configure notifications and response messages.

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for `Emergency Outreach`.

3.  Click **install**.

    The Application installation dialog box opens.

4.  Load the demo data by selecting the **Load demo data**check box.

    For information about how to install or reinstall demo data after the initial installation, see the [Work around to install demo data if application is already installed \[KB0722909\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0722909) article in the Now Support Knowledge Base.

5.  Click **install**.

6.  When the installation is complete, click **Close**.


## Result

Emergency Outreach is installed on your instance.

## What to do next

Optionally install Employee Readiness Surveys to use with Emergency Outreach. The Employee Readiness Surveys app enables you to evaluate the readiness of your employees to return to the workplace using Emergency Outreach notifications.

**Parent Topic:**[Emergency Outreach](../concept/emergency-outreach.md)

## Install Employee Readiness Surveys to use with Emergency Outreach

You can install Employee Readiness Surveys if you have the admin role. Installing Employee Readiness Surveys adds notification options to the Emergency Outreach app. A default health readiness survey is provided as an example.

### Before you begin

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
</table>If you've subscribed to the Safe Workplace suite and you already have some of the apps installed, refer to the following order of installation for the remaining apps.

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

### About this task

The Send Outreach form in Emergency Outreach has an option to send a survey instead of a health status request. Users with the sn\_imt\_checkin.checkin\_admin role become owners of the example health readiness survey.

### Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for `Employee Readiness Surveys`.

3.  Select **install**.

    The Application installation dialog box opens.

4.  Load the demo data by selecting the **Load demo data**check box.

    For information about how to install or reinstall demo data after the initial installation, see the [Work around to install demo data if application is already installed \[KB0722909\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0722909) article in the Now Support Knowledge Base.

5.  Select **install**.

6.  When the installation is complete, select **Close**.


### Result

Employee Readiness Surveys is installed on your instance. Use it by navigating to the Emergency Outreach app.

## Components installed with Emergency Outreach

Several types of components are installed with Emergency Outreach, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Emergency Outreach admin\[sn\_imt\_checkin.checkin\_admin\]

</td><td>

Can create a new Emergency Outreach notification and view the responses received from the user. Can create and manage Safe Workplace audiences. The Employee Readiness Core app must be installed.

</td><td>

survey\_creator

</td></tr></tbody>
</table>### Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Emergency Outreach \[sn\_imt\_checkin\_employee\_check\_in\]

</td><td>

Define the audience and the notification content to send to the users.

</td></tr><tr><td>

Outreach Acknowledgements \[sn\_imt\_checkin\_check\_in\_acknowledgement\]

</td><td>

Define the outreach acknowledgement record and the response received from a user.

</td></tr><tr><td>

Response Options\[sn\_imt\_checkin\_response\_option\]

</td><td>

Define the responses that appear in the notification message to users.

</td></tr><tr><td>

Emergency Outreach Channels\[sn\_imt\_checkin\_channels\]

</td><td>

Create notification channels using a script or subflow, such as for Slack or Facebook collaboration platforms.

</td></tr><tr><td>

Health Verification Acknowledgements\[sn\_imt\_checkin\_health\_verification\_acknowledgement\]

</td><td>

Define the daily health verification acknowledgement record and the response received from a user.The table is available for use only if you also subscribe to ServiceNow® Employee Health Screening. The data of this table is displayed in the Health Verification Acknowledgements related list when you send the Daily Health Verification outreach notification to employees.

</td></tr><tr><td>

Emergency Outreach Notification Channels\[sn\_imt\_checkin\_m2m\_channel\_employee\_check\_in\]

</td><td>

Contains records connecting Emergency Outreach notifications with the notification channel used when it was sent.

</td></tr><tr><td>

Outreach Sysauto Script\[sn\_imt\_checkin\_outreach\_sysauto\_script\]

</td><td>

Contains scheduled jobs for sending outreach notifications, such as for daily contact logs from the Contact Tracing app.

</td></tr><tr><td>

Survey Instances\[sn\_imt\_m2m\_asmt\_assessment\_instance\_checkin\]

</td><td>

Associates outreach survey records with survey instances for better reporting.

</td></tr><tr><td>

Response Criteria\[sn\_imt\_checkin\_response\_criteria\]

</td><td>

Set of questions that determine whether the response script runs when an employee completes a survey based on the employee's answers to those questions.

</td></tr><tr><td>

Response Script\[sn\_imt\_checkin\_response\_script\]

</td><td>

List of all response scripts. Response scripts are used to automatically take actions based on employee responses to survey questions.

</td></tr><tr><td>

View Outreach Instance Logs\[sn\_imt\_checkin\_employee\_check\_in\_log\]

</td><td>

List of outreach surveys with information about their creation and the status of their survey instances.

</td></tr></tbody>
</table>