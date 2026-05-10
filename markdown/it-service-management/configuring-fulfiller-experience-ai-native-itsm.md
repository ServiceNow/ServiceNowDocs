---
title: Configuring the fulfiller experience in Simplified IT Service Management
description: Enable an AI-first fulfiller experience for simplified incident and request management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configuring the fulfiller experience in Simplified IT Service Management

Enable an AI-first fulfiller experience for simplified incident and request management.

The following experiences are available after configuring the fulfiller experience:

-   Simplified fulfiller experience with a unified record view and AI-embedded workflows.
-   Improved triage and resolution of incidents by leveraging historical resolution patterns to inform decision-making, thereby enabling service desk agents to focus on resolving complex issues.

For information about available AI agents for fulfiller configurations, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

## Incident Management

It enables you to restore normal service operations while minimizing the impact on business operations and maintaining quality.

<table id="table_h4c_bnq_whc"><thead><tr><th>

Configuration

</th><th>

Description

</th><th>

Default configuration

</th><th>

Optional configurations

</th></tr></thead><tbody><tr><td>

Incident forms

</td><td>

An incident documents a deviation from an expected standard of operation.

</td><td>

Incident form is preconfigured.

</td><td>

Review and update the form layout based on business requirement. For information about creating an incident using Form Builder, see [Working with incident record form](../../incident-management/concept/working-incident-record-form.md) and [Forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/form-configurable-workspace.md).For information about the Implementation Plan Manager Agent that provides conversational AI-native experience for incident form configuration, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Incident lists

</td><td>

Incident list displays incidents grouped by their state.

</td><td>

Incident list and related lists are preconfigured.

</td><td>

Review and update list layouts based on business requirements. For information about updating these fields, see [Working with incident record form](../../incident-management/concept/working-incident-record-form.md).For information about the Implementation Plan Manager Agent that provides conversational AI-native experience for incident list configuration, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Categories

</td><td>

Categories and subcategories help with routing an incident to the right team. It helps reduce the troubleshooting time and bring the service to normalcy.

</td><td>

None

</td><td>

For information about incident categories and subcategories, see[Incident categories and subcategories](../../incident-management/reference/r_CategorizingIncidents.md).For information about the Incident Category Configuration AI Agent that provides conversational AI-native experience for incident category configurations, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Agent inbox

</td><td>

Routing of incoming requests using filters to support service delivery requirements.

</td><td>

Incident routing to fulfiller’s inbox is auto-configured post installation. Configuration includes routing condition, work item size, max wait time, routing group, and so on.

</td><td>

Manage and configure the incident routing experience. For information about configuring this channel, see [Create or configure a service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-service-channel.md).

</td></tr><tr><td>

Routing

</td><td>

Identifying the right user group or user who is skilled to work on an incident by defining conditions and triggers to auto-assign cases and trigger relevant subflows.

</td><td>

None

</td><td>

For information about incident assignment rules, [Define assignment rules for incidents](../../incident-management/task/t_DefinAnAssignRuleIncidents.md).

 For information about business rules, see [Classic Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/business-rules-classic/c_BusinessRules.md).

 For information about the Incident routing configuration agent that provides conversational AI-native experience for incident routing configurations, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Service Level Management

</td><td>

Service level agreements \(SLAs\) define the amount of time for a task to reach a certain condition, to verify that incidents are closed or resolved according to the expectations set for customers.

</td><td>

SLAs and their associated flows are preconfigured for Incident Management. Response and resolution SLAs are defined for incidents with priority P1 through P4.

</td><td>

Review and update the definitions, flows, and notifications that are available with Service Level Management according to the incident process. For information about SLAs, see [Service Level Agreement \(SLA\) definition](../../service-level-management/concept/c_SLADefinitions.md).For information about the SLA Management AI Agent that provides conversational AI-native experience for SLA configuration, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Notifications

</td><td>

Keeping employees and fulfillers informed at every stage of incident resolution.

</td><td>

Notifications align with the default Employee Center notification template.

</td><td>

