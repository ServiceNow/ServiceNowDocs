---
title: Install the Conversational Integration with Workplace from Facebook
description: You can install the Conversational Integration with Workplace from Facebook \(sn\_va\_fb\_workplace\) application with the admin role.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Conversational Integration with Workplace from Facebook, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Install the Conversational Integration with Workplace from Facebook

You can install the Conversational Integration with Workplace from Facebook \(sn\_va\_fb\_workplace\) application with the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   If you're using an earlier release of Virtual Agent, you must upgrade to the Australia release to use the features supported in this messaging integration.
-   Conversational Integration with Workplace from Facebook requires the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) to activate full functionality in Virtual Agent or the Virtual Agent Lite plugin \(com.glide.cs.chatbot.lite\) to activate a limited version of Virtual Agent. Activate the appropriate plugin before you install the integration.
-   Install the Conversational Integration with Workplace from Facebook from the ServiceNow® Store.

    **Important:** Installing the Conversational Integration app from the ServiceNow Store store activates the corresponding **Install** button in the Channels and integrations page. If you have not installed the integration app, the Workplace from Facebook app is listed in the Available Channels section.

    ![Channels and integrations page before the Conversational Integration with Workplace app is installed from the ServiceNow Store.](../images/workplace-pre-install.png "Channels and integrations page before Conversational Integration with Workplace from Facebook is installed")

    After you install the Conversational Integration with Workplace from Facebook app, the Workplace from Facebook is seen in the Integrations section, and you can proceed with the configuration.


Roles required: virtual\_agent\_admin and external\_app\_install\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  In **General Settings** under **Channels and integrations**, click **View All**.

3.  On the Channels and integrations page, in the Microsoft Teams tile, click **Get Workplace plugin**.

    ![Microsoft Teams tile in Channels and integrations, with Get Workplace plugin button highlighted.](../images/get-workplace-plugin.png)

    You are redirected to the Conversational Integration with Workplace from Facebook ServiceNow Store page.

4.  On the top right corner of the screen, click **Get**.

    **Note:** You must be logged into the ServiceNow Store portal to get the plugin.

5.  On the Conversational Integration with Workplace from Facebook ServiceNow Store page, click **Request Install**.

6.  On the Request Install screen, provide the **Instance Name** and **Reason for request**.

    You can also validate the instance that you provided by clicking **Validate Instance**.

7.  Click **Request**.

    A message pops up on the Request Install screen that your request has been auto approved.


## What to do next

[Integrate ServiceNow Virtual Agent with Workplace from Facebook](configure-va-facebook.md).

**Parent Topic:**[Configuring Conversational Integration with Workplace from Facebook](../concept/configuring-ci-workplace-fb.md)

