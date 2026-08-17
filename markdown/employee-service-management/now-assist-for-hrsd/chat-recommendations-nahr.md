---
title: Generate a chat reply recommendation by using ServiceNow Otto for HRSD
description: Generate a reply based on the context of the chat conversation using ServiceNow Otto icon. Chat reply recommendations can help provide agents with quick replies to common questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-hrsd/chat-recommendations-nahr.html
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use generative AI skills, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Generate a chat reply recommendation by using ServiceNow Otto for HRSD

Generate a reply based on the context of the chat conversation using ServiceNow Otto icon. Chat reply recommendations can help provide agents with quick replies to common questions.

## Before you begin

[Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md).

Role required: sn\_hr\_gen\_ai.admin

## About this task

You can do these actions by using the ServiceNow Otto icon:

-   Generate a recommended reply that is based on the context of the conversation.
-   Refine the recommendation by elaborating or shortening the response.

**Note:** The Chat reply recommendation skill can be found in the **HRSD** tab under the **Employee** group in AI Admin Hub. To learn how to activate this skill, see [Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md).

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Agent Workspace for HRSD**.

2.  Open the inbox and accept the chat interaction.

    In the Active Chat section of the interaction, a summary of the Virtual Agent conversation is generated. The summary includes the actions that were taken before the requester engaged with the live agent. With this information, you can get an overview of what the requester has already mentioned in the Virtual Agent conversation and troubleshoot the issue.

3.  Chat with the requester to get any additional details about their question or issue, if needed.

    For example, if the requester is having an issue with hardware, you may need the hardware model number and serial number.

4.  In the chat message window, either type a response, or leave blank, and then select the ServiceNow Otto icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: Sparkle icon for Now Assist.

<table id="choicetable_nbt_cxv_bcc"><thead><tr><th align="left" id="d402702e186">

Chat message window

</th><th align="left" id="d402702e189">

ServiceNow Otto icon

</th></tr></thead><tbody><tr><td id="d402702e197">

**Typed response**

</td><td>

Provides the option to refine your response:

-   Elaborate
-   Shorten


</td></tr><tr><td id="d402702e217">

**Left blank**

</td><td>

Generates a recommended reply that is based on the context of the conversation up to this point.

</td></tr></tbody>
</table>    The reply response appears in the ServiceNow Otto icon modal.

5.  Review the generated reply and select **Refine** to modify the response, or select **Insert** to paste the response into the chat message window.

    If the reply response was refined, you can toggle between versions.

6.  In the chat message window, select **Send**.

7.  End the chat by selecting **End Chat**.


**Parent Topic:**[Using ServiceNow Otto for HR Service Delivery \(HRSD\) in Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Summarize a Sidebar discussion by using ServiceNow Otto for HRSD]()

[Generate a knowledge article from HR Agent Workspace with ServiceNow Otto for HRSD]()

[Generate a knowledge article from multiple cases]()

[Generate an email reply recommendation using ServiceNow Otto for HRSD]()

[Summarize an HR case using ServiceNow Otto for HRSD]()

[Summarize an ER case using ServiceNow Otto for HRSD]()

[Summarize an ER case interview using ServiceNow Otto for HRSD]()

[Generate resolution notes using ServiceNow Otto for HRSD]()

[View employee summary reports]()

[Summarize actions while transferring an HR case]()

[Use Knowledge Graph in ServiceNow Otto for HRSD]()

[Use ServiceNow Otto for HRSD – Galileo Inside to answer HR-related questions]()

[Use the ServiceNow Otto panel in HR Agent Workspace]()

[Submit an HR request with Gen AI Virtual Agent]()

[ServiceNow Otto for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework]()

[Analyze sentiments in ServiceNow Otto for HR Service Delivery \(HRSD\)]()

