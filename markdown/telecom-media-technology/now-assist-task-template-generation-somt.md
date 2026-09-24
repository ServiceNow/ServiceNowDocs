---
title: ServiceNow Otto for Sales CRM for Telecommunications AI agent Image to task plan template AI agent
description: Use the AI agent to create a task plan template for a given specification. The agent uses an uploaded image file, or falls back to tasks from the closest matching specification when no image is available.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-task-template-generation-somt.html
release: brazil
topic_type: concept
last_updated: "2026-09-22"
reading_time_minutes: 1
breadcrumb: [Standalone AI agents, Use agentic workflows, ServiceNow Otto for Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# ServiceNow Otto for Sales CRM for Telecommunications AI agent Image to task plan template AI agent

Use the AI agent to create a task plan template for a given specification. The agent uses an uploaded image file, or falls back to tasks from the closest matching specification when no image is available.

## Image to task plan template AI agent overview

This agent processes an uploaded image, extracts tasks and task dependencies, and stores them as a task plan template for a given specification and order action. If no image is available for the specification, the agent instead searches historical order tasks for the closest matching specification and action.

The AI agent integrates with order action catalogs, file upload services, and template management systems to produce standardized task plan templates with dependency graphs and action mappings. NOW LLM does not support this agent.

To generate a template from an image, see . If no image is available, see Generate a task plan template without an image instead.

To modify the Image to task plan template AI agent, [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md) and adjust the settings according to your requirements.

To add tools and information, see [Add tools and information to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-tool-aia.md) for details.

Role required: sn\_task\_plan.admin and sn\_prd\_pm.product\_catalog\_admin

**Important:** In the select channels and status page, make sure that the **Active** button is turned on to activate the AI agent.

To access the agent in AI Agent Studio, see Access the Image to task plan template AI agent. To test the use case, see Test the Image to task plan template AI agent.

