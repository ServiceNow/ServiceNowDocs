---
title: Connect the ServiceNow instance to your Microsoft Teams tenant
description: Connect your ServiceNow instance to your Microsoft Teams tenant to enable the users to create their requests from within Microsoft Teams.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrate Notify connector pre-published app with Microsoft Teams, Integration for Agent Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Connect the ServiceNow instance to your Microsoft Teams tenant

Connect your ServiceNow instance to your Microsoft Teams tenant to enable the users to create their requests from within Microsoft Teams.

## Before you begin

Role required: External admin \(external\_app\_install\_admin\)

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Install Azure apps**.

2.  Click **Connect** to install Microsoft Teams in your instance.

    ![Install Azure apps.](../image/install-azure-apps-02.png)

3.  Select the **Consent on behalf of your organization** option to provide the consent for all your users, and click **Accept** button to provide the admin consent.

    ![Admin consent for the app.](../../sn-teams/images/sso-activity-notification-admin-consent.png)

    SSO and Activity Notification is one of the apps to verify the users and connect the Microsoft tenant to the ServiceNow instance. Provide the desired Microsoft tenant details to connect to the ServiceNow instance.

    Select the **Consent on behalf of your organization** option to provide the consent for all your users.

    **Note:** All the users must also accept the permissions, not accepting the permissions result in not being able to use the ServiceNow integrations with Microsoft Teams.


**Parent Topic:**[Integrate Notify connector pre-published app with Microsoft Teams](../concept/setup-notify-ms-teams-multi-tenant.md)

