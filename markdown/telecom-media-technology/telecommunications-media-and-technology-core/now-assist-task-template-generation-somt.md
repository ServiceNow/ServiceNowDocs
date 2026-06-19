---
title: Now Assist for Sales CRM for Telecommunications AI agent Image to task plan template AI agent
description: Use the AI agent to create a task plan template for a given specification based on the uploaded image file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/telecommunications-media-and-technology-core/now-assist-task-template-generation-somt.html
release: australia
product: Telecommunications, Media and Technology Core
classification: telecommunications-media-and-technology-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Standalone AI agents, Use agentic workflows, Now Assist for Sales CRM for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Now Assist for Sales CRM for Telecommunications AI agent Image to task plan template AI agent

Use the AI agent to create a task plan template for a given specification based on the uploaded image file.

## Image to task plan template AI agent overview

This agent processes uploaded image file, extract tasks and tasks dependencies and store them as a task plan template for a given specification and order action.

The AI agent integrates with order action catalogs, file upload services, and template management systems to produce standardized task plan templates with dependency graphs and action mappings. NOW LLM does not support this agent.

The uploaded image should define the tasks and the tasks flow and dependency in a clear chart, with clear text visualization.

From the image the agent always expects the first node or the root node as the specification and not tasks and all others will be tasks.

\[Omitted image "task-plan-template-1.jpg"\] Alt text: example image for task plan template.

Guidelines for image:

-   Size of the image must be less than 10MB.
-   Format of the image must be PNG, PDF, JPG.
-   Connecting lines of tasks and node must not overlap.

    \[Omitted image "task-plan-template-2.jpg"\] Alt text: Connecting lines of tasks and node must not overlap.

    \[Omitted image "task-plan-3.png"\] Alt text: images with intersection or overlapping lines aren't supported by agent.


To modify the Image to task plan template AI agent,  and adjust the settings according to your requirements.

To add tools and information, see  for details.

Role required: sn\_task\_plan.admin and sn\_prd\_pm.product\_catalog\_admin

**Important:** In the select channels and status page, make sure that the **Active** button is turned on to activate the AI agent.

## Image to task plan template AI agent

To access the AI agent:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Image to task plan template AI agent**.

## Testing the AI agent

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Test use cases**.

To test the use case, see .

