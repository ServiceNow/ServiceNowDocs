---
title: Request time off using ITSM Virtual Agent
description: Automate your request for time off using the ITSM Virtual Agent. Type keywords into the chatbot to create and submit your request, which then gets automatically routed to your manager for approval. You can also use Natural Language Understanding to make your time-off request.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace - Scheduling, Workforce Optimization for ITSM in the Service Operations Workspace, Optimize, Service Operations Workspace for ITSM, IT Service Management]
---

# Request time off using ITSM Virtual Agent

Automate your request for time off using the ITSM Virtual Agent. Type keywords into the chatbot to create and submit your request, which then gets automatically routed to your manager for approval. You can also use Natural Language Understanding to make your time-off request.

## Before you begin

The ITSM Virtual Agent Conversation Topics \(com.snc.itsm.virtualagent\) plugin must be enabled.

**Note:** To search shifts and schedules, you must [generate the text index](https://www.servicenow.com/docs/access?context=index-multiple-tables&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) for the Topic \[sys\_cs\_topic\] table before you start using the ITSM Virtual Agent for making time off requests.

Before you can use [Natural Language Understanding](https://www.servicenow.com/docs/access?context=nlu-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) to make time-off requests, the Time Off Request NLU model must be [trained](https://www.servicenow.com/docs/access?context=test-train-nlu-model&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [published](https://www.servicenow.com/docs/access?context=publish-nlu-model&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Role required: sn\_shift\_planning.agent

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Home**.

2.  Click the chat icon.

3.  In the chat window, do one of the following to create the request:

    -   To use keywords, enter *time off*, *vacation*, or similar keywords.
    -   To use Natural Language Understanding, enter an [utterance](https://www.servicenow.com/docs/access?context=va-NLU&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
4.  Select the Time Off Request topic.

    The calendar appears with the message, "When do you want to start your time off?"

5.  Select the start date and time for your time-off request and click **Select**.

    The calendar appears with the message, "When do you want to end your time off?"

6.  Select the end date and time for your time-off request and click **Select**.

    The "Would you like to enter the reason for your time off?" message appears.

7.  Click **Yes** and enter the reason for taking time off and click **Enter**.

    The message, "Your time-off request has been submitted and is in your manager's approval queue," appears.

8.  To view the submitted request on your calendar, click **View submitted request \(Request Number\)**.


**Parent Topic:**[Service Operations Workspace - Scheduling](../concept/itsm-sow-workspace-scheduling.md)

