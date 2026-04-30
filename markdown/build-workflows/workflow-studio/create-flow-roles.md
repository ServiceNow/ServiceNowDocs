---
title: Create a flow with roles
description: Create a flow or subflow that runs with assigned roles. Assigning roles enables you to create a user-initiated flow that runs with its own roles rather than the user's roles.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a flow in Workflow Studio, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a flow with roles

Create a flow or subflow that runs with assigned roles. Assigning roles enables you to create a user-initiated flow that runs with its own roles rather than the user's roles.

## Before you begin

Role required: flow\_designer or admin

## About this task

Create a user-initiated flow that runs with its own roles and not the roles of the user. For more information about assigning roles to a flow, go to [Flow roles](../concept/flow-roles.md). For example, allow a flow to run with the itil role so that it can access data belonging to IT Service Management applications such as incidents and problems.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click **+ New** &gt; **Flow** or **+ New** &gt; **Subflow**.

3.  On the Flow Properties form, define the Name, Application, and Description for the flow.

    For more information, see [Create a flow in Workflow Studio](create-flow.md).

4.  Expand the **Additional properties** section.

5.  In the **Run As** field, select **User who initiates session**.

    Role selection is not available if the **System User** option is selected in the **Run As** field.

6.  In the **Run with roles** field, select one or more roles that you want the flow to use while it runs.

    ![Run with roles property using the itil role.](../images/example-flow-properties-run-with-roles.png)

    The roles you select replace any roles that the user normally has. If you don't select any roles, then the flow runs with the roles normally associated with the user.

    **Tip:** If you have the Explicit Roles plugin \(com.glide.explicit\_roles\) activated, add the snc\_internal role to your flow.

    For example, an inbound email flow normally runs as an existing user or as the Guest user when there is no existing user. Guest users don't have access to IT Service Management data such as incidents and problems. Running a flow without any roles may produce access errors when the flow tries to access restricted data on the guest user's behalf. Running a flow with a role such as itil ensures that the flow can access the data it needs.

7.  Select **Build Flow**.


## What to do next

![Sample flow execution details of a flow that ran with the itil role.](../images/example-flow-execution-details-run-with-roles.png)

Continue to build and test your flow until you're ready to activate it. You can modify your flow's roles at any time by updating the Flow Properties form.

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

