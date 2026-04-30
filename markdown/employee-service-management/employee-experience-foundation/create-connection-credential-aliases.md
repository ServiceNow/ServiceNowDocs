---
title: Create a Connection &amp; Credentials alias for Microsoft Teams
description: Create an alias to associate the connection information with the credential data required to complete the application integration in Microsoft Teams.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating Notify connector self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Create a Connection &amp; Credentials alias for Microsoft Teams

Create an alias to associate the connection information with the credential data required to complete the application integration in Microsoft Teams.

## Before you begin

Role required: admin

## About this task

For more information, refer [Introduction to credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials Aliases**.

2.  Select **MSTeamsCommunicationsSpoke**.

3.  Select **New** in the Credentials related list.

4.  Select **OAuth 2.0 Credentials**.

5.  Set the values for the credentials.

    1.  Enter a name for the credential in the **Name** field, for example, `Notify Microsoft Teams credentials for self-configured app`.

    2.  Enter the OAuth Entity profile information in the **OAuth Entity Profile** field, for example, `<application-registry-name>_default_profile`.

        The profile ID is set when you generate the application registry entry.

6.  Select **Submit**.


**Parent Topic:**[Integrating Notify connector self-configured app with Microsoft Teams](../concept/setup-notify-ms-teams-single-tenant.md)

