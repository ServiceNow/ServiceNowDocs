---
title: Test the Action utility
description: Test the Action utility to make sure that the integrated action works as intended in the conversation.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating Virtual Agent with Workflow Studio workflows, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Test the Action utility

Test the Action utility to make sure that the integrated action works as intended in the conversation.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

When you test the subflow or action associated with the Action utility, you see a test results preview pane that includes preview-only messages. These messages include a link called **View in Workflow Studio**. This link takes you to the execution details. You can use the execution details to do the following:

-   Verify what is being returned to Virtual Agent.

    **Note:** Only topic authors have access to the **View in Workflow Studio** link. In non-production environments, this link is available by default. In production environments, topic authors must enable access to this link by creating a record in the \[sys\_flow\_execution\_setting\] table for each Workflow Studio asset. This link is not available in conversations where password2 input is used.

-   View the subflow or action execution details.

Topic authors can also see the test results in the Conversation Task FDIH Invocations \[sys\_cs\_fdih\_invocation\_list\] table.

**Note:** If you have turned on and set up Now Assist in Virtual Agent, you can work with conversational actions and subflows from the Assistant Designer home page. For each assistant, you can test topics, subflows, and actions by using the Assistant Designer home page **Test Assistant** button. Assistant Designer opens a Workflow Studio tab where you can test subflows and actions. For more information on conversational actions and subflows, see Conversational actions and Conversational subflows. You can still integrate actions and subflows that are not conversational from Workflow Studio into Virtual Agent topics via Assistant Designer. The following content is only relevant to actions or subflows that can't be made conversational in Workflow Studio.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  In the Asset library page, open the topic with the Action utility that you want to test.

3.  Select **Test**.

    If an action or subflow in the test window is slow to respond or appears to be waiting, you see a relevant error message.

    By default, a scheduled job checks the conversation flow every 120 seconds. For more information about scheduled jobs, see Scheduled jobs.

    You can change this interval, as needed. To change the interval, see [Specify the action workflow timeout](va-fdih-action-timeout.md).

4.  Troubleshoot the Action utility node:

    -   View the execution details.
    -   Look at the Conversation Task FDIH Invocations \[sys\_cs\_fdih\_invocation\_list\] table.
5.  Select **Save** when you're finished.


**Parent Topic:**[Integrating Virtual Agent with Workflow Studio workflows](../concept/va-flow-designer-integration.md)

