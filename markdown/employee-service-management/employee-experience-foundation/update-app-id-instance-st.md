---
title: Update the app ID in the ServiceNow instance
description: Update the ServiceNow for Teams app ID from the Microsoft Teams admin center in your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/update-app-id-instance-st.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
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

    \[Omitted image "sn-ms-teams-app-id-value.png"\] Alt text: ServiceNow for Teams app ID value

5.  In your ServiceNow instance, search for `sys_properties.list`.

6.  Select the `sn_now_azure.teams_installed_app_id` property.

    \[Omitted image "edit-record.png"\] Alt text: Edit the entry

7.  Update the App ID value, then select **Update**.

    \[Omitted image "update-app-id-value.png"\] Alt text: Update the app id value


**Parent Topic:**[Setup for integrating self-configured apps with Microsoft Teams for Employee Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/c_employee_ex_s_tnt.md)

