---
title: Auto-generate the manifest file and upload it into Microsoft Teams for GCC-H or DoD
description: After you complete integrating the bot on the ServiceNow instance, configure the manifest file, auto-generate it, and upload the package file to Microsoft Teams to start conversing with the Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/upload-app-package-msteams.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrate VA with MS Teams for GCC-H, Specialized VA integrations for Teams, Integrate VA with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Auto-generate the manifest file and upload it into Microsoft Teams for GCC-Hor DoD

After you complete integrating the bot on the ServiceNow instance, configure the manifest file, auto-generate it, and upload the package file to Microsoft Teams to start conversing with the Virtual Agent.

## Before you begin

Role required: admin

## About this task

The self-configured bot that you created is not available in the Microsoft global app store, unlike the ServiceNow pre-published app - ServiceNow Virtual Agent. You must upload your app to Microsoft Teams. Uploading adds the app to the team that you select and you and your team can participate in the end-to end conversations with the bot.

**Note:**

You need permission to upload custom apps in Microsoft Teams. To learn how to enable it, refer to the Microsoft documentation.

## Procedure

1.  To configure the bot, auto-generate the manifest file, and download the manifest configured file in your ServiceNow instance, see [Auto-generate the manifest file for uploading on Microsoft Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/generate-manifest-file-msteams.md).

2.  To publish the manifest file, from Microsoft Teams, perform the following steps:

    1.  Open Microsoft Teams app and navigate to **Apps** &gt; **Manage your apps**.\[Omitted image "image\_ms\_teams\_app\_upload2.png"\] Alt text: Microsoft Teams apps portal. Apps, Manage your apps, and Upload an app to your org's app catalog options are highlighted.

    2.  Select **Upload an app to your org's app catalog** to release the self-configured bot to the entire organization.

    3.  Upload the zip file and select **Add/Install**.

    4.  After you successfully published the bot, select the 3-dot menu on the left pane to locate your app \(search in the Find an app bar\).\[Omitted image "msteams-find-app.png"\] Alt text: Microsoft Teams Apps portal, with three-dot menu icon highlighted.

        You have successfully published the bot on Microsoft Teams. It should now be available for your organization and you can start interacting with the bot.

3.  **Note:** If you have enabled pre-linking by turning on **Automatically Link ServiceNow user profiles** on the Messaging App Integration UI page, users are pre-linked without typing hi. For more information about pre-linking your accounts, see [Installing Microsoft Teams for all Virtual Agent users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/prelink-va-users-integ-msteams.md). If you have turned off the check box, use the following manual account linking process described.

    Type `hi` to start interacting with the bot.

    The bot presents a prompt that provides options to authenticate, such as **Link to ServiceNow**, **Continue as Guest**, and **Check out Tips**.

    The **Link to ServiceNow** option requires you to enter their ServiceNow instance credentials. If you choose to link to your ServiceNow account, the following screen is displayed asking you to confirm the account linking.

    Account linking associates your Microsoft Teams account with your ServiceNow account for the ServiceNow instance that is integrated with the Conversational Integration with Microsoft Teams. If your account is linked, you can run Virtual Agent topics that use ServiceNow information and records.

    \[Omitted image "msteams-acnt-link-snow.png"\] Alt text: ServiceNow account linked with Microsoft Teams tenant.

    If you do not link your ServiceNow accounts, you can access and run only the public topics.

4.  Configure the bot on your ServiceNow instance.

    For more information, see [Integrating Virtual Agent with messaging apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-integration-messaging-apps.md).


## What to do next

You have successfully integrated Virtual Agent with Microsoft Teams using the self-configured method. If you are interested in getting additional ITSM and HR capabilities in Microsoft Teams, see these instructions for using a self-configured bot with ServiceNow for Microsoft Teams.

**Parent Topic:**[Integrating Virtual Agent with Microsoft Teams for GCC-H or DoD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-integ-msteams-gcch.md)

