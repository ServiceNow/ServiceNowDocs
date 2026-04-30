---
title: Summarize a chat conversation by using Now Assist for IT Service Management \(ITSM\)
description: Summarize the Virtual Agent chat conversation between a live agent and a requester in Service Operations Workspace for ITSM. You can generate the summary by using the chat summarization skill in Now Assist for IT Service Management \(ITSM\).
locale: en-US
release: yokohama
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Summarize a chat conversation by using Now Assist for IT Service Management \(ITSM\)

Summarize the Virtual Agent chat conversation between a live agent and a requester in Service Operations Workspace for ITSM. You can generate the summary by using the chat summarization skill in Now Assist for IT Service Management \(ITSM\).

## Before you begin

Role required: itil

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

In a Virtual Agent conversation, when a requester chooses to connect to a live agent, a chat interaction appears in your inbox. When you accept the interaction, a summary of the Virtual Agent conversation is generated. You can request more details from the requester to resolve the issue.

You can also summarize the chat interaction when the chat ends or when an incident is created for further troubleshooting before or after the chat ends. The summary includes all points of the handoff, including the Virtual Agent conversation, and provides a context of the interaction to you and the other agents who might want to refer to it.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Open the inbox and accept the chat interaction.

    In the **Active Chat** section of the interaction, a summary of the Virtual Agent conversation is generated. The summary includes the actions taken before the requester engaged with the live agent. With this information, you can get an overview of what the requester has already mentioned in the Virtual Agent conversation and troubleshoot the issue.

3.  Chat with the requester to get any additional details about their question or issue.

    For example, if the requester is having an issue with hardware, you may need the hardware model number and serial number.

4.  Summarize the chat while interacting with the requester by using the `/summarize` quick action in the **Active Chat** section.

5.  End the chat by selecting **End Chat**.

    The **Short description** and **Chat Summary** fields are updated for the interaction.

    ![Chat summarization for an interaction.](../image/itsm-chat-summary.png)

6.  Review the text in the **Short description** or **Chat Summary** fields and edit if necessary.

    For example, you might want to make the summary more descriptive.

    **Note:** Because the information in these fields is automatically generated, it's a good idea to review the text and make sure it's accurate.

7.  Select **Save**.

8.  If you think that you need further help after the initial troubleshooting before or after ending the chat, create an incident from the interaction by selecting **Create incident**.

    -   When you create an incident before ending the chat, the **Short Description** and **Description** fields of the incident are updated with the interaction summary and saved.
    -   When you create an incident after ending the chat, the following information is generated:
        -   The **Chat summary** field of the interaction is updated with the interaction summary.
        -   The **Short Description** and **Description** fields of the incident are updated with the interaction summary and saved.

