---
title: Configure Virtual Agent for a ServiceNow mobile application
description: Virtual Agent provides optimized templates for the mobile experience. Configure a service portal to run Virtual Agent on a ServiceNow mobile application.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Configure Virtual Agent for a ServiceNow mobile application

Virtual Agent provides optimized templates for the mobile experience. Configure a service portal to run Virtual Agent on a ServiceNow mobile application.

## Before you begin

Install the required plugins:

-   Virtual Agent \(com.glide.cs.chatbot\)
-   Conversational Messaging \(com.glide.messaging.awa\)
-   Core ServiceNow® mobile plugins

    For more information, see [Mobile plugins](https://www.servicenow.com/docs/access?context=sg-mobile-plugins&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).


Role required: admin

## Procedure

1.  Install the corresponding mobile plugins for each application that you want to use in Virtual Agent.

    For example, if you're using Virtual Agent ITSM conversations, install the ITSM Mobile Agent \(sn\_itsm\_mobile\_agt\) plugin as well. For more information, see [Mobile plugins for ServiceNow Agent](https://www.servicenow.com/docs/access?context=sg-mobile-plugins&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

2.  Navigate to **All** &gt; **Now Mobile App** &gt; **Applet Launchers**.

3.  Click the **Homepage** record.

    If prompted, click the link at the top of the page to edit the record.

4.  Click the **Body** tab.



    ![Select the Body tab at the bottom of the Launcher screen Homepage record to see the Quick actions menus section.](../images/mobile-launcher-homepage.png)

5.  Click **Chat** under **Quick Action Button** to open the record.

    If you don't see a Chat entry, add it as follows:

    1.  In the Unified Navigation bar, click the scope icon and change the application scope so that it matches the application that contains the record.

        ![When you change the scope, the scope icon turns red. A message on the screen indicates that you're editing a record in the Now Mobile application.](../images/change-application-scope-mobile.png)

    2.  Click the back button to return to the previous page.

    3.  Click the **Homepage** record.

    4.  Click the **Body** tab.

    5.  Under **Quick Action Button**, double-click **Insert a new row**.

    6.  Type `Chat`, and then press Enter or click the save icon.

    7.  Click **Update**.

6.  Fill in the Chat form as follows.

    **Note:** If prompted, click the link at the top of the page to edit the record.

    1.  In the **Function** field, select **Agent Chat**.

    2.  Click the info icon ![Information icon.](../images/icon-info.png) on the **Function** field and verify that **Chat Launcher** is set in the **Type** field \(this is the default setting\).

    3.  Select the **Active** check box.

    4.  Click **Update**.

    ![The Function field should specify "Agent Chat." The Type field should display "Chat Launcher" by default.](../images/mobile-chat-configuration.png "Chat form configuration")


## Result

Depending on the device and the patch version of the server instance, end users can access the Virtual Agent chat icon in the bottom-right or top-right corner of the app. Tap the plus icon or the chat icon to start a conversation.

The topics you create in Virtual Agent Designer can be used in both the web and mobile clients, as well as any other channels you may configure. Virtual Agent output components are already optimized for Android and iOS, including [image and video cards](../reference/va-card-output.md), [link unfurling](../concept/va-link-unfurling.md), [AI Search results](../concept/va-ai-search.md), and [Virtual Agent notifications](../concept/configuring-va-notifications.md).

## What to do next

To enable Now Assist in native Virtual Agent, see [Configuring Now Assist in Virtual Agent](../../now-assist-in-va/task/configure-now-assist-va.md).

-   **[Now Mobile notification of unread chat and Virtual Agent messages](../concept/va-mobile-unread-messages.md)**  
When Now® Mobile app users navigate away from the app after starting an active conversation, they can automatically receive Virtual Agent mobile push notifications informing them of new, unread chat messages and  Virtual Agent notifications that have arrived.
-   **[View and modify Virtual Agent style templates](modify-va-templates.md)**  
Virtual Agent provides optimized templates for the mobile experience. You can view and modify the style sheets in the Adapter Cards \[sys\_cs\_adapter\_card\] table.

**Parent Topic:**[Configuring Virtual Agent](../concept/configure-virtual-agent.md)

