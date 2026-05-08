---
title: Request the generative AI capabilities in Customer Service Management by using the Now Assist panel
description: Request the contextual generative AI capabilities, such as a chat summary, case summary, case resolution notes, call summary, or knowledge article generation in the CSMCustomer Service Management application by using the conversational interface in the Now Assist panel.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI, Now Assist for CSM, Customer Service Management]
---

# Request the generative AI capabilities in Customer Service Management by using the Now Assist panel

Request the contextual generative AI capabilities, such as a chat summary, case summary, case resolution notes, call summary, or knowledge article generation in the CSMCustomer Service Management application by using the conversational interface in the Now Assist panel.

## Before you begin

Make sure that Next Experience is enabled in the instance. For more information, see [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Make sure that [AI search](https://www.servicenow.com/docs/access?context=configuring-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and [Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=turn-on-the-subflows-and-actions-skill&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) are enabled in the instance for the conversational subflows and actions to work.

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

You can use the Now Assist panel in CSM Configurable Workspace to request a chat, call or case summary, generate case resolution notes and knowledge article, ask a question about a case, Use AI agents to complete cases and use conversational subflows and actions.

For more information about the Now Assist panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For information about activating the Now Assist panel, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Log in to an instance where the Now Assist for CSM application is installed.

3.  Request the generative AI capabilities in CSM for an interaction or case by selecting the Now Assist icon![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg).

    ![Now Assist panel with a list of available actions and a task selection dropdown displayed after the user chose "Add Comment To Task.".](../image/now-assist-csm-na-panel.png "Now Assist panel")

4.  After you request the generative AI capabilities, you can summarize a chat for an interaction, summarize a chat for a case created from an interaction, summarize a case, generate the resolution notes for a case, summarize a call, generate a knowledge article, ask questions about a case, use AI agents to complete cases, and complete tasks with conversational subflows and actions.

<table id="choicetable_tvj_cqn_xyb"><thead><tr><th align="left" id="d40764e203">

Option

</th><th align="left" id="d40764e206">

Description

</th></tr></thead><tbody><tr><td id="d40764e212">

**Summarize the chat for an interaction**

</td><td>

1.  Open the interaction.
2.  From the header menu, select the Now Assist icon ![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg).
3.  In the Now Assist panel, select **Chat Summarization**. A summary of the chat conversation with the live agent is displayed.


</td></tr><tr><td id="d40764e248">

**Summarize the chat for a case that is created from an interaction**

</td><td>

1.  Open the case that was created from an interaction.
2.  From the header menu, select the Now Assist icon ![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg).
3.  In the Now Assist panel, select **Chat Summarization**. A summary of the chat conversation with the live agent before the case was created is displayed.


</td></tr><tr><td id="d40764e284">

**Summarize a case**

</td><td>

1.  Open the case.
2.  From the header menu, select the Now Assist icon ![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg).
3.  In the Now Assist panel, select **Summarize a record**.


</td></tr><tr><td id="d40764e320">

**Generate case resolution notes**

</td><td>

1.  Open the case.
2.  From the header menu, select the Now Assist icon ![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg).
3.  In the Now Assist panel, select **Generate resolution notes**.


</td></tr><tr><td id="d40764e357">

**Summarize a call**

</td><td>

1.  Open the case.
2.  From the header menu, select the Now Assist icon ![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg).
3.  In the Now Assist panel, select **Summarize conversation**. A call summary of the conversation with the live agent is generated on the details page.


</td></tr><tr><td id="d40764e393">

**Generate a knowledge article**

</td><td>

1.  Open the case.
2.  From the header menu, select the Now Assist icon ![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg).
3.  In the Now Assist panel, select **Generate Article**. A knowledge article is drafted for the case using task data, comments, and work notes from the activity stream.


</td></tr><tr><td id="d40764e429">

**Ask questions about a case**

</td><td>

1.  Open the case.
2.  From the header menu, select the Now Assist icon ![Now assist icon.](../../../reuse/icons/brand-icons/bus-ai-sparkle.svg).
3.  In the Now Assist panel, enter a case assist topic question and select a case assist topic. Information requested about the case is shown.


</td></tr><tr><td id="d40764e462">

**Use AI agents to complete cases**

</td><td>

1.  Get notified when an AI agent use case is triggered.
2.  Follow the onscreen instructions to complete the task.


</td></tr></tbody>
</table>5.  You can also use the Now Assist panel to type in a question related to a case and complete tasks with conversational subflows and actions.

    |Available actions and subflows|Example questions that can be asked|
    |------------------------------|-----------------------------------|
    |**Action- Add comments to task**|I want to add comments to a case|
    |**Action- Add work notes to task**|I want to add work notes to a case|
    |**Subflow- Create task for case**|I want to create a task for a case|
    |**Subflow- Reassign case**|I want to reassign a case|

    Information requested about the case is shown. Conversational subflows and actions capture users' intents when requesting to run specific subflows and actions, along with all necessary details for those subflows and actions. This streamlines the user experience by enabling them to accomplish everything in one place within the Now Assist panel.


**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](../concept/now-assist-csm-using.md)

