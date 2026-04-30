---
title: Set up Emergency Self Report
description: To set up Emergency Self Report, install the application. Then configure user access, a dedicated knowledge base, and system properties.You can install Emergency Self Report if you have the admin role.Several types of components are installed with Emergency Self Report, including tables and user roles.Configure Emergency Self Report to align with your business needs.
locale: en-US
release: zurich
product: Emergency Self Report
classification: emergency-self-report
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Emergency Self Report, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Set up Emergency Self Report

To set up Emergency Self Report, install the application. Then configure user access, a dedicated knowledge base, and system properties.

**Parent Topic:**[Emergency Self Report](../concept/emergency-self-report.md)

## Install Emergency Self Report

You can install Emergency Self Report if you have the admin role.

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

### Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for `Emergency Self Report`.

3.  Click **Install**.

    The Application installation dialog box opens.

4.  Load the demo data by selecting the **Load demo data** check box.

    For information about how to install or reinstall demo data after the initial installation, see the [Work around to install demo data if application is already installed \[KB0722909\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0722909) article in the Now Support Knowledge Base.

5.  Click **Install**.

6.  When the installation is complete, click **Close**.


### Result

The Emergency Self Report application is installed on your instance.

## Components installed with Emergency Self Report

Several types of components are installed with Emergency Self Report, including tables and user roles.

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

Self report user \[sn\_imt\_quarantine.crisis\_task\_user\]

</td><td>

Access the Emergency Self Report Dashboard to report health status.

</td><td>

notify\_view

</td></tr><tr><td>

Crisis task users\[sn\_imt\_quarantine.humanResourceTeam\]

</td><td>

View and manage HR tasks, submit updates for other users, and import crisis tasks.

 Also grant the self report user role.

</td><td>

notify\_view

</td></tr></tbody>
</table>### Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Crisis Task\[sn\_imt\_quarantine\_crisis\_task\]

</td><td>

Contains all self report crisis tasks, including HR crisis tasks.

</td></tr><tr><td>

Crisis Task Status Log\[sn\_imt\_quarantine\_crisis\_task\_status\_log\]

</td><td>

Contains a history of all reported health statuses for each user. This table is only populated when the **sn\_imt\_quarantine.enable.health.status.log** property is set to `true`.

</td></tr><tr><td>

Bulk Import Crisis Tasks\[sn\_imt\_quarantine\_bulk\_load\_crisis\_task\]

</td><td>

The Import Set table for importing reported health statuses from an Excel spreadsheet to create crisis tasks in bulk. When you load data from the Excel file into the application, the imported records are first saved in this import set table. After you run the transform or execute the scheduled import script, the records are copied to the Crisis Task table.

</td></tr></tbody>
</table>## Configure Emergency Self Report

Configure Emergency Self Report to align with your business needs.

### Before you begin

Role required: admin

### About this task

Complete the following configurations as needed.

-   Grant app access to the appropriate response team members.
-   Specify custom system messages to help your users and response team members.
-   Set system properties to control how you use Emergency Self Report.
-   Configure user health status choices.
-   Create a dedicated knowledge base and add it to your Service Portal.

### Procedure

1.  Add the default application user roles to appropriate groups.

    The application provides the following default roles in the sys\_user\_role table:

    -   **sn\_imt\_quarantine.crisis\_task\_user**

        Enables group members or individuals to submit a health alert for themselves. Managers can also submit and monitor alerts for their direct reports.

    -   **sn\_imt\_quarantine.humanResourceTeam**

        Enables group members, such as HR or Global Security team members, to manage the reported health alerts.

    For information about how to assign roles to groups, see [Roles](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

2.  Navigate to **Emergency Self Report** &gt; **UI Configuration**, set the desired message values, and then click **Update**.

<table id="table_bj4_pmr_llb"><thead><tr><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_imt\_quarantine.crisisSubmitMessage

</td><td>

Configure the message that is displayed to users after they submit a health status.![Sample information message.](../image/emergency-self-report-message-example.png "Example confirmation message")

</td></tr><tr><td>

sn\_imt\_quarantine.openTasksInfoMessage

</td><td>

Configure a tooltip for managers who are viewing open tasks for their direct reports.![Message for My direct reports' open tasks.](../image/emergency-self-report-direct-report-msg.png "Example message for open tasks")

</td></tr></tbody>
</table>3.  Navigate to **Emergency Self Report** &gt; **Emergency Self Report Properties**, set the desired property values, and then click **Update**.

<table id="table_mzp_gjr_1lb"><thead><tr><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_imt\_quarantine.enable.health.status.log

</td><td>

When this property is set to `true`, a new record is created in the Crisis Task Status Log table \[sn\_imt\_quarantine\_crisis\_task\_status\_log\] every time that a user health status update is submitted. Crisis task records have a Crisis Task Status Logs related list that shows all health status updates for that crisis task. When this property is set to `false`, the Crisis Task Status Log table is not populated.The default value is `false`.

</td></tr><tr><td>

sn\_imt\_quarantine.data.retention.period

</td><td>

Sets the number of days that records are stored in the Crisis Task Status Log table \[sn\_imt\_quarantine\_crisis\_task\_status\_log\] before they are deleted.The default value is 30 days.

</td></tr><tr><td>

sn\_imt\_quarantine.fetchTaskQuery

</td><td>

Determines the data that is visible in the Emergency Self Report dashboard in the My direct reports' open tasks section.

 The default value is to show only P1 and P2 requests, incidents for the last month, and those assigned to the manager's direct reports:

 ```
sys_created_on>=javascript:gs.beginningOfLastMonth()
^active=true^assigned_to.managerDYNAMIC90d1921e5f510100a9ad2572f2b477fe
^sys_class_name=incident^ORsys_class_name=sc_task
^ORsys_class_name=sc_request^priorityIN1,2
```

</td></tr><tr><td>

sn\_imt\_quarantine.healthStatusChangeTaskBehavior

</td><td>

Sets the behavior of crisis tasks for users who update their health status after their most recent crisis task is closed. When the value is `update`, the user’s most recent HR crisis task is reopened and their health status is updated with their new reported status. When the value is `create`, a new HR crisis task is created if an open one doesn’t already exist for the user's newly reported status.

 The default value is `update`.

</td></tr><tr><td>

sn\_imt\_quarantine.healthStatusesToTriggerTaskReopen

</td><td>

Sets the health statuses that reopen tasks or create new tasks if reported by a user after their most recent crisis task is closed. By default, the statuses that reopen or create new tasks are **In quarantine** and **Reporting symptoms**.

</td></tr><tr><td>

sn\_imt\_quarantine.hrGroup

</td><td>

Members of the global response team, who will have access to your team's user records. You can add a role to a group to act as a global response team or you can add the role directly to the users.

</td></tr><tr><td>

sn\_imt\_quarantine.MaxOrgLevelLimit

</td><td>

Number of levels in your organization structure. For example, If you have CEO, VP, Director, Manager, and Individual Contributors, you have five levels in your organization structure.

</td></tr><tr><td>

sn\_imt\_quarantine.outSickDuration

</td><td>

The time frame \(in days\) after which users are safe to return to work if sick.The default value is 20 days.

</td></tr><tr><td>

sn\_imt\_quarantine.quarantineDuration

</td><td>

The time frame \(in days\) after which users are safe to return to work if self-quarantined.The default value is 14 days.

</td></tr></tbody>
</table>4.  Configure the check-in choices that the user can select.

    1.  Navigate to **System Definition** &gt; **Choice Lists**.

    2.  Set a search filter with the following conditions:

        -   **\[Table\] \[is\] \[sn\_imt\_quarantine\_crisis\_task\]**
        -   **\[Element\] \[is\] \[request\_type\]**
    3.  Change the label or value for choices in the list, or add new values.

    4.  Click **Update**.

5.  Configure knowledge articles about the emergency event.

    For example, provide local regulations, organization policies, and how-to information.

    1.  Create a knowledge base to contain the application's articles.

    2.  Navigate to **Service Portal** &gt; **Pages**.

    3.  Search for ID `self_report_dashboard` and click the record.

    4.  Click the **Emergency Self Report - Container 2** link.

    5.  Under Column 2, click **Instance of Simple List**.

    6.  On the Table &amp; Filter tab, name the knowledge base by setting the following filter condition: **\[Knowledge Base\] \[is\] \[&lt;name&gt;\]**.

    7.  Associate application articles with the application knowledge base.


