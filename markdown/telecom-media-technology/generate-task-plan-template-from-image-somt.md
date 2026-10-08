---
title: Generate a task plan template from an image
description: Upload an image of the fulfillment journey so the ServiceNow Otto for Sales CRM for Telecommunications AI agent can convert it into a task plan template for a specification and order action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/generate-task-plan-template-from-image-somt.html
release: brazil
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 5
breadcrumb: [Image to task plan template AI agent, Standalone AI agents, Use agentic workflows, Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Generate a task plan template from an image

Upload an image of the fulfillment journey so the ServiceNow Otto for Sales CRM for Telecommunications AI agent can convert it into a task plan template for a specification and order action.

## Before you begin

A published product specification must exist and be mapped to a published product offering.

A customer order for the product offering must be approved. If no fulfillment flow or published task plan template exists for the specification and order action, the system creates an intermediate task on the order line item. The AI agent then processes this task.

A user for the task plan template AI agent must exist and have the required roles. This user isn't provided with the application, so you create it.

Image guidelines:

-   Size of the image must be less than 10MB.
-   Format of the image must be PNG, PDF, or JPG.
-   Connecting lines between tasks and nodes must not overlap.
-   The agent treats the first, or root, node in the image as the specification and every other node as a task.

Role required: sn\_task\_plan.admin, sn\_prd\_pm.product\_catalog\_admin, and admin or impersonator \(to impersonate the AI agent user\).

## About this task

When no template or flow is associated with a specification for a domain order, the system generates an intermediate task. The intermediate task has the short description **Placeholder task to trigger the fulfillment AI agent**.

## Procedure

1.  Open the intermediate task from the **Order Tasks** tab of the order line item.

    Don't open the task with the short description **Placeholder task to trigger the enrichment AI agent**, which a different AI agent uses.

2.  In the **Assigned to** field, select the AI agent user, and then select **Update**.

    Assigning the task to that user starts the AI agent. Don't select **Assign to me**. To start the agent manually instead, navigate to **All** &gt; **Product Catalog Management** &gt; **Specifications** &gt; **Product Specifications**, open the product specification record, and select **Add Fulfillment Journey**.

3.  Impersonate the AI agent user.

    Select your user avatar, and then select **Impersonate user**. In the **Select a user** field, search for and select the AI agent user, and then select **Impersonate user**.

    The Service Operations Workspace home page opens.

4.  In the ServiceNow Otto panel, open the conversation for the intermediate task.

    The conversation title starts with the intermediate task number, followed by Design Telecom Order Fulfillment Template. The agent starts automatically when the task is assigned to the AI agent user.

5.  When the agent asks how to create the template, select **Upload an image for task plan template creation**.

    The agent offers this choice only when it starts automatically from the intermediate task. To use historical data instead, see [Generate a task plan template without an image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/generate-task-plan-template-without-image-somt.md).

6.  Upload an image of the fulfillment journey, showing the tasks and their dependencies in a clear chart with clear text visualization.

    To upload the file, select **Click here to upload a file**. The agent extracts the tasks and their dependencies from the image. The process can take a few minutes. The agent then lists each task and the tasks that it depends on. You can't edit the dependencies while the agent is running.

7.  When the agent lists the order intent types, select the order action for the template.

    The list includes **Add**, **Change**, **Disconnect**, **Cancel**, **Suspend**, and **Resume**. You can also enter the action in the reply field. The template applies only to orders for this specification that use the selected action.

    The agent creates the task plan template and displays its number, the number of tasks and dependencies, and a link to the template.

8.  Review the task plan template that the agent generates from the image, including its task dependency graph, in the Task Plan Template UI.

    The template is presented in **Draft** state. To open it, use the link that the agent provides. In the template, you can add template items and change dependencies.

    -   Check the **Specification** and **Action** conditions. You can't change the conditions after you publish the template.
    -   On the **Template Items** tab, check the tasks. To add a missing task, select **New**, enter a **Short description**, select Order Task \[sn\_ind\_tmt\_orm\_order\_task\] in the **Table** field, enter the task's position in the **Order** field, and select **Submit**.
    -   On the **Task Plan Template Dependencies** tab, check the dependencies. To add a missing dependency, select **New**.
    **Note:** The AI agent might not extract every task or dependency correctly, especially if parts of the image are unclear. Before you publish the template, compare its template items and dependencies with your image.

9.  Select **Publish**.

    The template state changes to **Published**, and **Publish** no longer appears on the form.


## What to do next

**Warning:** Before you close the intermediate task, publish the generated template. If you try to close the task while the template is still in **Draft** state, the system displays a warning message: `Please publish the Task Template that has been created to verify successful fulfillment journey to be triggered.` The warning doesn't prevent you from closing the task, but if you close it without publishing the template, the order isn't fulfilled.

When you close the intermediate task, the system applies the published template to the current order and generates its fulfillment tasks. The template also orchestrates any subsequent orders for the same specification and action, so the agent no longer needs to be invoked for that combination.

To close the intermediate task, open it from the **Order Tasks** tab of the order line item and select **Close**. The system adds an order task for each template item to the order line item.

For later orders with the same specification and order action, the system adds the template's order tasks directly and doesn't create an intermediate task for the AI agent. The system still creates the placeholder task for the enrichment AI agent.

To stop applying the template to future orders, open the template and select **Deactivate**.

