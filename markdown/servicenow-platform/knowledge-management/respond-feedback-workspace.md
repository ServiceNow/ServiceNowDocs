---
title: Work on a feedback task in Agent Workspace
description: Start working on a feedback task, request clarifications, and resolve or close the feedback task in Agent Workspace. You can view all feedback tasks assigned to you or your ownership group.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Authoring a knowledge article in Agent Workspace, Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Work on a feedback task in Agent Workspace

Start working on a feedback task, request clarifications, and resolve or close the feedback task in Agent Workspace. You can view all feedback tasks assigned to you or your ownership group.

## Before you begin

You must have contribute access to the knowledge base that stores the knowledge article you want to work on.

Role required: agent\_workspace\_user

## About this task

A feedback task is created based on the following types of feedback sources.

<table id="table_cx2_zgs_rjb"><thead><tr><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User feedback

</td><td>

Knowledge article was marked as not helpful or given low ratings.

</td></tr><tr><td>

Internal feedback

</td><td>

Knowledge article was flagged.

</td></tr><tr><td>

Knowledge gap

</td><td>

Knowledge gap feedback task was created for one or more tasks using the Knowledge Demand Insights feature.

</td></tr><tr><td>

Knowledge gap - manual

</td><td>

Knowledge gap feedback task was created manually from a task, such as a customer service case or an incident.

</td></tr><tr><td>

Unsuccessful search

</td><td>

Knowledge gap feedback task was created from the Unsuccessful Searches report in the Self-Service Analytics for Customer Service dashboard.

</td></tr><tr><td>

Other

</td><td>

Feedback for a knowledge article from other sources.**Note:** When you upgrade your instance, for any existing records that don't have any feedback task type set or don't match with supported types, the feedback task type is automatically set to **Other**.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Agent Workspace** &gt; **Agent Workspace Home**.

2.  Click **Lists** &gt; **Knowledge** &gt; **My Tasks - Feedback**.

3.  Click the link to a feedback task number.

4.  On the Knowledge Feedback Task form, review the feedback given by the submitter.

5.  Work on the feedback task.

<table id="choicetable_p3v_5sb_vjb"><thead><tr><th align="left" id="d584860e191">

To

</th><th align="left" id="d584860e194">

Do this

</th></tr></thead><tbody><tr><td id="d584860e200">

**Start working on the feedback task**

</td><td>

From the State list, select **Work in progress**. You can save the feedback task, edit the knowledge article for which the feedback task was added, or create another knowledge article from a feedback task if the information in the existing article is irrelevant or obsolete. For more information, see [Create a knowledge article from a feedback task in Agent Workspace](create-article-feedback-agent.md) and [Edit a knowledge article from a feedback task in Agent Workspace](edit-article-feedback-agent.md).

</td></tr><tr><td id="d584860e229">

**Request clarification from the feedback submitter**

</td><td>

1.  From the State list, select **Awaiting information**.
2.  In the **Additional comments** field, enter the information you need from the submitter of the feedback task.
 When you save the feedback task form, an email notification is sent to the feedback task submitter.

</td></tr><tr><td id="d584860e256">

**Resolve the feedback task**

</td><td>

1.  From the State list, select **Resolved**.
2.  From the Resolution Code list, select a code for resolving the feedback task.
3.  In the **Resolution notes** field, enter the reason for the resolution.
 When you save the feedback task form, an email notification is sent to the feedback submitter to accept or reject the feedback.

 **Note:** If the submitter accepts the feedback resolution, the state for the feedback task is automatically set to **Closed**.

</td></tr><tr><td id="d584860e292">

**Close the feedback task without the submitter having to accept the feedback resolution**

</td><td>

From the State list, select **Closed**.

</td></tr></tbody>
</table>6.  In the Compose section, enter comments, which all viewers can see, or work notes, which only internal users can see.

7.  Track the time spent on each state for a feedback task by clicking the **Knowledge Feedback Task Metrics** tab and then clicking a link to the state in the **Value** column.

8.  Click **Save**.


## Result

The feedback task is updated.

**Related topics**  


[View a knowledge article in Agent Workspace](view-article-agent.md)

