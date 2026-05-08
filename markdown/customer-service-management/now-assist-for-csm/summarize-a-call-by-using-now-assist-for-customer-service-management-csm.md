---
title: Summarize a call by using Now Assist for Customer Service Management \(CSM\)
description: Generate a summary of the call conversation between a live agent and a customer by using the call summarization skill in the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI, Now Assist for CSM, Customer Service Management]
---

# Summarize a call by using Now Assist for Customer Service Management \(CSM\)

Generate a summary of the call conversation between a live agent and a customer by using the call summarization skill in the Now Assist for Customer Service Management \(CSM\) application.

## Before you begin

To make the skill available in the Now Assist Admin console, install Install ServiceNow Voice applications.

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, sn\_csm\_agent

## About this task

The call summarization skill enables you to do the following actions:

-   Summarize the call between a live agent and a caller when either the caller or the agent wraps up the conversation and ends the interaction.
-   Generate a call summary on demand from the Now Assist panel. For more information, see [Request the generative AI capabilities in Customer Service Management by using the Now Assist panel](request-gen-ai-capabilities-csm-now-assist-panel.md).
-   When real-time transcription is enabled, agents can see a transcript of the voice calls while interacting with the customers. With real-time transcription, an agent gets a better understanding of the customer issues, and a manager gains insights into the customer trends and agent training gaps.
-   When real-time transcription is turned off, agents don't see the conversation panel. Once the transcripts are ready, agents can see a Now Assist banner showing field predictions being generated. Then, another banner shows up with the predicted fields.
-   A call summary is available for both outbound and inbound calls. For more information, see [Real time transcriptions for ServiceNow Voice for Customer Service Management](https://servicenow.com/docs/csh?topicname=using-voice-rtt.html&version=latest).
-   Dynamic translation is supported for call summarization.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Set your status as Available in CSM Configurable Workspace so that you can receive a call request when a customer calls in and requests to speak to an agent.

    The call summarization skill creates an inline summary in the Active Chat window. This summary includes the transcript of the conversation between the agent and the customer.

3.  Chat with the customer to get any additional details about their question or issue.

    In the Active Chat window, a transcript of the call conversation with the customer is created.

    For example, if the customer is having an issue with the hardware, you may need the hardware model number and serial number.

4.  If enabled, transfer a call to another agent after accepting an incoming call and do the following actions:

    You need to have Advanced Work Assignment set up for an agent-to-agent transfer. For more information, see advanced work assignment setup.

    1.  From the keypad, select **Quick connects** while you’re still connected to the customer.

    2.  Select the name of another live agent.

    3.  Select **Call**.

        -   If the second agent selects **Join**, the second agent joins the conversation with both the first agent and the customer. The customer can have a conversation with both agents.
        -   If the second agent selects **Swap**, the second agent joins the conversation while the first agent is put on hold. The customer is in a conversation with the second agent only.
        -   The **Assigned to** field is updated with the new agent’s name and a summary card of the call is created in the conversation thread when the call is transferred from one live agent to another.
5.  End the conversation by selecting **End call**.

    The call summarization skill updates the **Short description** and **Chat Summary** fields on the interaction record when you end the call.

    **Note:**

    If a call summary isn’t available for the interaction, the **Chat Summary** field doesn’t appear on the interaction record.

6.  Review the text in the **Short description** and **Chat Summary** fields and make any necessary corrections.

    Because the information in these fields is automatically generated, human review of the text is necessary to ensure its accuracy.

7.  Select **Save**.

    ![AI-generated call summary for an interaction.](../image/now-assist.csm-call-summary.png "Interaction record with call summary")


## What to do next

If necessary, you can create a case from an interaction record. The system uses the information from the **Short description** and **Chat Summary** fields in the interaction record to populate the **Short description** and **Description** fields in the case record.

The system displays the Now Assist icon \(![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg)\) next to these fields and removes the icon if the agent changes the fields and saves the record.

**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](../concept/now-assist-csm-using.md)

