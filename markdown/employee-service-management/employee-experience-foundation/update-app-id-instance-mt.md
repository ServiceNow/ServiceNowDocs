---
title: Update the app ID in the ServiceNow instance
description: Update the ServiceNow for Teams app ID from the Microsoft Teams admin center in your ServiceNow instance.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Update the app ID in the ServiceNow instance

Update the ServiceNow for Teams app ID from the Microsoft Teams admin center in your ServiceNow instance.

## Before you begin

Role required: admin

## Procedure

1.  Log in to the Microsoft Teams admin center.

2.  Navigate to **Teams apps** &gt; **Manage apps**.

3.  Select the **ServiceNow for Teams** app.

4.  Copy the App ID value.

    ![ServiceNow for Teams app ID value](../images/sn-ms-teams-app-id-value.png)

5.  In your ServiceNow instance, search for `sys_properties.list`.

6.  Select the `sn_now_azure.teams_installed_app_id` property.

    ![Edit the entry](../images/edit-record.png)

7.  Update the App ID value, then select **Update**.

    ![Update the app id value](../images/update-app-id-value.png)


**Parent Topic:**[Setup for integrating pre-published apps with Microsoft Teams for Employee Experience](../concept/c_employee_ex_tnt.md)

