---
title: Define post-chat survey configurations
description: Control the post-chat questionnaire displayed to your requesters to gather feedback on their experience with live agents. You configure the post-chat surveys to be used for chat queues defined in Advanced Work Assignment.
locale: en-US
release: australia
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Define post-chat survey configurations

Control the post-chat questionnaire displayed to your requesters to gather feedback on their experience with live agents. You configure the post-chat surveys to be used for chat queues defined in Advanced Work Assignment.

## Before you begin

-   Activate the Agent Chat plugin \(com.glide.interaction.awa\) if Advanced Work Assignment is not already installed.
-   In AWA, [configure the chat service channel](../../advanced-work-assignment/task/awa-create-service-channel.md) and the [work item queues](../../advanced-work-assignment/task/awa-create-queue.md).
-   Determine the post-chat survey to be displayed to your requesters.
    -   Review the existing chat surveys available in the Assessment Metric Types \[asmt\_metric\_type\] table by navigating to **All** &gt; **Survey View** &gt; **View Surveys**. You can use a pre-built feedback survey, such as the survey for Virtual Agent feedback \(a pre-built Virtual Agent setup topic\).
    -   If you need different post-chat surveys, create them using Survey Designer. For details, see [Create chat surveys](create-chat-surveys.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Settings** &gt; **Queues**.

2.  Select the queue \(that uses the Chat service channel\) to which the post-chat survey configuration applies.

3.  Go to the **Post Chat Survey** related list, and then select **New**.

    If the Post Chat Survey list doesn't display, you may need to add it to the form.

4.  On the form, fill in the fields.

<table id="table_tty_dm1_kjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for this post-chat survey configuration.

</td></tr><tr><td>

Active

</td><td>

Option that enables this post-chat survey configuration.

</td></tr><tr><td>

Show Summary

</td><td>

Survey option that asks requesters if they want to see a summary of the survey responses they entered.

</td></tr><tr><td>

Order

</td><td>

Number that indicates the order in which survey configurations run. If there are multiple chat survey configurations, the system runs the first survey found, from lowest to highest order.

</td></tr><tr><td>

Requester ended

</td><td>

Option that specifies if the post chat survey should always run regardless of who ends the chat.-   True: Survey should run when either the requester or the agent ends the chat.
-   False: Survey should run only when the agent ends the chat.


</td></tr><tr><td>

Condition mode

</td><td>

Type of condition that determines the conversational survey presented to requesters.-   Simple: Specify a condition using the condition builder.
-   Advanced: Specify a JavaScript scripted condition.


</td></tr><tr><td>

Condition

</td><td>

Condition that determines the conversational survey displayed to requesters.Use the condition builder to select the conditions to be applied. The fields available for selection are based on the Chat service channel.

</td></tr><tr><td>

Script

</td><td>

JavaScript condition statement that specifies the condition for using this chat survey. The condition must evaluate to true.

</td></tr><tr><td>

Survey

</td><td>

List of the chat surveys available. Choose the post-chat survey to be presented to your requesters.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

When a live agent ends the chat session, the post-chat survey \(configured for the chat queue\) is presented to the requester. When the requester submits the post-chat survey, the chat session ends for the requester. The Interaction Related Records list stores the post-survey chat results and creates a related record that links the assessment to the live agent \(fulfiller\).

**Parent Topic:**[General chat settings](../concept/ci-configuring-chat-features.md)

