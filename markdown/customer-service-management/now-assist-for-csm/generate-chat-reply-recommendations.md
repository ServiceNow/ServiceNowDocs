---
title: Generate a chat reply recommendation by using ServiceNow Otto for Customer Service Management \(CSM\)
description: Generate a reply based on the context of the chat conversation using AI icon. Chat reply recommendations can help provide agents with quick replies to common questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/generate-chat-reply-recommendations.html
release: brazil
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI, ServiceNow Otto for CSM, Customer Service Management]
---

# Generate a chat reply recommendation by using ServiceNow Otto for Customer Service Management \(CSM\)

Generate a reply based on the context of the chat conversation using AI icon. Chat reply recommendations can help provide agents with quick replies to common questions.

See the video to understand how generative AI provides agents with suggested, personalized responses during live chat interactions. \[Omitted video\] Description: Chat reply recommendation

## Before you begin

Role required: agent

**Note:** To generate replies in a language other than English, a multilingual service must be enabled for ServiceNow Otto for CSM and the language must be activated on your instance. For the list of supported languages and the difference between native translation and Dynamic Translation, see [Multilingual service for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/translation-for-now-assist.md).

## About this task

You can do these actions by using the AI icon:

-   Generate a recommended reply that is based on the context of the conversation.
-   Refine the recommendation by elaborating or shortening the response.

**Note:**

-   The recommended reply is generated in the session language of the user. Language detection relies on the user's session language. With native translation, the chat text is sent to the model as-is and the model responds in the same language. If both native translation and Dynamic Translation are enabled, native translation is used first, and Dynamic Translation is applied automatically for languages that the model doesn't support natively. Language coverage varies by model provider. For more info, see [Configure multilingual service for ServiceNow Otto applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/enable-dynamic-translation-for-now-assist-applications.md)
-   The Chat reply recommendation skill is on the Chat skill card in the Customer group.

## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace**.

2.  Open the inbox and accept the chat interaction.

    In the Active Chat section of the interaction, a summary of the Virtual Agent conversation is generated. The summary includes the actions that were taken before the requester engaged with the live agent. With this information, you can get an overview of what the requester has already mentioned in the Virtual Agent conversation and troubleshoot the issue.

3.  Chat with the requester to get any additional details about their question or issue, if needed.

    For example, if the requester is having an issue with hardware, you may need the hardware model number and serial number.

4.  In the chat message window, either type a response, or leave blank, and then select the AI icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: Sparkle icon for Now Assist.

<table id="choicetable_nbt_cxv_bcc"><thead><tr><th align="left" id="d34765e170">

Chat message window

</th><th align="left" id="d34765e173">

AI icon

</th></tr></thead><tbody><tr><td id="d34765e179">

**Typed response**

</td><td>

Provides the option to refine your response:

-   Elaborate
-   Shorten
 Provides the option to change your tone:

-   Casual
-   Formal
-   Sympathetic


</td></tr><tr><td id="d34765e213">

**Left blank**

</td><td>

Generates a recommended reply that is based on the context of the conversation up to this point.

</td></tr></tbody>
</table>    The reply response appears in the AI icon modal.

    **Note:** Refine and tone options apply in the session language. If the generated reply appears in a different language than expected, confirm that the language is activated in Now Assist Admin and supported by your selected model provider.

5.  Review the generated reply and select **Refine** to modify the response, or select **Insert** to paste the response into the chat message window.

    If the reply response was refined, you can toggle between versions.

6.  In the chat message window, select **Send**.

7.  End the chat by selecting **End Chat**.


**Parent Topic:**[Using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

**Related topics**  


[https://www.youtube.com/watch?v=6A5jwZFOPR4](https://www.youtube.com/watch?v=6A5jwZFOPR4)

