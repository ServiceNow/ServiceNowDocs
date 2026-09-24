---
title: Create an Assistant for Field Service Management
description: Set up a ServiceNow Otto Virtual Agent to help Field Service technicians summarize work order tasks and find relevant Knowledge Base articles to complete their tasks efficiently from the Mobile Agent application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/mobile-experience-for-field-service-management-glide-family/activate-virtual-agent-for-field-service-management.html
release: brazil
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up Virtual Agent conversations, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Create an Assistant for Field Service Management

Set up a ServiceNow Otto® Virtual Agent to help Field Service technicians summarize work order tasks and find relevant Knowledge Base articles to complete their tasks efficiently from the Mobile Agent® application.

## Before you begin

Role required: wm\_admin

The Field Service Mobile plugin \(com.sn\_fsm\_mobile\) must be installed to use ServiceNow Otto® Virtual Agent in mobile.

## About this task

The ServiceNow Otto® Virtual Agent for FSM, available OOTB, enables agents to ask questions and get specific answers found in Knowledge Base articles. It sources the article used to provide the answer and provides the relevant answer found there. By providing immediate access to essential information, the ServiceNow Otto® Virtual Agent for FSM enables technicians to resolve issues more swiftly and accurately, ultimately improving service quality and customer satisfaction. This setup is required to see the ServiceNow Otto® Virtual Agent for Field Service Mobile Agent® application. The following steps guide you through the process of activating this virtual agent to optimize your Field Service Management.

To set up and control who has access to the AI agents and the workflows they manage, see [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aia-security-implementation.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants**.

2.  Select **ServiceNow Otto Virtual Agent for FSM**.

    **Note:**

    If you select one of the default assistants, you might see some inapplicable options. These options are a part of the menu by default and won’t affect your task.

3.  Review each of the seven guided setup steps:

    All of the guided setup steps are preconfigured. No changes are required to complete the setup.

    |Guided Setup Steps|Description|
    |------------------|-----------|
    |Overview|In the Add some details section, provide a unique name and description for your Virtual Agent.|
    |Now Assist Skills|Enable ServiceNow Otto® Q&amp;A and ServiceNow Otto® topics skills.|
    |Display Experiences|Set the display experience for mobile to ServiceNow Otto® for FSM.|
    |Information Sources|Select the knowledge table as the information source.|
    |Branding|Set the branding for mobile to ServiceNow Otto® for FSM.|
    |Chat Experiences|Manage greeting, closing, and fallback messages.|
    |Review|Review your choices and, optionally, test your virtual agent.|

4.  Select **Continue and Save** after reviewing each step.

5.  Select **Turn on** after the final review step.


