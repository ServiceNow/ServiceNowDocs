---
title: Generate a chat reply recommendation by using ServiceNow Otto for IT Service Management \(ITSM\)
description: Generate a reply based on the context of the chat conversation using the Now Assist icon. Chat reply recommendations provide agents with quick replies to common questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-chat-recommendation.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, ServiceNow Otto for IT Service Management \(ITSM\), IT Service Management]
---

# Generate a chat reply recommendation by using ServiceNow Otto for IT Service Management \(ITSM\)

Generate a reply based on the context of the chat conversation using the Now Assist icon. Chat reply recommendations provide agents with quick replies to common questions.

## Before you begin

Your admin must have enabled Virtual Agent and configured the chat assistant on the portal. For more information, see [Display your assistant on a portal, channel, or mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/display-assistant-portal-channel.md) and [Summarize a chat conversation by using ServiceNow Otto for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/generate-chat-summary-interaction-now-assist-itsm.md).

Role required: itil

## About this task

You can do these actions by using ServiceNow Otto icon:

-   Generate a recommended reply that is based on the context of the conversation.
-   Refine the recommendation by elaborating or shortening the response.

**Note:** The Chat reply recommendation skill is on the Chat skill card in the Technology group.

The Chat reply recommendation skill is turned on by default. The skill will be automatically available to appropriate role users for the application. When new customers install a Now Assist product, designated skills are turned on automatically. For existing users who upgrade, there will be no change to the skill activation. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Open the inbox and accept the chat interaction.

    In the Active Chat section of the interaction, a summary of the Virtual Agent conversation is generated. The summary includes the actions taken before the requester engaged with the live agent. With this information, you can get an overview of what the requester has already mentioned in the Virtual Agent conversation and troubleshoot the issue.

3.  Chat with the requester to get any additional details about their question or issue, if needed.

    For example, if the requester is having an issue with hardware, you may need the hardware model number and serial number.

4.  In the chat message window, either type a response, or leave blank, and then select the Now Assist icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: Now assist icon..

    \[Omitted image "now-assist-itsm-write-reply.png"\] Alt text: Chat message window with Now Assist option.

<table id="choicetable_mlz_kxk_1cc"><thead><tr><th align="left" id="d288061e200">

Chat message window

</th><th align="left" id="d288061e203">

ServiceNow Otto icon

</th></tr></thead><tbody><tr><td id="d288061e211">

**Typed response**

</td><td>

Provides the option to refine your response.

-   Elaborate
-   Shorten


</td></tr><tr><td id="d288061e231">

**Left blank**

</td><td>

Generates a recommended reply based on the context of the conversation up to this point.

</td></tr></tbody>
</table>    The reply response appears in the ServiceNow Otto context menu modal.

    \[Omitted image "now-assist-itsm-generate-reply.png"\] Alt text: Now Assist context menu modal.

5.  Review the generated reply and select **Refine** to modify the response, or select **Insert** to paste the response into the chat message window.

    **Note:** If the reply response was refined, you can toggle between versions.

6.  In the chat message window, select **Send**.

7.  End the chat by selecting **End Chat**.


