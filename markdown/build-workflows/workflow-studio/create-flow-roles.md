---
title: Create a flow with roles
description: Create a flow or subflow that runs with assigned roles. Assigning roles enables you to create a user-initiated flow that runs with its own roles rather than the user's roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/create-flow-roles.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 2
breadcrumb: [Create a flow, Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Create a flow with roles

Create a flow or subflow that runs with assigned roles. Assigning roles enables you to create a user-initiated flow that runs with its own roles rather than the user's roles.

## Before you begin

Role required:

-   flow\_designer or admin to run a flow with a standard role
-   an application administrator role to run a flow with a high-security role

## About this task

Create a flow that runs with its own roles rather than just inheriting the roles of the user who starts the flow. For more information about assigning roles to a flow, go to [Flow roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-roles.md). For example, allow a flow to run with the itil role so that it can access data belonging to IT Service Management applications such as incidents and problems.

For information about application administration and the special roles that it requires, see [Application administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/application-administration.md).

## Procedure

1.  If necessary, log in with a user who has an application administrator role.

2.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

3.  Click **+ New** &gt; **Flow** or **+ New** &gt; **Subflow**.

4.  On the Flow Properties form, define the Name, Application, and Description for the flow.

    For more information, see [Create a flow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow.md).

5.  Expand the **Additional properties** section.

6.  In the **Run As** field, select **User who initiates session**.

    Role selection is not available if the **System User** option is selected in the **Run As** field.

7.  In the **Run with roles** field, select one or more roles that you want the flow to use while it runs.

    \[Omitted image "example-flow-properties-run-with-roles.png"\] Alt text: Run with roles property using the itil role.

    The roles you select replace any roles that the user normally has. If you don't select any roles, then the flow runs with the roles normally associated with the user.

    **Tip:** If you have the Explicit Roles plugin \(com.glide.explicit\_roles\) activated, add the snc\_internal role to your flow.

    For example, an inbound email flow normally runs as an existing user or as the Guest user when there is no existing user. Guest users don't have access to IT Service Management data such as incidents and problems. Running a flow without any roles may produce access errors when the flow tries to access restricted data on the guest user's behalf. Running a flow with a role such as itil ensures that the flow can access the data it needs.

8.  To add one or more application administrator roles, select **+ Add high-security roles**.

    \[Omitted image "add-high-security-roles-option.png"\] Alt text: The Add high-security roles option is after the Run with roles option

9.  In the **High-security roles** field, select one or more application administration roles that you want the flow to run with.

    \[Omitted image "example-high-security-roles-field.png"\] Alt text: The High-security roles field contains two example application administration roles for the Employee Center and the Secrets Management applications.

    **Important:** This field only displays high-security roles to users who logged in with an application administrator role.

10. Select **Build Flow**.


## What to do next

\[Omitted image "example-flow-execution-details-run-with-roles.png"\] Alt text: Sample flow execution details of a flow that ran with the itil role.

Continue to build and test your flow until you're ready to activate it. You can modify your flow's roles at any time by updating the Flow Properties form.

**Parent Topic:**[Create a flow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow.md)

