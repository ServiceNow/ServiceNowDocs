---
title: Request the generative AI capabilities in Customer Service Management by using the ServiceNow Otto panel
description: Request generative AI capabilities in the ServiceNow Otto panel, such as chat summaries, case summaries, resolution notes, or knowledge article generation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/request-gen-ai-capabilities-csm-now-assist-panel.html
release: brazil
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI, ServiceNow Otto for CSM, Customer Service Management]
---

# Request the generative AI capabilities in Customer Service Management by using the ServiceNow Otto panel

Request generative AI capabilities in the ServiceNow Otto panel, such as chat summaries, case summaries, resolution notes, or knowledge article generation.

## Before you begin

Make sure that Next Experience is enabled in the instance. For more information, see [Next Experience UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/next-experience-landing-page.md).

Make sure that [AI search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/configuring-ais.md) and Now Assist in Virtual Agent are enabled in the instance for the conversational subflows and actions to work.

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

You can use the Now Assist panel in CRM Workspace to request a chat, call or case summary, and generate case resolution notes and knowledge articles. You can also ask questions about a case and use AI agents to complete casesand conversational subflows and actions.

For more information about the Now Assist panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md). For information about activating the panel, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-now-assist-panel.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace**.

2.  Log in to an instance where the ServiceNow Otto for CSM application is installed.

3.  Request the generative AI capabilities in CSM for an interaction or case by selecting the AI icon\[Omitted image "bus-ai-sparkle.svg"\] Alt text: AI icon..

    \[Omitted image "now-assist-csm-na-panel.png"\] Alt text: Panel with a list of available actions and a task selection dropdown displayed after the user chose "Add Comment To Task.".

4.  After you request the generative AI capabilities, you can use the following options.

<table id="choicetable_tvj_cqn_xyb"><thead><tr><th align="left" id="d41903e191">

Option

</th><th align="left" id="d41903e194">

Description

</th></tr></thead><tbody><tr><td id="d41903e200">

**Summarize the chat for an interaction**

</td><td>

1.  Open the interaction.
2.  From the header menu, select the AI icon \[Omitted image "bus-ai-sparkle.svg"\] Alt text: AI icon..
3.  In the panel, select **Chat Summarization**. A summary of the chat conversation with the live agent is displayed.


</td></tr><tr><td id="d41903e230">

**Summarize the chat for a case that is created from an interaction**

</td><td>

1.  Open the case that was created from an interaction.
2.  From the header menu, select the AI icon \[Omitted image "bus-ai-sparkle.svg"\] Alt text: AI icon..
3.  In the panel, select **Chat Summarization**. A summary of the chat conversation with the live agent before the case was created is displayed.


</td></tr><tr><td id="d41903e260">

**Summarize a case**

</td><td>

1.  Open the case.
2.  From the header menu, select the AI icon \[Omitted image "bus-ai-sparkle.svg"\] Alt text: AI icon..
3.  In the panel, select **Summarize a record**.


</td></tr><tr><td id="d41903e290">

**Generate case resolution notes**

</td><td>

1.  Open the case.
2.  From the header menu, select the AI icon \[Omitted image "bus-ai-sparkle.svg"\] Alt text: AI icon..
3.  In the panel, select **Generate resolution notes**.


</td></tr><tr><td id="d41903e321">

**Summarize a call**

</td><td>

1.  Open the case.
2.  From the header menu, select the AI icon \[Omitted image "bus-ai-sparkle.svg"\] Alt text: AI icon..
3.  In the panel, select **Summarize conversation**. A call summary of the conversation with the live agent is generated on the details page.


</td></tr><tr><td id="d41903e351">

**Generate a knowledge article**

</td><td>

1.  Open the case.
2.  From the header menu, select the AI icon \[Omitted image "bus-ai-sparkle.svg"\] Alt text: AI icon..
3.  In the panel, select **Generate Article**. A knowledge article is drafted for the case using task data, comments, and work notes from the activity stream.


</td></tr><tr><td id="d41903e381">

**Ask questions about a case**

</td><td>

1.  Open the case.
2.  From the header menu, select the AI icon \[Omitted image "bus-ai-sparkle.svg"\] Alt text: AI icon..
3.  In the panel, enter a case assist topic question and select a case assist topic. Information requested about the case is shown.


</td></tr><tr><td id="d41903e408">

**Use AI agents to complete cases**

</td><td>

1.  Get notified when an AI agent use case is triggered.
2.  Follow the onscreen instructions to complete the task.


</td></tr></tbody>
</table>5.  You can also use the panel to type in a question related to a case and complete tasks with conversational subflows and actions.

    |Available actions and subflows|Example questions that can be asked|
    |------------------------------|-----------------------------------|
    |**Action- Add comments to task**|I want to add comments to a case|
    |**Action- Add work notes to task**|I want to add work notes to a case|
    |**Subflow- Create task for case**|I want to create a task for a case|
    |**Subflow- Reassign case**|I want to reassign a case|

    Information requested about the case is shown. Conversational subflows and actions capture users' intents when requesting to run specific subflows and actions, along with all necessary details for those subflows and actions. This streamlines the user experience by enabling them to accomplish everything in one place within the panel.


**Parent Topic:**[Using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

