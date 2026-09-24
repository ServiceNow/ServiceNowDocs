---
title: Trigger a flow from a task plan template item
description: Configure a flow to run automatically when a task plan template item creates a record. A single step of a task plan can be completed by a flow, a subflow, or an AI agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/associate-a-flow-with-a-task-plan-template-item.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [task plan template, flow, template item, automation, AI agent, subflow]
breadcrumb: [Flow-based automation for task plan template items, Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Trigger a flow from a task plan template item

Configure a flow to run automatically when a task plan template item creates a record. A single step of a task plan can be completed by a flow, a subflow, or an AI agent.

## Before you begin

Role required: `sn_task_plan.admin` or `sn_task_plan.creator` role to configure the template item, and a role that allows you to create and activate flows in Workflow Studio.

-   A task plan template with at least one template item. Note the number of the template item that the flow must run for, such as PI0001001.
-   A reference field on the target table of the template item that points to the Template Item table `[sn_task_plan_template_item]`. This field is available by default on some tables. If the target table does not have it, create it before you start.

## About this task

Use this procedure when one step of a task plan needs work that the task plan template can't do on its own. Examples include validating data in an external system or handing the task to an AI agent.

You configure the template item to stamp its number on each record it creates, and then create a flow that uses that stamped value as its trigger condition. For more information, see [Flow-based automation for task plan template items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-flows-with-task-plan-template-items.md).

## Procedure

1.  Configure the template item to stamp its number on the records it creates.

    1.  Navigate to **All** &gt; **Task Plan Templates** &gt; **Draft Task Plan Templates**.

    2.  Select a task plan template record number to display the record.

    3.  Select the **Template items** tab and open the template item that the flow must run for.

    4.  In the **Template item field** field, select the field on the target table that references the template item.

        For more information about this field, see [Template item form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/task-plan-template-item-form.md).

    5.  Select **Save**.

2.  In Workflow Studio, create a flow.

3.  Define the trigger for the flow.

    1.  In the **Trigger** field, select **Created**.

    2.  In the **Table** field, select the target table of the template item.

    3.  Add a condition where the reference field that you selected in step 1 is the number of the template item.

        For example, if the target table is the Task \[task\] table and the template item is PI0001001, the condition is **\[Template Item\] \[is\] \[PI0001001\]**.

    4.  Select **Done**.

4.  Add the actions that the flow must perform, and then select **Done**.

    The actions can update the record that triggered the flow, call an existing subflow, or call an AI agent. For example, a flow can set the **Assigned to** and **Priority** fields on the new task and then send an email notification to the assigned agent.

    To pass the new record to a subflow, map the task record from the trigger to the subflow input.

5.  Save and activate the flow.

6.  Repeat this procedure for each template item in the task plan template that needs its own flow.


## Result

When the task plan template is applied, the template item creates its record and the system stamps the template item number in the reference field on that record. The record then meets the trigger condition of the flow, and the flow runs its actions.

## What to do next

To confirm that the flow ran, open the record that the template item created. The reference field displays the number of the template item, and the fields that the flow updates display their new values.

