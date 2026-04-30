---
title: Configure Now Assist for Field Service Management \(FSM\) in Virtual Agent
description: Set up Now Assist Virtual Agent to help Field Service technicians summarize work order tasks and find relevant Knowledge Base articles to complete their tasks efficiently from the ServiceNow Agent mobile application.
locale: en-US
release: zurich
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for FSM]
---

# Configure Now Assist for Field Service Management \(FSM\) in Virtual Agent

Set up Now Assist Virtual Agent to help Field Service technicians summarize work order tasks and find relevant Knowledge Base articles to complete their tasks efficiently from the ServiceNow Agent mobile application.

## Before you begin

Role required: wm\_admin

The Field Service Mobile plugin \(com.sn\_fsm\_mobile\) must be installed to use Now Assist Virtual Agent in mobile.

## About this task

The Now Assist Virtual Agent for FSM, available OOTB, enables agents to ask questions and get specific answers found in Knowledge Base articles. It sources the article used to provide the answer and provides the relevant answer found there. By providing immediate access to essential information, the Now Assist Virtual Agent for FSM enables technicians to resolve issues more swiftly and accurately, ultimately improving service quality and customer satisfaction. This setup is required to see the Now Assist Virtual Agent for Field Service Mobile Agent® application. The following steps guide you through the process of activating this virtual agent to optimize your Field Service Management.

To set up and control who has access to the AI agents and the workflows they manage, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants**.

2.  Select **Now Assist Virtual Agent for FSM**.

    **Note:**

    If you select one of the default assistants, you might see some inapplicable options. These options are a part of the menu by default and won’t affect your task.

3.  Review each of the seven guided setup steps:

    All of the guided setup steps are preconfigured. No changes are required to complete the setup.![Overview page of the guided setup](../image/nava-for-fsm.png)

    |Guided Setup Steps|Description|
    |------------------|-----------|
    |Overview|In the Add some details section, provide a unique name and description for your Virtual Agent.|
    |Now Assist Skills|Enable Now Assist Q&amp;A and Now Assist topics skills.|
    |Display Experiences|Set the display experience for mobile to Now Assist for FSM.|
    |Information Sources|Select the knowledge table as the information source.|
    |Branding|Set the branding for mobile to Now Assist for FSM.|
    |Chat Experiences|Manage greeting, closing, and fallback messages.|
    |Review|Review your choices and, optionally, test your virtual agent.|

4.  Select **Continue and Save** after reviewing each step.

5.  Select **Turn on** after the final review step.


