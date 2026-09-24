---
title: Assigning work to the L1 IT Service Desk AI Specialist
description: Assign work to the L1 IT Service Desk AI Specialist in one of three ways, depending on your current work assignment procedures.Manually assign specific records to the L1 IT Service Desk AI Specialist by changing the Assigned to field when you must override automatic assignment rules.Route work to the L1 IT Service Desk AI Specialist using assignment rules.Add the L1 IT Service Desk AI Specialist to an existing Advanced Work Assignment \(AWA\) assignment rule so that it can receive work items alongside your human agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/work-assign-l1-sd-ai-spec.html
release: brazil
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 5
keywords: [AI specialist, work assignment, assignment rules, Advanced Work Assignment, AWA, manual assignment, assignment group, service channels, work item queues, routing conditions, assignment criteria, Service Desk, AI specialist, manual assignment, assign work, assigned to field, task assignment, work assignment, AI agent assignment, assignment rules, AI specialist, work assignment, automated routing, assignment rule admin, system policy, filter conditions, task routing, Advanced Work Assignment, AWA, AI specialist, assignment rule, auto-assign, work item queue, AI agent, service channel, agent capacity, prioritize AI agents]
audience: [administrator, user, administrator, administrator]
breadcrumb: [Configure, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Assigning work to the L1 IT Service Desk AI Specialist

Assign work to the L1 IT Service Desk AI Specialist in one of three ways, depending on your current work assignment procedures.

AI specialists can't assign themselves work, even if they've been put into an assignment group. There are three ways you can assign work to the L1 IT Service Desk AI Specialist.

1.  Manual assignment. You can change the user in the **Assigned to** field to the L1 IT Service Desk AI Specialist on a record form or list. A Service Desk manager or team lead can assign work to the AI specialist just like they'd assign work to human agents on their team.

2.  Assignment rules. Assignment rules automatically assign work on your instance based on pre-defined conditions. They are applied whenever a task that isn't already assigned is created or updated. If you have multiple assignment rules, the one with the lowest order takes precedence.

3.  Advanced Work Assignment \(AWA\). AWA assigns work based on more context than simple assignment rules, such as an agent's availability, capacity, and skills. Configuring AWA involves creating and managing service channels, work item queues, routing conditions, and assignment criteria.


Manual assignment allows fine control over exactly which records the L1 IT Service Desk AI Specialist works on. This works best when doing initial testing to see how an AI specialist handles a particular task type or subject. Once you've established trust, you can allow the AI specialist to work at a larger scale by creating assignment rules or configuring AWA.

**Important:**

If you want AWA to assign work to the L1 IT Service Desk AI Specialist, it's best that you already have AWA configured so that you can add the AI specialist to existing work queues, like another member of the team. If you don't already have AWA set up on your instance, simple assignment rules can most likely cover what you need more effectively and with less effort than AWA configured just for AI specialists.

## Manually assign work to the L1 IT Service Desk AI Specialist

Manually assign specific records to the L1 IT Service Desk AI Specialist by changing the Assigned to field when you must override automatic assignment rules.

### Before you begin

Role required: itil\_admin

### Procedure

1.  Navigate to the table containing the record you want to assign.

    AI specialists can be assigned to records in tables such as Incident.

2.  Open the record you want the L1 IT Service Desk AI Specialist to work on.

3.  In the **Assigned to** field, enter the name of the AI specialist.

    If the L1 IT Service Desk AI Specialist does not appear in the **Assigned to** list, verify that the L1 IT Service Desk AI Specialist is active and has the appropriate capabilities configured for this record type.

4.  Save the record.


### Result

The record is assigned to the L1 IT Service Desk AI Specialist. The AI specialist processes the record according to its configured capabilities and workflows.

## Create assignment rules for the L1 IT Service Desk AI Specialist

Route work to the L1 IT Service Desk AI Specialist using assignment rules.

### Before you begin

Role required: assignment\_rule\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Assignment**.

2.  Select **New**.

3.  In the **Name** field, enter a name for your assignment rule, such as "L1 IT Service Desk AI Specialist."

4.  In the **Applies to** tab, select the table and filter conditions for which tasks you want the AI specialist to handle.

5.  In the **Assign to** tab, enter the name of the AI specialist in the **User** field.

6.  Select **Submit** to create the assignment rule.


### Result

Your L1 IT Service Desk AI Specialist is now automatically routed cases that match the filter conditions you set.

## Configure Advanced Work Assignment for L1 IT Service Desk AI Specialist

Add the L1 IT Service Desk AI Specialist to an existing Advanced Work Assignment \(AWA\) assignment rule so that it can receive work items alongside your human agents.

### Before you begin

The following procedure applies when AWA already has existing service channels and work item queues. For instructions on creating new ones, see [Create a service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/awa-create-service-channel.md) and [Create a work item queue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/awa-create-queue.md).

Role required: awa\_admin

### Procedure

1.  Confirm the L1 IT Service Desk AI Specialist has the AWA agent role \(awa\_agent\).

    Navigate to **All** &gt; **User Administration** &gt; **Users**, find and open the user record for the AI specialist, and check the roles in the **Roles** related list.

2.  Navigate to **All** &gt; **Advanced Work Assignment** &gt; **Home** &gt; **Assignment rules**.

3.  Select **New** to open the new record form or open an existing assignment rule.

4.  In the **Auto-assign handling** tab, select **Enable auto-assign work items**.

5.  In the **Manage AI agents** tab, select **Include AI agents**.

6.  In the same tab, select **Prioritize AI agents**.

    Choosing to prioritize AI agents routes possible relevant work to the AI specialist first. This allows the AI specialist to triage the task and evaluate its ability to propose an acceptable solution. If it isn't confident, or if the work is outside its expertise, it can reassign to a human agent or different assignment group. For steps on configuring the routing criteria for reassignment, see [Edit the tasks of an AI specialist in AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/modify-aiw-tasks-new.md).

    If you don't choose to prioritize AI agents, the AI specialist can still be assigned work from the work item queue.

7.  Select **Save** to save the record.

8.  Set the maximum capacity for the AI specialist.

    See [Override agent capacity for selected agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/awa-change-agent-capacity.md).


### Result

Your L1 IT Service Desk AI Specialist is added to the AWA assignment rule as an eligible assignee.

### What to do next

You can track the L1 IT Service Desk AI Specialist's performance and which records an AI specialist works on in AI Agent Studio. See [Review the performance of an AI specialist in AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/view-aiw-performance-new.md) and [View the activity of an AI specialist in AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/view-aiw-activity-new.md).

