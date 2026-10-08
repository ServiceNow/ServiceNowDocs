---
title: Assigning work to an AI specialist
description: You can assign work to an AI specialist in one of three ways, depending on your current work assignment procedures.Manually assign specific records to an AI specialist by changing the Assigned to field when you need to override automatic assignment rules.Create an assignment rule to route matching tasks to an AI specialist automatically, without setting the Assigned to field on each record.Add an AI specialist to an existing Advanced Work Assignment \(AWA\) assignment rule so that it can receive work items alongside your human agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/work-assign-aiw.html
release: brazil
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 4
keywords: [AI specialist, manual assignment, assign work]
breadcrumb: [Configure, Autonomous Workforce, AI Agent Studio \(legacy\), AI agents and agentic workflows, Enable AI Experiences]
---

# Assigning work to an AI specialist

You can assign work to an AI specialist in one of three ways, depending on your current work assignment procedures.

AI specialists can't assign themselves work, even if they've been put into an assignment group. There are three ways you can assign work to an AI specialist.

1.  Manual assignment. You can change the user in the **Assigned to** field to your AI specialist on a record form or list. A service desk manager or team lead can assign work to the AI specialist just as they would assign work to human agents on their team.

2.  Assignment rules. Assignment rules automatically assign work on your instance based on predefined conditions. They are applied whenever a task that isn't already assigned is created or updated. If you have multiple assignment rules, the one with the lowest order takes precedence.

3.  Advanced Work Assignment \(AWA\). AWA assigns work based on more context than simple assignment rules, such as an agent's availability, capacity, and skills. Configuring AWA involves creating and managing service channels, work item queues, routing conditions, and assignment criteria.


With manual assignment, you control exactly which records an AI specialist works on. This works best when doing initial testing to see how an AI specialist handles a particular task type or subject. After you've established trust, you can allow the AI specialist to work at a larger scale by creating assignment rules or configuring AWA.

To have AWA assign work to an AI specialist, configure AWA first. You can then add the AI specialist to existing work queues, like another member of the team. If you don't already have AWA set up on your instance, assignment rules require less configuration than setting up AWA for AI specialists alone.

## Manually assign work to an AI specialist

Manually assign specific records to an AI specialist by changing the Assigned to field when you need to override automatic assignment rules.

### Before you begin

Role required: itil\_admin

### Procedure

1.  Navigate to the table containing the record to assign.

    You can assign AI specialists to records in tables such as the Incident \[incident\] table.

2.  Open the record for the AI specialist to work on.

3.  In the **Assigned to** field, enter the name of the AI specialist.

    If the AI specialist does not appear in the **Assigned to** list, verify that the AI specialist is active and has the appropriate capabilities configured for this record type.

4.  Save the record.


### Result

The record is assigned to the AI specialist. The AI specialist processes the record according to its configured capabilities and workflows.

## Create an assignment rule for an AI specialist

Create an assignment rule to route matching tasks to an AI specialist automatically, without setting the Assigned to field on each record.

### Before you begin

Role required: assignment\_rule\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Assignment**.

2.  Select **New**.

3.  In the **Name** field, enter a name for your assignment rule, such as `AI L1 Service Desk`.

4.  In the **Applies to** tab, select the table and filter conditions that identify the tasks for the AI specialist to handle.

5.  In the **Assign to** tab, enter the name of the AI specialist in the **User** field.

6.  Select **Submit** to create the assignment rule.


### Result

The assignment rule routes matching tasks to the AI specialist automatically.

## Configure Advanced Work Assignment for an AI specialist

Add an AI specialist to an existing Advanced Work Assignment \(AWA\) assignment rule so that it can receive work items alongside your human agents.

### Before you begin

This procedure applies when service channels and work item queues are already configured in AWA. For instructions on creating new ones, see [Create a service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/awa-create-service-channel.md) and [Create a work item queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/awa-create-queue.md).

Role required: awa\_admin

### Procedure

1.  Confirm that the AI specialist has the awa\_agent role.

    Navigate to **All** &gt; **User Administration** &gt; **Users**, find and open the user record for the AI specialist, and check the roles in the Roles related list.

2.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Home** &gt; **Assignment rules**.

3.  Select **New** to open the new record form or open an existing assignment rule.

4.  In the **Auto-assign handling** tab, select **Enable auto-assign work items**.

5.  In the **Manage AI agents** tab, select **Include AI agents**.

6.  In the **Manage AI agents** tab, select **Prioritize AI agents**.

    Choosing to prioritize AI agents routes relevant work to the AI specialist first. The AI specialist then triages the task and determines whether it can propose an acceptable solution. If the AI specialist can't propose a solution, or if the task is outside its configured capabilities, it can reassign the task to a human agent or a different assignment group. For steps on configuring the routing criteria for reassignment, see [Configure AI specialist tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/modify-aiw-tasks-new.md).

    If you don't choose to prioritize AI agents, the AI specialist can still be assigned work from the work item queue.

7.  Select **Save**.

8.  Set the maximum capacity for the AI specialist.

    See [Override agent capacity for selected agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/awa-change-agent-capacity.md).


### Result

Your AI specialist is added to the AWA assignment rule as an eligible assignee.

### What to do next

You can track an AI specialist's performance and the records it works on in AI Agent Studio. See [View performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/view-aiw-performance-new.md) and [View activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/view-aiw-activity-new.md).

