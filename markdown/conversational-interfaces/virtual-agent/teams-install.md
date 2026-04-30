---
title: Install Conversational Integration with Microsoft Teams
description: You can install the Microsoft Teams \(sn\_va\_teams\) application to integrate with Now Virtual Agent if you have the admin role.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-05-12"
reading_time_minutes: 3
breadcrumb: [Integrating ServiceNow Virtual Agent with Microsoft Teams, Integrating Virtual Agent with Microsoft Teams, Integrating Virtual Agent with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Install Conversational Integration with Microsoft Teams

You can install the Microsoft Teams \(sn\_va\_teams\) application to integrate with Now Virtual Agent if you have the admin role.

## Before you begin

-   Roles required:

    -   virtual\_agent\_admin and external\_app\_install\_admin or admin.

    -   Microsoft Teams administrator \(one of the following\): Global administrator, Application administrator, or Cloud Application administrator.

        **Note:** These aren’t necessarily required. Microsoft allows non-admin users to give consent to some or all requested permissions. Granting non-admin consent is not recommended, as this may cause unexpected behavior in the Now Now Virtual Agent application. Please review your user consent policies by consulting: https://learn.microsoft.com/en-us/entra/identity/enterprise-apps/configure-user-consent?pivots=portal


-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   If you're using an earlier release of Virtual Agent, you must upgrade to the 2023, February store release to use the features supported in this channel integration.
-   Conversational Integration with Microsoft Teams requires the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) to activate full functionality in Virtual Agent or the Virtual Agent Lite plugin \(com.glide.cs.chatbot.lite\) to activate a limited version of Virtual Agent. Activate the appropriate plugin before you install the integration.
-   Install the Conversational Integration with Microsoft Teams app from the ServiceNow® Store.

    **Important:** Installing the Conversational Integration with Microsoft Teams app from the ServiceNow Store activates the app for integration on your ServiceNow instance. If you have not installed the integration app, the Microsoft Teams app is listed in the Available Channels section.

    ![The Channels and integrations page displays a card with a Get Teams plugin link. For details, select the Learn more with a step-by-step guide link.](../images/msteams-pre-install.png "Channels and integrations page before Conversational Integration with Microsoft Teams apps is installed")

    After you install the Conversational Integration with Microsoft Teams app, Microsoft Teams is seen in the Integrations section, and you can proceed with the configuration.


## About this task

Review these guidelines for using Virtual Agent with Microsoft Teams.

-   The Microsoft Teams app creates a one-to-one association between the ServiceNow instance that you’re installing from and the Microsoft Teams tenant in which the integration runs.

    Use a separate Microsoft Teams tenant for each instance that you plan to install the integration in. If you plan to test with a non-production instance and clone the instance, be sure to run the configuration steps again on the clone target to associate the bot to the new instance. Running the steps again disassociates the integration between the original non-production instance and the tenant.

-   The Microsoft Teams app doesn’t support the Microsoft Teams premium account, which enables user email accounts other than Microsoft Office 365 accounts.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Channels and integrations**.

2.  On the Channels and integrations page, in the Microsoft Teams card, select **Get Teams plugin**.

    ![Microsoft Teams tile on Channels and integrations, with Get Teams Plugin button highlighted.](../images/get-teams-plugin.png)

    You’re redirected to the Conversational Integration with Microsoft Teams ServiceNow Store page.

3.  Select **Get**.

    **Note:** You must be logged in to the ServiceNow Store portal to get the plugin.

4.  On the Conversational Integration with Microsoft Teams ServiceNow Store page, select **Request Install**.

5.  On the Request Install screen, provide the **Instance Name** and **Reason for request**.

    You can also validate the instance that you provided by selecting **Validate Instance**.

6.  Select **Request**.

    A message pops up on the Request Install screen that your request has been auto-approved.


## What to do next

[Integrate ServiceNow Virtual Agent with Microsoft Teams](add-msteams-snow-va-bot.md).

**Parent Topic:**[Integrating ServiceNow Virtual Agent with Microsoft Teams](../concept/va-integ-msteams.md)

