---
title: Install the Task Intelligence for Customer Service application
description: You can install the Task Intelligence for Customer Service application \(com.snc.csm\_ml\_task\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence. JW - No demo data per dev team.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Task Intelligence for Customer Service, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Install the Task Intelligence for Customer Service application

You can install the Task Intelligence for Customer Service application \(com.snc.csm\_ml\_task\) if you have the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Task Intelligence for Customer Service](https://store.servicenow.com/sn_appstore_store.do#!/store/application/892158dc7deec910f877d4d6a46b1d5f) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   The minimum version of the workspace required to support Task Intelligence for Customer Service application is CSM and FSM Configurable Workspace Foundation \(sn\_cwf\_wrkspc\): 24.2.1.
-   To enhance ML functionality, we need to set up three Access Control Lists \(ACLs\) within the Customer Service application. These ACLs are essential for granting the platform\_ml\_read role the necessary read access to the sn\_customerservice\_case table and its associated fields. For more information, see [KB1705485](https://support.servicenow.com/kb_knowledge.do?sys_id=4d3e9b1f93d15610f2167de86cba1061&sysparm_record_target=kb_knowledge&sysparm_record_row=1&sysparm_record_rows=228&sysparm_record_list=short_descriptionSTARTSWITHACL%5EORDERBYDESCnumber)


Role required: ti\_admin

## About this task

The following items are installed with Task Intelligence for Customer Service:

-   Store applications: Task Intelligence for Customer Service
-   Roles
-   Tables
-   Properties
-   Flows
-   Scheduled jobs

For more information, see [Components installed with Task Intelligence for Customer Service](../reference/case-categorization-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Task Intelligence for Customer Service application \(com.snc.csm\_ml\_task\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


