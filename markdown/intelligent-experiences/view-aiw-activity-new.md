---
title: View the activity of an AI specialist in AI Agent Studio
description: View the task execution history of an AI specialist in the new AI Agent Studio to track where and when it plans and attempts executions. You can also give feedback on its performance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/view-aiw-activity-new.html
release: zurich
topic_type: task
last_updated: "2026-08-12"
reading_time_minutes: 2
keywords: [AI specialist activity]
breadcrumb: [Use in AI Agent Studio, Use, Autonomous Workforce, AI Agent Studio, Enable AI experiences]
---

# View the activity of an AI specialist in AI Agent Studio

View the task execution history of an AI specialist in the new AI Agent Studio to track where and when it plans and attempts executions. You can also give feedback on its performance.

## Before you begin

Role required: sn\_aia.admin

## About this task

Monitoring AI specialist activity allows you to identify where your AI specialist is being used on which records.

For a given execution, you can rate the work of the AI specialist as either helpful \(thumbs up\) or not helpful \(thumbs down\) in the **Feedback** field of the list.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the AI specialist you want to preview.

3.  In the node view, select the first node of the AI specialist.

    The first node contains the main configuration settings for the AI specialist. The other nodes represent the individual agents that comprise the underlying architecture and don't require access to view the AI specialist's activity.

4.  Scroll down to the **Activity** section in the AI specialist guided setup.

    \[Omitted image "aiw-aias-2-activity.png"\] Alt text: Activity page of an AI specialist with columns for associated record, state, state reason, assigned to, created time, and feedback

5.  Review the activity of the AI specialist.

    AI specialist activity is presented as a filtered list that includes all records related to the AI specialist. You can add more filters to narrow down the activity further.

    You can sort by any of the list columns by selecting the column name.

    If the execution state is not **Completed**, a reason is given to explain the state. Possible reasons include "failed execution" or "no activity."

    You can give feedback on any given activity item. Select the thumbs up icon \[Omitted image "nap-thumbs-up.png"\] for positive feedback or the thumbs down icon \[Omitted image "nap-thumbs-down.png"\] to give negative feedback. If you select the thumbs down icon, you can specify exactly why you have given it that rating. After selecting a reason, you can also add a comment to detail the issue further.

    \[Omitted image "aiw-aias-activity-neg-feedback.png"\] Alt text: Negative feedback response form

    Possible reasons for negative feedback include:

    -   Missed important details
    -   Included irrelevant details
    -   Put details in wrong places
    -   Made up things that didn't happen
    -   Other

## What to do next

If you want to change which records the AI specialist picks up, you can change the capabilities or assignment groups in the AI specialist's profile. See [Edit the profile of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/modify-aiw-profile-new.md) for more information.

To learn more about changing the specific tasks that the AI specialist performs on a record, see [Edit the tasks of an AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/modify-aiw-tasks-new.md).

You can test the AI specialist on a specific record of your choosing by [previewing the AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/test-aiw-ais-new.md).

