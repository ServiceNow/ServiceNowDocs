---
title: Configure Microsoft Teams
description: Easily integrate and collaborate with Microsoft Teams to resolve Major Security Incident to view and filter collaboration chat activities.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Major Security Incident Management, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure Microsoft Teams

Easily integrate and collaborate with Microsoft Teams to resolve Major Security Incident to view and filter collaboration chat activities.

Configuring and subscribing to a Microsoft Teams chat environment, retrieving chat conversations from within specified channels, and archiving the Team and associated channels are included as part of the incident closure process. A designated Microsoft Teams environment and related Microsoft Teams Graph API configuration is required to create individual channels that are specific to a Major Security Incident.

To configure Microsoft Teams, activate Teams as the chat provider. You can then create chat channels for the various stakeholders and groups communicating about activities and track chat conversations to resolve the Major Security Incident. The Microsoft Teams and Microsoft Graph API configuration includes:

-   [Establish MS Teams Graph connection on ServiceNow AI Platform](../task/msim-micorsoft-team-requirements.md)
-   [Activate MS Teams as a chat provider](../task/chat-provider-configuration.md)
-   [Create a chat channel template](../../secops-integration-major-security-incident-management/task/create-chat-channel-template-for-msim.md)
-   [View Chat Message Activity](../task/chat-message-activity.md)

-   **[Get started with Microsoft Teams](../../secops-integration-major-security-incident-management/reference/get-started-with-microsoft-teams.md)**  
Review the following information before you start working with Microsoft Teams as a connector application.
-   **[Activate MS Teams as a chat provider](../task/chat-provider-configuration.md)**  
Activate Microsoft Teams by validating the Microsoft Teams Connection.
-   **[Create a chat channel template](../../secops-integration-major-security-incident-management/task/create-chat-channel-template-for-msim.md)**  
Configure Chat Teams and Channel Templates to create chat teams and channels to collaborate, track the chat conversations, and add users and user groups to those Chat Channels. These Channel templates are created in the Microsoft Teams when a major security incident is promoted.
-   **[View Chat Message Activity](../task/chat-message-activity.md)**  
Chat message activity is recorded and displayed on the Collaboration tab of the Major Security Incident Management workspace.
-   **[MS Teams Chat Connector Troubleshooting for MSIM](microsoft-teams-chat-connector-troubleshooting-for-msim.md#)**  
Refer to Microsoft Teams chat connector troubleshooting section on the scheduled jobs, system properties, and Microsoft Teams flow designer subflows.

**Parent Topic:**[Configuring Major Security Incident Management](../../secops-integration-major-security-incident-management/reference/configuring-major-security-incident-management.md)

**Related topics**  


[Configure File Explorer Component](file-explorer.md)

[Configure Slack chat connector for major security incidents](../../secops-integration-major-security-incident-management/concept/configure-slack-chat-connector-msi.md)

