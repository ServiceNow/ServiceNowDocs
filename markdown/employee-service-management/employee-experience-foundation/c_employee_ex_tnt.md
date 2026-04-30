---
title: Setup for integrating pre-published apps with Microsoft Teams for Employee Experience
description: Set up pre-published apps to integrate with IT, HR, and Universal Request through Microsoft Teams. Employees can interact with the agents from within Microsoft Teams to resolve their issues.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setup for integrating pre-published apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Setup for integrating pre-published apps with Microsoft Teams for Employee Experience

Set up pre-published apps to integrate with IT, HR, and Universal Request through Microsoft Teams. Employees can interact with the agents from within Microsoft Teams to resolve their issues.

-   **[Connect your ServiceNow instance to your Microsoft Teams tenant](../task/connect-sn-instance-ms-teams-mt.md)**  
Connect your ServiceNow instance to your Microsoft Teams tenant to enable users to create their requests from within Microsoft Teams.
-   **[Grant permissions to required Microsoft Azure apps](../task/authorize-multi-tenant-apps-mt.md)**  
Authorize the required pre-published apps to enable your ServiceNow instance to make API calls to Microsoft Azure to enable ServiceNow for Teams application workflows.
-   **[Enable connecting to meetings from Microsoft Teams](../task/create-oauth-oidc-record.md)**  
Create the OIDC provider configuration record that enables users to connect to meetings in the Microsoft Teams application.
-   **[Change tenant to configure pre-published apps](../task/change-tenant.md#)**  
Change the tenant to use pre-published apps in your environment.
-   **[Create and download the manifest file for pre-published apps](../task/download-manifest-file-mt.md)**  
Create and download the ServiceNow for Microsoft Teams manifest file from your instance to enable Microsoft Teams to use the ServiceNow for Teams app.
-   **[Upload manifest file in Microsoft Teams](../task/upload-manifest-ms-teams.md)**  
Upload the manifest file in Microsoft Teams to integrate Microsoft Teams with your ServiceNow instance.
-   **[Update the app ID in the ServiceNow instance](../task/update-app-id-instance-mt.md)**  
Update the ServiceNow for Teams app ID from the Microsoft Teams admin center in your ServiceNow instance.
-   **[Disable the Now Virtual Agent](../task/disable-now-virtual-agent-ms-teams.md)**  
Disable the Now Virtual Agent app to avoid duplicate notifications from Microsoft Teams when you install and integrate ServiceNow for Microsoft Teams with your ServiceNow instance.
-   **[Translate the Microsoft Teams manifest file](localize-manifest-file.md)**  
ServiceNow for Microsoft Teams supports localization to multiple languages, using UTF-8 for international characters.
-   **[Request-based chat access for a guest user](guest-user-chat-access-mt.md)**  
Request-based pre-published app chat access enables a guest user to start and import chats in a single ServiceNow® for Microsoft Teams instance.
-   **[User Presence Indicator](user-presence-indicator-mt.md)**  
User presence indicator helps the agents to know the status of the users in Microsoft Teams before the agent can initiate a chat using Microsoft Teams.
-   **[Sending notifications to employees using Microsoft Teams](using-campaigns-ms-teams-mt.md)**  
Integrate Microsoft Teams with the Employee Center to enable content managers to send notifications to employees through Microsoft Teams.

**Parent Topic:**[Setup for integrating pre-published apps with Microsoft Teams](setup-multi-tenant.md)

