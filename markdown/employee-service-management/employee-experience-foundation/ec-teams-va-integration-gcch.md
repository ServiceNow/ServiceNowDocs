---
title: Integrating Employee Center and Virtual Agent with Microsoft Teams for GCC-H or DoD
description: You can integrate Employee Center and the Virtual Agent bot with Microsoft Teams to enable Government Community Cloud High \(GCC-H\) and US Department of Defense \(DoD\) customers to interact with agents through Virtual Agent and access the attached files in Employee Center.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ServiceNow with Microsoft Teams for GCC-H or DoD, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Integrating Employee Center and Virtual Agent with Microsoft Teams for GCC-H or DoD

You can integrate Employee Center and the Virtual Agent bot with Microsoft Teams to enable Government Community Cloud High \(GCC-H\) and US Department of Defense \(DoD\) customers to interact with agents through Virtual Agent and access the attached files in Employee Center.

## Prerequisites

Before integrating Employee Center with your Microsoft Teams tenant, ensure that the following prerequisites are met:

-   Your ServiceNow instances have been upgraded to the Vancouver release.
-   You have not previously attempted to install the Conversational Integration with Microsoft Teams app on your instances.
-   You have the admin permissions on ServiceNow and Microsoft Azure instances.

## Integration process

The overall process to integrate Employee Center with your Microsoft Teams tenant involves the following tasks:

1.  Activate the IT Service Management integration with Microsoft Teams plugin \(sn\_now\_teams\_it\) and Glide Virtual Agent plugin \(com.glide.cs.chatbot\).

    **Note:** For more information on activating plugins, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

2.  [Create Microsoft Azure application and authenticate users to access Employee Center in Microsoft Teams](../task/authenticate-users-your-hub-ms-teams.md).
3.  [Create a bot in Microsoft Teams for GCC-H or DoD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/create-msteams-bot-gcch.md).
4.  [Integrate your self-configured bot with Microsoft Teams for GCC-H or DoD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/link-msteams-bot-snow.md).
5.  [Update your Microsoft Teams tenant URL for GCC-H or DoD](../task/gcch-response-header.md).
6.  [Modify and download the manifest file for GCC-H or DoD](../task/modify-download-manifest-file.md).
7.  [Upload manifest file in Microsoft Teams](../task/upload-manifest-ms-teams.md).

-   **[Modify and download the manifest file for GCC-H or DoD](../task/modify-download-manifest-file.md)**  
Create and download the ServiceNow for Microsoft Teams manifest file from your instance to enable Microsoft Teams to use the ServiceNow for Teams app.

**Parent Topic:**[Integrating ServiceNow with Microsoft Teams for GCC-H or DoD](setup-sn-ms-teams-gcch.md)

