---
title: Authenticate users with additional permissions to send campaign notifications in Microsoft Teams
description: Assign additional Microsoft Azure permissions to users to enable Microsoft Teams create and send new campaign notifications on the user’s behalf in the teamwork activity feed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/authenticate-user-addnl-campaign.html
release: xanadu
product: Employee Service Management
classification: employee-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working on campaigns in Microsoft Teams, Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Authenticate users with additional permissions to send campaign notifications in Microsoft Teams

Assign additional Microsoft Azure permissions to users to enable Microsoft Teams create and send new campaign notifications on the user’s behalf in the teamwork activity feed.

## Before you begin

Role required: admin

## Procedure

1.  Log in to the Microsoft Azure portal.

2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **App Registrations**.

3.  Open the Microsoft Azure application for self-configured app if it is already created, else create it.

4.  Navigate to **API Permissions** &gt; **Add a permission** &gt; **Microsoft Graph**, and click **Application permissions**.

5.  Select **TeamsActivity** accordion, and select **TeamsActivity.Send** check box.

    \[Omitted image "request-api-permissions-teams-activity-send.png"\] Alt text: Authenticate TeamsActivity.Send permission

6.  Select **Add permissions**.

7.  On the API permissions screen, select **Grant admin consent for \{tenant\}** link, and then select **Yes** on the pop-up dialog box.

8.  Regenerate and upload the manifest file in Microsoft Teams.

    For more information, see [Send campaign notifications automatically in Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/enable-activity-feed.md).

9.  Register the Request-based chat app in your instance to use Microsoft Teams chat on a self-configured app environment.

    For more information, see [Configure Application Registry on the ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/app-registry-chat-single-tenant.md).


**Parent Topic:**[Working on campaigns in Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/using-campaigns-ms-teams.md)

