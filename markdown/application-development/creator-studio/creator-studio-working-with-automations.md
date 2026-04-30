---
title: Working with automation in Creator Studio
description: How do you simplify and streamline tasks for fulfillers? Use automation! For example, you can have a task assigned automatically to someone based on what type of request it is. We’ll use playbooks to accomplish adding this automation to your app.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 8
keywords: [app automation, app playbook, workflow automation]
breadcrumb: [Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Working with automation in Creator Studio

How do you simplify and streamline tasks for fulfillers? Use automation! For example, you can have a task assigned automatically to someone based on what type of request it is. We’ll use playbooks to accomplish adding this automation to your app.

**Summary:** After reading this section, you'll understand how to use [automation](creator-studio-glossary.md#) to do the following things:

-   Use playbooks to guide agents and fulfillers through processes from start to finish, improving the customer experience and the way tasks are carried out.
-   Create a consistent process for your tasks or activities to be carried out.
-   Consolidate business decisions and processes across the organization.

**Note:** Because playbooks are based on forms, you must publish a form \(mark it as ready\) before you use it to create a playbook. For more information, see [Publish a form for your app in Creator Studio](../task/creator-studio-publish-form.md).

[Playbooks](creator-studio-glossary.md#) are a series of steps triggered by an event. You can add multiple playbooks to an app if needed

**Key terms:**

-   **Activity**

    Activities in a playbook complete automated tasks, such as obtaining approvals, assigning records, and sending email.

-   **Automation**

    Tasks or requests moving through a workflow without manual intervention.

-   **Playbook**

    A set of actions based on an initiating action called a trigger.

-   **Record**

    A task or request that must be acted on. All rows in ServiceNow tables are individual records. Records have different states depending on what actions have been taken.

-   **Trigger**

    The event that starts making the playbook run.

-   **Workflow**

    The path a record takes from creation to completion.


## What is automation?

Automation in Creator Studio enables you to create simplified playbooks, which are basic, automatic workflows. Simple playbooks consist of a trigger \(such as a record changing states, or a user choosing a specific answer for a question\) and an activity \(such as the record being assigned to a new person\). Playbooks enable you to add the following:

-   Activities to your automation to define the workflow’s path.
-   Decisions to create different paths, or branches, depending on the decision's outcome.
-   Custom activities defined by your admin or ServiceNow AI Platform owner.

Playbooks take the guess work out of assigning tasks and help users focus on the tasks and information that matter to their job. A well-designed playbook can do these things:

-   Automatically start or trigger changes for different types of records, such as task assignments.
-   Reuse activities and business decisions from other workflows you’ve already created.
-   Clearly show the next steps that fulfillers must take to move to the next step of completing the record’s life cycle.

There are several types of activities that you can add to playbooks that, when paired with decisions, remove the manual thinking behind what to do next when addressing tasks. Depending on your configuration, some of the activities you can add include:

-   Request approval for a task
-   Assign the task to someone
-   Create a new task as a next step
-   Send an email
-   Choose a custom action configured by your admin

**Note:** In addition to creating custom activities, your admin can also hide standard activities, so you may not see all of the above options.

You can even use answers from a playbook's associated form to power activities. For example, if someone's requesting a gift box and they answer `Yes` to the question "Do you eat meat?" then you can create an Assign to activity to route the gift box to the Meat department for fulfillment.

You can also use a placeholder activity for more complex activities that must be configured outside of Creator Studio, or for another activity to be swapped in later.Complex activities are configured in a different tool called Workflow Studio.

## What goes into building automation?

Automations in Creator Studio include the following parts.

<table id="table_gdk_c1g_l1c"><thead><tr><th>

Concept

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Playbook

</td><td>

An automatic workflow that guides users through tasks based on the record's status changes. Find out more about creating playbooks in [Add an automated playbook to an app in Creator Studio](../task/creator-studio-add-automation.md).

</td></tr><tr><td>

Trigger

</td><td>

The event that specifies when the playbook should start running, such as when a form is submitted or updated to a specific status. Check out [Edit the trigger for a playbook in Creator Studio](../task/creator-studio-add-trigger-automation.md) for more information.

</td></tr><tr><td>

Activity

</td><td>

The thing that happens during the playbook, such as assigning a task or requiring approval.**Note:** If you're already familiar with optional activities in playbooks, that’s great! However, to keep automations streamlined and simple, Creator Studio doesn't support optional activities. If you must create optional activities, you can add a placeholder activity in Creator Studio and then edit the placeholder in Workflow Studio or swap it out for another activity later in Creator Studio.

Additionally, admins can create custom activities for you to include in a playbook.

Learn how to add activities in [Add activities to an app's playbook in Creator Studio](../task/creator-studio-add-activities-automation.md).

</td></tr><tr><td>

Decision

</td><td>

A series of inputs, conditions, and results that create different branches, or conditional paths that users follow based on the decision's outcome. Get the scoop on adding decisions in [Add a decision to an app's playbook in Creator Studio](../task/creator-studio-add-decision-automation.md).

</td></tr><tr><td>

Branch

</td><td>

A distinct path from a decision's outcome, or what happens for each of the decision's possible choices. For more information, see [Add a decision to an app's playbook in Creator Studio](../task/creator-studio-add-decision-automation.md).

</td></tr><tr><td>

Parallel process

</td><td>

Branches for activities and stages that run in parallel to another branch of activities. Learn about parallel processes in [Add a parallel process to an app's playbook in Creator Studio](../task/creator-studio-decision-parallel-process-add.md).

</td></tr><tr><td>

Connectors

</td><td>

Lines that connect activities and decisions in a playbook that enable you to add more activities, decisions, and parallel processes. You can drag connectors between activities to create parallel activities.

</td></tr></tbody>
</table>## Board and Diagram views of a playbook

Creator Studio offers two ways of working with playbooks: the Board view and the Diagram view.

The Diagram view is a visually intuitive diagram that shows you the order that activities occur in the playbook. When you select an activity, such as the trigger or a decision, a modal pops up where you can edit its details. You must use the Diagram view to add decisions.

![A playbook in Creator Studio in Diagram view](../image/crs-playbook-diagram.png "Diagram view of the playbook")

The Board view is a more traditional layout, which shows each activity as a card in the navigation panel. When you select an activity, for example a task, its editable details appear in the canvas for you to work with them. You must use the Board view to rearrange activities.

![A playbook in Creator Studio in Board view](../image/crs-playbook-board.png "Board view of the playbook")

This help document will primarily give instructions using the Diagram view, with alternate directions on how to complete automation tasks in the Board view.

## Where do playbooks run in the ServiceNow AI Platform?

Users work on requests in the Request App Workspace on the ServiceNow AI Platform, which lists a record for each request. The playbooks run on the specified records in the app's workspace category.

Specifically, the **Catalog tasks** tab of the record details walks users through the activities they must do to complete the task and close the record.

-   **[Workflow for creating automations in Creator Studio](../task/creator-studio-automations-workflow.md)**  
Provide your organization's fulfillers with guidance when addressing records generated from the app by adding automated playbooks to it.
-   **[Add an automated playbook to an app in Creator Studio](../task/creator-studio-add-automation.md)**  
Create an automated playbook, which is a process that runs whenever a record is created or updated by the app's specified form.
-   **[Copy an automated playbook in Creator Studio](../task/creator-studio-duplicate-automation.md)**  
Duplicate an existing playbook and make small changes to it, which may be faster than creating an entirely new automated playbook.
-   **[Add activities to an app's playbook in Creator Studio](../task/creator-studio-add-activities-automation.md)**  
Add activities to an app's playbook to specify what the automation does to the designated record type. An activity defines what actually happens when a playbook executes.
-   **[Add a decision to an app's playbook in Creator Studio](../task/creator-studio-add-decision-automation.md)**  
Add decisions, which are if/then conditions, to define branches, or different paths of an automation's playbook in Creator Studio.
-   **[Add a parallel process to an app's playbook in Creator Studio](../task/creator-studio-decision-parallel-process-add.md)**  
Create parallel processes in Creator Studio to make things happen in your app at the same time.
-   **[Edit the trigger for a playbook in Creator Studio](../task/creator-studio-add-trigger-automation.md)**  
Define the trigger for a playbook in Creator Studio to specify what makes the playbook start running.
-   **[Edit a playbook in Creator Studio](../task/creator-studio-edit-automation.md)**  
Update a playbook to change its settings, or rearrange or remove tasks, to make it work for your app.
-   **[Activate a playbook in Creator Studio](../task/creator-studio-activate-automation.md)**  
Activating a playbook means that it will run when its related form is created or updated on your non-production, development instance. However, the app must still be deployed to production.
-   **[Delete a playbook in Creator Studio](../task/creator-studio-delete-automation.md)**  
Delete a playbook to remove it from the app completely.

**Parent Topic:**[Building apps with Creator Studio](building-apps-with-creator-studio.md)

