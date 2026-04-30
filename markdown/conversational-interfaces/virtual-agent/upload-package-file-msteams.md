---
title: Upload the manifest package file to publish your bot
description: Upload the manifest file that you generated to the Microsoft Teams and test your app experience to make it be available in the Microsoft global app store.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrating Virtual Agent with Microsoft Teams using the self-configured bot, Conversational Integration with Microsoft Teams, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Upload the manifest package file to publish your bot

Upload the manifest file that you generated to the Microsoft Teams and test your app experience to make it be available in the Microsoft global app store.

## Before you begin

Role required: admin

The self-configured bot that you created will not be available in the Microsoft global app store unlike the ServiceNow pre-published app - ServiceNow Virtual Agent. To test your app experience within Microsoft Teams, you must upload your app to Microsoft Teams. Uploading adds the app to the team that you selected and your team can participate in the end-to end conversations with the bot.

## Procedure

1.  Log in to the [Microsoft Teams Admin Center](https://admin.teams.microsoft.com/) using the admin credentials and navigate to **Teams apps** &gt; **Setup policies**.

2.  Select **Add** and turn on **Upload custom apps** \(if it has not been enabled already\) and select **Save** at the bottom of the page.![Microsoft Teams admin center portal, with Teams apps tab open and Setup policies selected. Teams apps, Setup policies, Add policies, and Upload custom apps areas are highlighted.](../images/enable-custom-app-msteams.png)

3.  Open Microsoft Teams app and navigate to **Apps** &gt; **Manage your apps**.![Microsoft Teams apps portal. Apps, Manage your apps, Upload a custom app, and Upload an app to your org's app catalog options are highlighted.](../images/msteams-manage-apps.png)

4.  Select **Upload a custom app** for testing purposes and select **Upload an app to your org's app catalog** to release the self-configured bot to the entire organization.

5.  Upload the zip file and select **Add/Install**.

6.  After you successfully published the bot, select the 3-dot menu on the left pane to locate your app \(search in the Find an app bar\).![Microsoft Teams Apps portal, with three-dot menu icon highlighted.](../images/msteams-find-app.png)

    You have successfully published the bot on Microsoft Teams. It should now be available for your organization and you can start interacting with the bot.

7.  Perform the following steps on the Microsoft Teams Admin center.

    **Note:** If you have enabled pre-linking by turning on **Automatically Link ServiceNow user profiles** on the Messaging App Integration UI page, users are pre-linked without typing hi. For more information about pre-linking your accounts, see [Pre-link Virtual Agent requesters for integration with Microsoft Teams](prelink-va-users-integ-msteams.md). If you have turned off the check box, use the following manual account linking process described.

    1.  Type `hi` to start interacting with the bot.

        The bot presents a prompt that provides options to authenticate, such as **Link to ServiceNow**, **Continue as Guest**, and **Check out Tips**.

        ![Microsoft Teams multi instance bot prompts.](../images/msteams-custom-bot-response.png "Microsoft Teams bot responses")

        The **Link to ServiceNow** option requires users to enter their ServiceNow instance credentials. If you choose to link to your ServiceNow account, the following screen is displayed asking you to confirm the account linking.

        ![Microsoft Teams account linking confirmation dialog box.](../images/msteams-confirm-snow-acnt-link.png "Linking Microsoft Teams account with ServiceNow account")

        Account linking associates your Microsoft Teams account with your ServiceNow account for the ServiceNow instance that is integrated with the Conversational Integration with Microsoft Teams. Users with linked accounts can run Virtual Agent topics that use ServiceNow information and records.

        ![ServiceNow account linked with Microsoft Teams tenant.](../images/msteams-acnt-link-snow.png "ServiceNow account linked with Microsoft Teams tenant")

        If your users do not link their ServiceNow accounts, they can access and run only the public topics.

    2.  Configure the bot on your ServiceNow instance.

        For more information, see [Virtual Agent integration with messaging apps](../concept/va-integration-messaging-apps.md).


## What to do next

You have successfully integrated Virtual Agent with Microsoft Teams using the self-configured method. If you are interested in getting additional ITSM and HR capabilities in Microsoft Teams, see these [instructions for using a self-configured bot](https://www.servicenow.com/docs/access?context=download-manifest-file-mt&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US) with ServiceNow for Microsoft Teams.

