---
title: Configure the IBM Watson Assistant Chat integration
description: Set up the IBM Watson Assistant topic to run dialog skills \(conversations created in IBM Watson Assistant\) in the web-based chat client. This topic returns information exchanged during the virtual agent conversation to IBM Watson Assistant.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-05"
reading_time_minutes: 3
keywords: [IBM Watson Assistant, Virtual Agent, chat widget, NLU, Natural Language Understanding]
breadcrumb: [Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure the IBM Watson Assistant Chat integration

Set up the IBM Watson Assistant topic to run dialog skills \(conversations created in IBM Watson Assistant\) in the web-based chat client. This topic returns information exchanged during the virtual agent conversation to IBM Watson Assistant.

## Before you begin

-   In IBM Watson Assistant:
    -   Create the dialog skill \(conversation\) in your IBM Watson Assistant workspace. The skill includes the dialog and any intents and entities that you define.
    -   Navigate to your skill tile and in the tile menu, select **View API Details**. View the Skill Details and Service Credentials. Copy the following items: **Skill ID**, **Workspace ID**, **Username**, and **Password**. You need these items when setting up this integration.
-   Activate the IBM Watson Assistant Integration plugin \(com.glide.cs.ibm.watson.assistant\).

Role required: virtual\_agent\_admin or admin

## About this task

This topic runs an IBM Watson Assistant dialog in Virtual Agent. It doesn't require enabling Natural Language Understanding \(NLU\) or setting IBM Watson Assistant NLU as the NLU service provider for Virtual Agent.

## Procedure

1.  In your ServiceNow instance, update the watson\_assistant.workspaceID system property.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  In the System Properties \[sys\_properties\] table, locate the watson\_assistant.workspaceID property.

    3.  Replace the existing **Value** with the **Workspace ID** for your skill, and select **Update**.

2.  Verify that the REST message for IBM Watson Assistant provides the correct authentication endpoint for your IBM skill:

    1.  Navigate to **System Web Services** &gt; **Outbound** &gt; **REST Message**.

    2.  Select the IBM Watson Assistant record to open the REST Message IBM Watson Assistance form.

    3.  Confirm that the **Endpoint** field and the **Endpoint** column displayed on the **Authentication** tab have the correct endpoint URL for your IBM Watson account.

        ![REST Messages form for IBM Watson Assistant with IBM endpoint URLs highlighted.](../images/REST-msg-Watson.png)

3.  In the **Basic auth profile** field on the **Authentication** tab, open the Assistant Profile record.

4.  In the Basic Auth Configuration form, enter the **Username** and **Password** values from your IBM Watson Assistant Service Credentials, then select **Update**.

    ![Basic Auth Configuration form for IBM Watson Assistant assistant profile.](../images/Basic-auth-config-assistant-profile.png)

5.  Publish the IBM Skill topic:

    1.  Navigate to **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**, and then slide the discovery type toggle switch to **NLU/keyword**.

    2.  On the home page, select the IBM Watson Assistant topic to open the Topic Properties page.

        Notice that the **Keyword** for this topic is IBM Watson Assistant and the **Category** is IBM.

    3.  In the Topic Properties page, select **Publish** to deploy the topic to your Virtual Agent chat widget.

6.  Configure the default topic for the Virtual Agent chat widget in one of the following ways:

    -   Provide the URL that specifies the IBM Watson Assistant topic as the default topic that opens in the Service Portal client:

        For example: `https://<Your instance URL>$sn-va-web-client-app.do?sysparm_skip_load_history=true&sysparm_topic=*&lt;sys\_id&gt;*` where *&lt;sys\_id&gt;* is the sys\_id of the published IBM Watson Assistant topic. The `sysparm_skip_load_history` parameter doesn't load the conversation history in the chat widget.

    -   Configure the Service Portal widget by selecting the edit \(pencil\) icon in the upper right corner of the Virtual Agent widget.

        To set the default topic using the widget instance parameters, enter `sysparm_topic=sys_id` \(where *&lt;sys\_id&gt;* is the sys\_id of the published IBM Watson Assistant topic\) in the **Virtual Agent Client URL Parameters** field, and select **Save**.

        **Note:** You can find the sys\_id of a topic in the Topics \[sys\_cs\_topic\] table.

    **Important:**

    Use the `sysparm_topic` parameter only to load the given topic in the Service Portal chat client or when using the IBM Watson Assistant chat integrations \(com.glide.cs.ibm.watson.assistant.topic and com.glide.cs.ibm.watson.assistant.topicV2 plugins\). This parameter doesn’t allow users to start a new conversation or transfer to a live agent. It also disables the context menu and doesn't support other third-party chat clients.


