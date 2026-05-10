---
title: Using agentic flows in Universal Request AI agent collection
description: Use the Universal Request AI agent collection to complete tasks autonomously.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Universal Request, Employee Service Management]
---

# Using agentic flows in Universal Request AI agent collection

Use the Universal Request AI agent collection to complete tasks autonomously.

<table id="table_gyx_brq_l2c11"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Universal Request Router agentic workflow

</td><td>

Enables employees to request a department agnostic ticket to avail services that are not readily accessible/understandable via the catalog listings or the services that require collaboration across multiple departments.

</td><td>

-   Universal Request departmental ticket creator
-   Record field value prediction AI agent

</td></tr></tbody>
</table>|AI agents|Description|
|---------|-----------|
|Universal Request departmental ticket creator|Automates the routing of universal requests to appropriate departmental ticketing systems by analyzing department predictions and creating properly configured HR cases or IT incidents with all necessary field mappings and reference tracking.|
|Record field value prediction AI agent|Predict fields of an incoming task/record by gathering incoming task sys\_id. It can also provide a summary and justification of the field predictions.|

**Important:** All agentic workflow and AI agent records are read-only by default.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and then do the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn't necessary.

For more information about duplicating an agentic workflow, implementing access control lists, and activating the required components, see the following topics:

-   [Duplicate an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md)
-   [Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-aia-use-case.md)
-   [Modify an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-ai-agent.md)

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

-   **[Universal Request Router agentic workflow](agentic-flow-ur.md)**  
Enables employees to request a department agnostic ticket to avail services that are not readily accessible/understandable via the catalog listings or the services that require collaboration across multiple departments.

**Parent Topic:**[Universal Request](ur-landing-limitedaccess.md)

