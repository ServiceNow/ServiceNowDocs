---
title: Integrating ServiceNow with Microsoft Teams and Microsoft 365
description: Set up your ServiceNow instance to integrate Microsoft Teams or Microsoft 365 applications.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Integrating ServiceNow with Microsoft Teams and Microsoft 365

Set up your ServiceNow instance to integrate Microsoft Teams or Microsoft 365 applications.

**Important:**

-   From [IT Service Management for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/14eb9da8c3f310102986a81c8640dd08/2.6.7?referer=%2Fstore%2Fproduct%2F9389b69edbb8e810d27e581adc9619ca) \(version 2.6.7\), ServiceNow for Microsoft Teams is upgraded to ServiceNow for Microsoft 365.
-   From [HR Service Delivery for Microsoft 365](https://store.servicenow.com/sn_appstore_store.do#!/store/application/23364660c3b31010aab55b79c840ddc2/3.3.6?referer=%2Fstore%2Fproduct%2F9389b69edbb8e810d27e581adc9619ca) \(version 3.3.6\), ServiceNow for Microsoft Teams is upgraded to ServiceNow for Microsoft 365.

For upgrading existing Microsoft Teams capabilities to Microsoft 365 applications, see [Integrating ServiceNow with Microsoft 365 applications for Employee Experience](setup-sn-ms-teams-ms365.md).

To connect your ServiceNow instance to your Microsoft Office 365 tenant and to authorize applications, you must have both the external\_app\_install\_admin role and the application administrator role in Microsoft Office 365. For more information on Microsoft roles, see the Microsoft documentation on [Azure AD built-in roles](https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference#available-roles).

Azure Active Directory \(Azure AD\) organizes objects like users and apps into groups called tenants.

Self-configured apps \(previously referred to as single-tenant\) are available only in the tenant they were registered in, also known as their home tenant. Here, a single Microsoft Teams tenant is connected to multiple ServiceNow instances.

Pre-published apps \(previously referred to as multi-tenant\) are available to users in both their home tenants and other tenants. Here, a single Microsoft Teams tenant is connected to a single ServiceNow instance.

<table id="table_xbv_qmm_ktb"><thead><tr><th>

Pre-published app

</th><th>

Self-configured app

</th></tr></thead><tbody><tr><td>

-   The relevant Microsoft Azure app is provided by ServiceNow so you don’t need to create your own.

No need to create an app in the Microsoft Azure portal. Moderate Microsoft Azure expertise is required.

-   Once the administrator consents, ServiceNow automatically updates the Microsoft Azure app.

</td><td>

-   You must create your own app in the Microsoft Azure portal.

Requires proficiency in Microsoft Azure portal.

-   Own and control the Microsoft Azure app.

</td></tr></tbody>
</table>When you consent to the app to use the required permissions, a Service Principal \(SP\) is created representing the Microsoft Azure app. For more information about the admin consent, see [Understand user and admin consent](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-convert-app-to-be-multi-tenant#understand-user-and-admin-consent).

In a self-configured app configuration, you must create an app in Microsoft Azure portal and use the app ID and the client ID values to connect to your ServiceNow instance.

## When to use Pre-published app or Self-configured app configuration

Use the self-configured app or pre-published app configuration based on the following conditions:

-   In case of a single Microsoft tenant to multiple ServiceNow® instances integration, use the self-configured configuration setup.
-   In case of a single Microsoft tenant to single ServiceNow® instance integration, it is recommend to use the pre-published configuration setup. However, you can still use the self-configured configuration setup.
-   In case of a single ServiceNow® instance to multiple Microsoft tenant integration, use the Self-configured configuration setup.

-   **[Plan your installation](plan-installation-ms-teams.md)**  
Identify the need and plan your installation for ServiceNow® for Microsoft Teams.
-   **[Setting up the ServiceNow instance for Microsoft Teams integration](setup-tenants.md)**  
Set up your ServiceNow® instance for the Microsoft Teams integrations.

**Parent Topic:**[Configure integrations for Microsoft Teams and Microsoft 365](integrations-all-snteams.md)

**Related topics**  


[Integrating ServiceNow with Microsoft Teams for GCC-H or DoD](setup-sn-ms-teams-gcch.md)

[Integrating ServiceNow with Microsoft 365 applications for Employee Experience](setup-sn-ms-teams-ms365.md)

