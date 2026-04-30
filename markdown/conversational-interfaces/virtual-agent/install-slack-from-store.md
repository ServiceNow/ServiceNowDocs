---
title: Install the Conversational Integration with Slack
description: You can install the Conversational Integration with Slack \(sn\_va\_slack\) application if you have the admin role.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating ServiceNow Virtual Agent with Slack, Conversational Integration with Slack, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Install the Conversational Integration with Slack

You can install the Conversational Integration with Slack \(sn\_va\_slack\) application if you have the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   If you're using an earlier release of Virtual Agent, you must upgrade to the Xanadu release to use the features supported in this channel integration.
-   Conversational Integration with Slack requires the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) to activate full functionality in Virtual Agent or the Virtual Agent Lite plugin \(com.glide.cs.chatbot.lite\) to activate a limited version of Virtual Agent. Activate the appropriate plugin before you install the integration.
-   Install the Conversational Integration with Slack app from the ServiceNow® Store.

    **Important:** Installing the Conversational Integration with Slack app from the ServiceNow Store activates the app for integration on your ServiceNow instance. If you have not installed the integration app, the Slack app is listed in the Available Channels section.

    ![The Channels and integrations page before Slack is installed.](../images/slack-pre-install.png "Channels and integrations page before Conversational Integration with Slack apps is installed")

    After you install the Conversational Integration with Slack plugin \(sn\_va\_slack\), Slack is seen in the Integrations section, and you can proceed with the configuration.


Role required: virtual\_agent\_admin and external\_app\_install\_admin or admin

## About this task

Review these guidelines for using Virtual Agent with Slack or with Slack Enterprise Grid.

-   The Slack app creates a one-to-one association between the ServiceNow instance that you are installing from and the Slack workspace in which the integration runs.
    -   Use a separate Slack workspace for each instance that you plan to install the integration in.
    -   If you use a non-production instance for testing, use a Self-configured bot.

        For more information, see [Integrate ServiceNow instance with Self-configured bot](integ-slack-self-config-bot.md).

-   Slack Enterprise Grid – If you have Slack Enterprise Grid workspaces, your end users can move between workspaces and use the Virtual Agent bot from any workspace.
    -   If you use a non-production instance for testing, use a workspace in a different grid or use a non-grid workspace.
    -   After installing this store release:
        -   Your messaging users are automatically linked to their ServiceNow accounts.
        -   If you clone an instance for non-production testing, be sure to run the installation again on the cloned target.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, click **View All**.

3.  On the Channels and integrations page, in the Slack tile, click **Get Slack plugin**.![Slack tile in Channels and integrations, showing Get Slack plugin control.](../images/get-slack-plugin.png)

    You are redirected to the Conversational Integration with Slack ServiceNow Store page.

4.  On the top right corner for the screen, click **Get**.

    **Note:** You must be logged into the ServiceNow Store portal to get the plugin.

5.  On the Conversational Integration with Slack ServiceNow Store page, click **Request Install**.

6.  On the Request Install screen, provide the **Instance Name** and **Reason for request**.

    You can also validate the instance that you provided by clicking **Validate Instance**.

7.  Click **Request**.

    A message pops up on the Request Install screen that your request has been auto approved.


## What to do next

[Integrate ServiceNow Virtual Agent with Slack](add-slack-snow-bot.md).