Configure the notification template. Update notification details such as who receives it, when it is sent, and what \(content\), and so on. For information about creating an incident notification, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md).For information about the Notification Agent that provides conversational AI-native experience for notification configuration, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr></tbody>
</table>## Request Management

<table id="table_ssv_kmq_whc"><thead><tr><th>

Configuration

</th><th>

Description

</th><th>

Default configuration

</th><th>

Optional configurations

</th></tr></thead><tbody><tr><td>

Requested item forms and lists

</td><td>

A requested item helps fulfillers track and resolve an employee's request.

</td><td>

Requested item form, list, and related lists are preconfigured.

</td><td>

Review and update the form layout based on business requirements. For information about requested items, see [Request Management architecture](../../planning-and-policy/concept/request-management-architecture.md).For information about the Implementation Plan Manager Agent that provides conversational AI-native experience for requested item form and list configurations, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Catalog task forms and lists

</td><td>

A catalog task helps fulfillers track and resolve an employee's request.

</td><td>

Catalog task form, list and related lists are preconfigured.

</td><td>

Review the form layout and update based on business need. For information about catalog tasks, see [Request Management architecture](../../planning-and-policy/concept/request-management-architecture.md).For information about the Implementation Plan Manager Agent that provides conversational AI-native experience for catalog task form and list configurations, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Notifications

</td><td>

Keeping employees and fulfillers informed at every stage of request fulfillment.

</td><td>

Notifications align with the default Employee Center notification template.

</td><td>

Configure the notification template. Update notification details such as who receives it, when it is sent, and what \(content\), and so on. For information about creating a request notification, see [View request notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/view-request-notification.md).For information about the Notification Agent that provides conversational AI-native experience for notification configuration, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr></tbody>
</table>## Analytics

|Configuration|Description|Default configuration|Optional configurations|
|-------------|-----------|---------------------|-----------------------|
|Dashboard|Managing dashboards and data visualizations to track progress quickly.|Preconfigured dashboard on workspace landing page that provides visibility into agent workload with key metrics such as Assigned to you, Overdue, and Unassigned.|Edit the existing dashboard or create your own dashboard in Platform Analytics workspace. To create a dashboard using Platform Analytics, see [Platform Analytics KPIs and dashboards](../../itsm-success-dashboard/concept/operational-success-kpi.md).|

## Now Assist for ITSM

<table id="table_shv_kmq_whc"><thead><tr><th>

Configuration

</th><th>

Description

</th><th>

Default configuration

</th><th>

Optional configurations

</th></tr></thead><tbody><tr><td>

Agentic workflows

</td><td>

An agentic workflow is a coordinated, multi‑step process where AI agents plan, act, and collaborate to achieve a complex business goal. For information about agentic workflows in ITSM, see [Use agentic AI in Now Assist for IT Service Management \(ITSM\)](../../now-assist-itsm/concept/now-assist-itsm-ai-agents-use-cases.md).

</td><td>

Prebuilt AI agents for requesters such as for incident creation, status checks, and approvals are enabled in the base system. Additionally, the following prebuilt AI agents are enabled in the base system to improve fulfiller productivity:-   AI-Assisted Incident Triage
-   Resolution and AI Recommendations

</td><td>

Remove an agent that is part of the agentic workflow or manage \(edit, deactivate, activate, or create\) the triggers associated with the agentic workflows. For information about modifying agentic workflows, see [Modify an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aia-use-case.md).

</td></tr><tr><td>

Now Assist skills

</td><td>

Prebuilt, LLM‑powered capabilities that surface in the right UI touchpoints and can be activated or configured by admins across workflow. For example, summarization, KB generation, and email drafting. For information about Now Assist skills in ITSM, see [Using Now Assist for IT Service Management \(ITSM\) Generative AI skills](../../now-assist-itsm/concept/using-now-assist-for-itsm.md).

</td><td>

Now Assist skills such as KB generation, Incident summarization, Chat summarization, Resolution notes generation, and Email generation are enabled in the base system.

</td><td>

Activate or deactivate these skills based on business requirements. For information about modifying Now Assist skills, see [Edit a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/edit-a-now-assist-skill.md).

</td></tr></tbody>
</table>