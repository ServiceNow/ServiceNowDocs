---
title: Create a learning task
description: Create learning tasks for agents to keep track of their learning activities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/create-learning-task-configurable-wfo-cs.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Coaching with Learning, Using Coaching, Coaching, Workforce Optimization for Customer Service, Agent management, Use, Customer Service Management]
---

# Create a learning task

Create learning tasks for agents to keep track of their learning activities.

## Before you begin

Role required: sn\_lc.task\_creator

## About this task

Set learning task completion due dates to include or exclude weekends using the **exclude\_weekends\_on\_learning\_task\_due\_date** system property. For more information, see [Workforce Optimization for Customer Service Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/components-installed-configurable-wfo-cs.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Manager Workspace**.

2.  Click the Coaching \(\[Omitted image "coaching-new.png"\] Alt text: Coaching icon.\) icon.

3.  Click **Learning Tasks** and select **All Tasks**.

4.  Create a learning task.

    1.  Click **New**.
    2.  Fill in the following fields.

<table id="table_pr4_zgk_bpb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assigned to

</td><td>

Name of the agent to whom you want to assign the learning task.

</td></tr><tr><td>

Course item

</td><td>

The course that needs to be completed by the agent.

</td></tr><tr><td>

Due date

</td><td>

Date when the agent must complete the course. Default is 5 days after the creation of the learning task. This value is calculated from the **Days to Complete** field for the course item. The due date field is highlighted as follows:-   Green—if the task is due before the current day.
-   Yellow—if the task is due on the current day.
-   Red—if the task is due after the current day.


</td></tr><tr><td>

Catalog

</td><td>

The catalog that contains the course item for the learning task.

</td></tr></tbody>
</table>5.  Click **Save**.


**Parent Topic:**[Coaching with Learning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/workforce-learning-configurable-wfo-cs.md)

