---
title: Upload the manifest package file to publish your bot
description: Upload the manifest file that you generated to the Microsoft Teams and test your app experience to make it be available in the Microsoft global app store.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrate VA with MS Teams using self-configured bot, Specialized VA integrations for Teams, Integrate VA with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Upload the manifest package file to publish your bot

Upload the manifest file that you generated to the Microsoft Teams and test your app experience to make it be available in the Microsoft global app store.

## Before you begin

Role required: Microsoft Teams admin, Global Administrator, or roles containing Application Administrator.

The self-configured bot that you created will not be available in the Microsoft global app store unlike the ServiceNow pre-published app - ServiceNow Virtual Agent. To test your app experience within Microsoft Teams, you must upload your app to Microsoft Teams. Uploading adds the app to the team that you selected and your team can participate in the end-to end conversations with the bot.

## Procedure

1.  Log in to the [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/) using the admin credentials and navigate to **Teams apps** &gt; **Setup policies**.

2.  Under **Manage policies**, select the policy you are uploading your manifest under \(usually **Global \(Org-wide default\)**\), and activate the **Upload custom apps** toggle switch.![Microsoft Teams admin center portal, with Teams apps tab open and Setup policies selected. Teams apps, Setup policies, and Upload custom apps areas are highlighted.](../images/enable-custom-app-msteams.png)

3.  Navigate to **Teams apps** &gt; **Manage apps**.![Microsoft Teams apps portal. Teams apps, Manage apps, Actions, and Upload new app options are highlighted.](../images/msteams-manage-apps.png)

4.  Under the **Actions** drop-down menu, select **Upload new app**, then select **Upload** and add your manifest zip file.

    Your manifest file is uploaded and appears on the list of store apps.

    **Note:** If you receive any errors, correct the listed errors in your manifest, then download the zip file and upload it through this page again. If you activated Microsoft Copilot in your manifest, the Custom Engine Agent \(CEA\) is also uploaded with it. For more information on activating Copilot, see [Activate Now Assist in Virtual Agent for Microsoft Teams](activate-na-va-msteams.md).

5.  After you successfully published the bot, select the **All apps** tab and use the search bar to find your app.![Microsoft Teams Apps portal, with All apps tab, app search bar, and bot app highlighted.](../images/msteams-find-app.png)

    You have successfully published the bot on Microsoft Teams. It should now be available for your organization and you can start interacting with the bot.

6.  Perform the following steps on the Microsoft Teams Admin center.

    **Note:** If you have enabled pre-linking by turning on **Automatically Link ServiceNow user profiles** on the Messaging App Integration UI page, users are pre-linked without typing hi. For more information about pre-linking your accounts, see [Installing Microsoft Teams for all Virtual Agent users](prelink-va-users-integ-msteams.md). If you have turned off the check box, use the following manual account linking process described.

    1.  Type `hi` to start interacting with the bot.

        The bot presents a prompt that provides options to authenticate, such as **Link to ServiceNow**, **Continue as Guest**, and **Check out Tips**.

        ![Microsoft Teams multi instance bot prompts.](../images/msteams-custom-bot-response.png "Microsoft Teams bot responses")

        The **Link to ServiceNow** option requires users to enter their ServiceNow instance credentials. If you choose to link to your ServiceNow account, the following screen is displayed asking you to confirm the account linking.

        ![Microsoft Teams account linking confirmation dialog box.](../images/msteams-confirm-snow-acnt-link.png "Linking Microsoft Teams account with ServiceNow account")

        Account linking associates your Microsoft Teams account with your ServiceNow account for the ServiceNow instance that is integrated with the Conversational Integration with Microsoft Teams. Users with linked accounts can run Virtual Agent topics that use ServiceNow information and records.

        ![ServiceNow account linked with Microsoft Teams tenant.](../images/msteams-acnt-link-snow.png "ServiceNow account linked with Microsoft Teams tenant")

        If your users do not link their ServiceNow accounts, they can access and run only the public topics.

    2.  Configure the bot on your ServiceNow instance.

        For more information, see [Integrating Virtual Agent with messaging apps](../concept/va-integration-messaging-apps.md).


## What to do next

You have successfully integrated Virtual Agent with Microsoft Teams using the self-configured method. If you are interested in getting additional ITSM and HR capabilities in Microsoft Teams, see these [instructions for using a self-configured bot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/download-manifest-file-mt.md) with ServiceNow for Microsoft Teams.

**Parent Topic:**[Integrating Virtual Agent with Microsoft Teams using the self-configured bot](../concept/va-integ-teams-self-configured-bot.md)

