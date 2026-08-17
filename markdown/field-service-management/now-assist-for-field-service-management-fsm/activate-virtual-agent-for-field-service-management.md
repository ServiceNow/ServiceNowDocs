---
title: Create an Assistant for Field Service Management
description: Set up ServiceNow Otto in Virtual Agent to help Field Service technicians summarize work order tasks and find relevant Knowledge Base articles to complete their tasks efficiently from the Mobile Agent application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/now-assist-for-field-service-management-fsm/activate-virtual-agent-for-field-service-management.html
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, ServiceNow Otto for FSM]
---

# Create an Assistant for Field Service Management

Set up ServiceNow Otto in Virtual Agent to help Field Service technicians summarize work order tasks and find relevant Knowledge Base articles to complete their tasks efficiently from the Mobile Agent® application.

## Before you begin

Role required: wm\_admin

The Field Service Mobile plugin \(com.sn\_fsm\_mobile\) must be installed to use the ServiceNow Otto Virtual Agent in mobile.

## About this task

The ServiceNow Otto Virtual Agent for FSM enables agents to ask questions and get specific answers found in Knowledge Base articles. It sources the article used to provide the answer and provides the relevant answer found there. By providing immediate access to essential information, the ServiceNow Otto Virtual Agent for FSM enables technicians to resolve issues more swiftly and accurately, ultimately improving service quality and customer satisfaction. This setup is required to see the ServiceNow Otto Virtual Agent for Field Service Mobile Agent® application. The following steps guide you through the process of activating this virtual agent to optimize your Field Service Management.

To set up and control who has access to the AI agents and the workflows they manage, see [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants**.

2.  Select **ServiceNow Otto Virtual Agent for FSM**.

    **Note:**

    If you select one of the default assistants, there can be some inapplicable options. These options are a part of the menu by default and won’t affect your task.

3.  Select the **Settings** tab.

4.  Review the guided setup steps.

    All of the guided setup steps are preconfigured. No changes are required to complete the setup.

    |Guided Setup Steps|Description|
    |------------------|-----------|
    |Basic details|In the Add some details section, provide a unique name and description for your Virtual Agent.|
    |Agentic support|Enable the virtual assistant to use AI agent skills and agentic orchestration.|
    |Display Experiences|Set the display experience for mobile to ServiceNow Otto for FSM.|
    |Branding|Set the branding for mobile to ServiceNow Otto for FSM.|
    |Additional chat features|Enable or disable additional chat features, such as web search, response streaming, document uploads, closed chats, and voice input.|
    |Chat experience|Manage greeting, closing, and fallback messages.|
    |Response feedback|Enable response feedback from the user when they rate a response.|

5.  After all the details are provided, select **Test assistant** to preview how the agent will work.

6.  Select **Save** to save the inputs.

7.  Select **Activate** to activate the virtual agent.


