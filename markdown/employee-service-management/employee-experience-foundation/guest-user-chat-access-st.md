---
title: Request-based chat access for a guest user
description: Request-based self-configured app chat access enables a guest user to start and import chats in a single ServiceNow for Microsoft Teams instance.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Request-based chat access for a guest user

Request-based self-configured app chat access enables a guest user to start and import chats in a single ServiceNow® for Microsoft Teams instance.

Guest sharing is enabled by default in Microsoft Entra ID and in ServiceNow for Microsoft Teams. As a result, users can invite guests to teams and sites, and share files with guests without having to request assistance from the IT department.

Guests can take the following actions:

-   Initiate a chat with people from outside their organization.
-   Import their chat conversations with people from outside their organization.

For information about configuring access for guest users, see [Guest access in Microsoft Teams](https://docs.microsoft.com/en-us/microsoftteams/guest-access).

Guest access configuration is applicable to the following tables in both IT Service Management integration with Microsoft Teams and HR Service Delivery integration with Microsoft Teams applications:

-   HR Core task \(sn\_hr\_core\_task\)
-   HR Life events Case \(sn\_hr\_le\_case\)
-   HR Core case \(sn\_hr\_core\_case\)
-   Request Item \(sc\_req\_item\)
-   Task \(sc\_task\)
-   Incident \(incident\)
-   Request \(sc\_request\)
-   Change request \(change\_request\)

The ServiceNow system admin can extend guest access to other tables.

-   **[Authenticate guest users to initiate and import chat from Microsoft Teams](../task/authenticate-guest-start-import-chat.md)**  
Assign permissions to guest users to initiate and import chat conversations with employees from Microsoft Teams to a ServiceNow® instance for a self-configured app.
-   **[Enable authentication of guest users](../task/update-verify-app-registry-guest.md)**  
Verify and update application registry values to authenticate guest users in the Microsoft Teams application to start and import chats for a self-configured app.
-   **[Enable chat access for guest users](../task/enable-guest-chat-access-st.md)**  
Enable chat access for a guest user while configuring ServiceNow® for Microsoft Teams settings for a self-configured app.

**Parent Topic:**[Setup for integrating self-configured apps with Microsoft Teams for Employee Experience](c_employee_ex_s_tnt.md)

