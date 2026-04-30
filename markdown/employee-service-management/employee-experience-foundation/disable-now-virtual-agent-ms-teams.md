---
title: Disable the Now Virtual Agent
description: Disable the Now Virtual Agent app to avoid duplicate notifications from Microsoft Teams when you install and integrate ServiceNow for Microsoft Teams with your ServiceNow instance.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Disable the Now Virtual Agent

Disable the Now Virtual Agent app to avoid duplicate notifications from Microsoft Teams when you install and integrate ServiceNow for Microsoft Teams with your ServiceNow instance.

## Before you begin

**Note:** Your employees will not see or use the Now Virtual Agent app.

Role required: Microsoft Teams admin

## About this task

ServiceNow has two apps available for Microsoft Teams:

-   Now Virtual Agent

    This app displays the Virtual Agent within Microsoft Teams, has been available within Microsoft Teams app since 2019.

-   ServiceNow for Microsoft Teams

    ServiceNow for Microsoft Teams is a new app that provides a broader employee experience, including and expanding beyond Virtual Agent, with an embedded portal experience called **Employee Center**, and the ability for agents to reach out to employees in Microsoft Teams to quickly resolve open tickets.


Since the same Bot \(Virtual Agent\) is shared in both apps, blocking the Now Virtual Agent app also results in the same bot ID being blocked for the ServiceNow for Microsoft Teams app, making the Virtual Agent unusable in the ServiceNow for Microsoft Teams app. To work around this issue, it is necessary to make sure that the Now Virtual Agent app is in the list of allowed apps.

You must first block the Now Virtual Agent app, so it stops showing up for employees and then add the app to the allowed list. After this configuration, your employees will not see or use the Now Virtual Agent app, but will be able to use Virtual Agent within the ServiceNow for Microsoft Teams app.

**Note:** It may take up to 24 hours for the changes to be propagated.

## Procedure

1.  Log in to the Microsoft Teams admin portal.

2.  Navigate to **Teams apps** &gt; **Manage apps**.

3.  In the search field, enter `Now Virtual Agent`.

4.  Select the **Now Virtual Agent** app.

5.  Select **Actions**, then select **Block app**.

    ![Now Virtual Agent app in Microsoft Teams.](../images/block-now-virtual-agent-ms-teams.png)


**Parent Topic:**[Setup for integrating pre-published apps with Microsoft Teams for Employee Experience](../concept/c_employee_ex_tnt.md)

