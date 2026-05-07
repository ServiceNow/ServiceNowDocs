---
title: Test conversational subflow
description: Test a conversational subflow to verify it responds correctly to user inputs and performs the expected operations before deploying it in production.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 1
breadcrumb: [Build subflows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Test conversational subflow

Test a conversational subflow to verify it responds correctly to user inputs and performs the expected operations before deploying it in production.

## Before you begin

Role required: flow\_designer

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Subflows**.

3.  From the list of subflows, select the subflow that you want to test.

4.  Select **Test**.

5.  From the Test subflow dialog box, select **Trigger via a conversation**.

    |Trigger option|Description|
    |--------------|-----------|
    |Trigger by entering inputs|Test by manually entering and selecting input values.|
    |Trigger via a conversation|Test by providing inputs values in a chat experience.|

    ![Test subflow dialog box with Trigger via a conversation option selected](../images/example-test-subflow-via-conversation.png)

6.  For **Select skill**, select the conversational-enabled skill that you want to use for conversational testing.

    To configure subflow conversational settings, see [Configure subflow conversational settings](configure-subflow-conversation-settings.md).

7.  For **Select assistant**, select the AI assistant you want to use for conversational testing.

8.  Select **Run Test**.

9.  In the assistant conversation, answer the questions that the AI assistant asks you.

    For example, provide the details needed to create an address.

    ![Sample conversation to test Create Address subflow](../images/example-test-subflow-conversation.png)

10. Review the execution details.

    For example, these are sample execution details for the Create Address subflow.

    ![Sample execution details from testing the Crate Address subflow via a conversation](../images/example-execution-details-conv-subflow.png)


**Parent Topic:**[Building subflows](../concept/subflows.md)

