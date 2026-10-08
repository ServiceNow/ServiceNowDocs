---
title: Generate a task plan template without an image
description: If no fulfillment journey image is available for a specification, use the ServiceNow Otto for Sales CRM for Telecommunications AI agent to generate a task plan template from tasks used in similar past orders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/generate-task-plan-template-without-image-somt.html
release: brazil
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 4
breadcrumb: [Image to task plan template AI agent, Standalone AI agents, Use agentic workflows, Use, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Generate a task plan template without an image

If no fulfillment journey image is available for a specification, use the ServiceNow Otto for Sales CRM for Telecommunications AI agent to generate a task plan template from tasks used in similar past orders.

## Before you begin

A published product specification must exist and be mapped to a published product offering.

A customer order for the product offering must be approved. If no fulfillment flow or published task plan template exists for the specification and order action, an intermediate task is created for the AI agent.

A user for the task plan template AI agent must exist and have the required roles. This user isn't provided with the application, so you create it.

Role required:

-   sn\_task\_plan.admin
-   sn\_prd\_pm.product\_catalog\_admin
-   admin or impersonator, to impersonate the AI agent user

## About this task

When no template or flow is associated with a specification for a domain order, the system generates an intermediate task. Use that task to define a template for the specification and order action. You can also start the workflow manually from the product specification record. The intermediate task has the short description **Placeholder task to trigger the fulfillment AI agent**.

Use this procedure when no fulfillment journey image is available for the specification; otherwise, see [Generate a task plan template from an image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/generate-task-plan-template-from-image-somt.md).

## Procedure

1.  Open the intermediate task from the **Order Tasks** tab of the order line item.

    Don't open the task with the short description **Placeholder task to trigger the enrichment AI agent**, which a different AI agent uses.

2.  In the **Assigned to** field, select the AI agent user, and then select **Update**.

    Assigning the task to that user starts the AI agent. Don't select **Assign to me**. To start the agent manually instead, navigate to **All** &gt; **Product Catalog Management** &gt; **Specifications** &gt; **Product Specifications**, open the product specification record, and select **Add Fulfillment Journey**.

3.  Impersonate the AI agent user.

    Select your user avatar, and then select **Impersonate user**. In the **Select a user** field, search for and select the AI agent user, and then select **Impersonate user**.

    The Service Operations Workspace home page opens.

4.  In the ServiceNow Otto panel, open the conversation for the intermediate task.

    The conversation title starts with the intermediate task number, followed by Design Telecom Order Fulfillment Template. The agent is already running for the product order.

5.  When the agent displays a prompt for how to create the template, select **Use historical data for task plan template creation**.

    This choice appears only when the agent starts automatically from the intermediate task. To upload an image instead, see [Generate a task plan template from an image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/generate-task-plan-template-from-image-somt.md).

6.  If prompted, select the order **action**.

    The agent prompts you to select the action only when you start the workflow from the specification record page. When the workflow starts automatically from an order journey's placeholder task, the agent instead determines the action from the order line item and doesn't prompt for it. The list includes **Add**, **Change**, **Disconnect**, **Cancel**, **Suspend**, and **Resume**.

7.  Let the agent search historical order tasks for the closest matching specification and action.

    The agent presents those tasks in a task plan template draft. Unlike a template generated from an image, a template generated this way doesn't include task dependencies.

8.  Review the draft template in the Task Plan Template UI and [add the dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/add-dependencies-between-template-item.md) between template items.

    The agent fills in all required fields on the generated template and template items automatically, based on the matched tasks and specification.

9.  Select **Publish**.

    The template state changes to **Published**, and **Publish** no longer appears on the form.


## What to do next

**Warning:** Before you close the intermediate task, publish the generated template. If you try to close the task while the template is still in **Draft** state, the system displays a warning message: `Please publish the Task Template that has been created to ensure successful fulfillment journey to be triggered.` The warning doesn't prevent you from closing the task, but if you close it without publishing the template, the order isn't fulfilled.

When you close the intermediate task, the system applies the published template to the current order and generates its fulfillment tasks. The template also orchestrates any subsequent orders for the same specification and action, so the agent no longer needs to be invoked for that combination.

To close the intermediate task, open it from the **Order Tasks** tab of the order line item and select **Close**. The system adds an order task for each template item to the order line item.

For later orders with the same specification and order action, the system adds the template's order tasks directly and doesn't create an intermediate task for the AI agent. The system still creates the placeholder task for the enrichment AI agent.

To stop applying the template to future orders, open the template and select **Deactivate**.

