---
title: Configure the IBM Watson Assistant Chat integration for the Assistant V2 API
description: Configure the IBM Watson Assistant Chat Integration to run a dialog skill \(conversation\) created in IBM Watson Assistant with the Assistant V2 API. The V2 API enables the Virtual Agent chat widget to run a topic that uses Watson Assistant's intent disambiguation feature to improve topic discovery.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-14"
reading_time_minutes: 6
keywords: [IBM Watson Assistant, Virtual Agent, API]
breadcrumb: [Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure the IBM Watson Assistant Chat integration for the Assistant V2 API

Configure the IBM Watson Assistant Chat Integration to run a dialog skill \(conversation\) created in IBM Watson Assistant with the Assistant V2 API. The V2 API enables the Virtual Agent chat widget to run a topic that uses Watson Assistant's intent disambiguation feature to improve topic discovery.

## Before you begin

**Note:** An updated Virtual Agent Designer user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not enabled, you will see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](../reference/vad-prev-topics-page.md).

With the IBM Watson Assistant v2 API chat integration, the chat widget communicates with an assistant instead of with a workspace. Workspaces are referred to as dialog skills. For information on IBM Watson Assistant, see [Migrating to the v2 API](https://cloud.ibm.com/docs/services/assistant?topic=assistant-api-migration&locale=en-us#overview) in the IBM Watson Assistant documentation.

Role required: virtual\_agent\_admin or admin

## About this task

This integration runs an IBM Watson Assistant dialog as a Virtual Agent topic in the chat widget. It doesn't require enabling Natural Language Understanding \(NLU\) or setting IBM Watson Assistant NLU as the NLU service provider for Virtual Agent.

The IBM Watson Assistant V2 API enables the chat widget to use the Watson Assistant intent disambiguation feature, which can potentially reduce false-positive intent predictions. If a user's utterance is ambiguous, IBM Watson Assistant suggests additional intents that might better match the user's true intention. For example, if the user utterance is `restaurant`, IBM Watson Assistant can suggest other possible intents, such as `book a restaurant` or `restaurant reviews`.

## Procedure

1.  Configure IBM Watson Assistant.

    1.  Create your assistant, then add a dialog skill.

        For details, see [Creating an assistant](https://cloud.ibm.com/docs/services/assistant?topic=assistant-assistant-add) in the IBM Watson Assistant documentation.

    2.  On the Resource list page, locate and record your API key and URL, which you need to set up the chat integration:

        ![Resource list page in IBM Watson Assistant, which shows the API key and URL values for the assistant.](../images/Watson-Resource-list.png)

    3.  Select the three vertical dots icon ![More info icon.](../images/kebab-menu.png) and select **Settings**.

        -   Select the **API Details** tab.
        -   On the Assistant Settings page, find the **Assistant ID** key.
        ![IBM Watson Assistant Settings for the dialog skill to be used. API Details and Assistant ID are highlighted here.](../images/WatsonAssistantSettings.png)

2.  Enable the disambiguation feature in IBM Watson Assistant \(for premium and plus users only\).

    You can enable \(or disable\) disambiguation for each skill, and also specify a disambiguation message and the number of suggestions to be displayed to the end user.

    1.  Access your skill by selecting the skill tree icon ![Skill tree icon.](../images/IBM-watson-skilltree.png) in the panel.

        ![Assistants list in IBM Watson Assistant with skill tree icon highlighted.](../images/AccessSkillTree.png)

    2.  Navigate to **Options** &gt; **Disambiguation** to enable disambiguation and set the disambiguation features.

        The following example shows the disambiguation features that can be set, such as the disambiguation message and the number of suggested intents to be displayed to the end user.

        ![Disambiguation form in IBM Watson Assistant. Disambiguation tab, on-off toggle, disambiguation message, anything else message, and suggestion maximum are highlighted.](../images/WatsonDisambiguation.png)

3.  Navigate to **Dialog**, select a node to which the disambiguation feature will apply, and provide a summary of the node that will be displayed to users if it's one of the intent suggestions.

    ![Dialog node with a node purpose summary displayed to users as an alternate intent choice for disambiguation. Optional node summary is highlighted.](../images/WatsonDialogNodeSummary.png)

4.  In your ServiceNow instance, activate these plugins:

    -   Glide Virtual Agent \(com.glide.cs.chatbot\), if not already activated \(requires a subscription\)
    -   IBM Watson Assistant Integration V2 plugin \(com.glide.cs.ibm.watson.assistant.topicV2\)
5.  In Virtual Agent Designer, publish the IBM Watson Assistant V2 topic:

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

    2.  On the home page, select the IBM Watson Assistant V2 topic to open the Topic Properties page.

        Notice that the **Keyword** for this topic is IBM Watson Assistant V2.

    3.  In the Topic Properties page, select **Publish** to deploy the topic to your Virtual Agent chat widget.

6.  Navigate to **All**, and then enter `sys_properties.list` in the filter.

7.  Update the following properties.

    -   **watson\_assistant.v2.assistantID** — In the **Value** field, enter the Watson Assistant ID for your assistant and select **Update**.

        ![System Property form for the watson_assistant.v2.assistantID property. Example Watson Assistant ID value and Update button are highlighted.](../images/WatsonAssistantIDprop.png)

    -   **watson\_assistant.v2.service\_endpoint** — In the **Value** field, replace the existing value with your Watson Assistant URL and select **Update**.

        ![Form for the watson_assistant.v2.service_endpoint property. with example URL value and Update button highlighted.](../images/WatsonAssistant-endpoint-prop.png)

        **Note:** You can specify just the location portion of the service instance URL in the **Value** field. For example, if the base URL for the IBM Watson service endpoint is https://gateway.watsonplatform.net/assistant/api, you can enter just the location of the service instance, `gateway.watsonplatform.net` in the **Value** field.

        If your Watson Assistant is hosted in a data center other than Dallas, such as Washington DC, your base URL is https://gateway-wdc.watsonplatform.net/assistant/api. You would enter `gateway-wdc.watston.platform.net` in the **Value** field.

8.  Set the Watson Assistant API key as the password in the IBM Watson Assistant Profile.

    1.  Navigate to **All**, and then enter `sys_auth_profile_basic.list` in the filter.

    2.  Open the IBM Watson Assistant Profile record.

    3.  In the Basic Auth Configuration form, enter the Watson Assistant API key in the **Password** field and select **Update**.

        ![Basic auth configuration for the IBM Watson Assistant Profile, with Password field and Update button highlighted.](../images/WatsonAssistantAuthProfile.png)

9.  Add the Virtual Agent \(web chat\) client to the Service Portal.

    1.  Navigate to **Service Portal** &gt; **Service Portal Configuration**.

    2.  Select **Designer**, and then select the **Service Portal** landing page.

    3.  Search for the Virtual Agent widget and drag the widget into the outlined area.

        The purple chat icon appears in the bottom right corner.

        ![Service Portal designer page with Virtual Agent Service Portal Widget, design canvas, and chat icon highlighted.](../images/ServicePortal-WatsonChat.png)

10. Configure the Virtual Agent widget by selecting the edit icon ![Edit icon.](../images/edit-icon.png) in the upper right corner to set the URL parameters passed to the chat client and change the color of the floating chat button.

    1.  In the **Virtual Agent Client URL Parameters** field, enter the **sysparm\_skip\_load\_history=true** parameter so that the topic history doesn't display in the chat client and the **sysparm\_topic** parameter with the sys\_id of the published IBM Watson Assistant V2 topic to be run.

        You can find the sys\_id of a topic in the Topics \[sys\_cs\_topic\] table.

        If you don't configure the instance behavior in Service Portal, you can specify your instance URL with the **sysparm\_topic** and **sysparm\_skip\_load\_history** parameters when you open the chat chat widget. For example: `https://<Your instance URL>$sn-va-web-client-app.do?sysparm_skip_load_history=true&sysparm_topic=*&lt;sys\_id&gt;*` where *&lt;sys\_id&gt;* is the sys\_id of the published IBM Watson Assistant V2 topic to be run.

        **Important:**

        Use the `sysparm_topic` parameter only to load the given topic in the Service Portal chat client or when using the IBM Watson Assistant chat integrations \(com.glide.cs.ibm.watson.assistant.topic and com.glide.cs.ibm.watson.assistant.topicV2 plugins\). This parameter doesn’t allow users to start a new conversation or transfer to a live agent. It also disables the context menu and doesn’t support other third-party chat clients.

    2.  To change the floating button color, enter the new color \(RGB hex format\) in the **Floating Button Color** field.

    3.  Select **Save**.

        ![Service Portal designer page with open Instance dialog box. Virtual Agent Client URL Parameters field is highlighted.](../images/ServicePortal-sysparm-url-example.png)

11. Test that the disambiguation feature is working for your topic.

    Be sure that disambiguation is enabled for your Watson Assistant skill and at least two dialog nodes. In the following example, the virtual agent provides four additional intents that the user can select.

    ![Virtual Agent conversation showing additional intents discovered through the disambiguation feature.](../images/ExampleDisambiguationTopic.png "Example topic with disambiguation")


