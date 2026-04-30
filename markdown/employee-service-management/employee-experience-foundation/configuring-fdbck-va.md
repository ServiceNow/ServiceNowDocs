---
title: Feedback for Virtual Agent setup
description: You can promote the experience feedback or set up service feedback for the Virtual Agent.Promote the experience feedback topic to appear in the default Virtual Agent suggestions.Set up the service feedback to appear after a topic conversation in the Virtual Agent.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrated experience and service feedback, Setup continuous improvement, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Feedback for Virtual Agent setup

You can promote the experience feedback or set up service feedback for the Virtual Agent.

## Promote experience feedback in Virtual Agent

Promote the experience feedback topic to appear in the default Virtual Agent suggestions.

### Before you begin

You must have a feedback definition for the Virtual Agent channel with the **Feedback type** set to Experience.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Experience and Service Feedback** &gt; **Feedback Definitions**

2.  Select the feedback definition that you created for the Virtual Agent channel.

3.  Select the **Promote Experience feedback in VA** related link.

    The experience feedback is promoted in the Virtual Agent.

4.  View the promoted topic record by selecting the link in the displayed message.

    For more information about promoted topics, see [Promote or demote LLM conversational subflows, actions, and topics in Virtual Agent Designer](https://www.servicenow.com/docs/access?context=promote-demote-va-topics&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).


## Set up service feedback for Virtual Agent

Set up the service feedback to appear after a topic conversation in the Virtual Agent.

### Before you begin

You must have a feedback definition for the Virtual Agent channel with the **Feedback type** set to Service - workflow.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Experience and Service Feedback** &gt; **Feedback Definitions**

2.  Select the feedback definition that you created for the Virtual Agent channel.

3.  Select the **Setup Service feedback in VA** related link.

4.  View the setup topic record by selecting the link in the displayed message.

    For more information about setup topics, see [Working with setup topics](https://www.servicenow.com/docs/access?context=working-setup-topics&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

    **Note:** You can set the value of the **com.glide.cs.survey.probability** system property to change the probability \(percentage\) that the survey setup topic occurs in your conversations. For example, set the Value to 0.50 to display the survey setup topic randomly in 50% of conversations.


### Result

The service feedback is set up for the Virtual Agent.

