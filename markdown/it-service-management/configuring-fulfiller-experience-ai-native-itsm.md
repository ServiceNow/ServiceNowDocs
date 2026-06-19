---
title: Configuring the fulfiller experience in Simplified IT Service Management
description: Enable an AI-first fulfiller experience for simplified incident and request management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configuring-fulfiller-experience-ai-native-itsm.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configuring the fulfiller experience in Simplified IT Service Management

Enable an AI-first fulfiller experience for simplified incident and request management.

The following experiences are available after configuring the fulfiller experience:

-   Simplified fulfiller experience with a unified record view and AI-embedded workflows.
-   Improved triage and resolution of incidents by leveraging historical resolution patterns to inform decision-making, thereby enabling service desk agents to focus on resolving complex issues.

For information about available AI agents for fulfiller configurations, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

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

Review and update the form layout based on business requirement. For information about creating an incident using Form Builder, see [Working with incident record form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/working-incident-record-form.md) and .For information about the Implementation Plan Manager Agent that provides conversational AI-native experience for incident form configuration, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Incident lists

</td><td>

Incident list displays incidents grouped by their state.

</td><td>

Incident list and related lists are preconfigured.

</td><td>

Review and update list layouts based on business requirements. For information about updating these fields, see [Working with incident record form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/working-incident-record-form.md).For information about the Implementation Plan Manager Agent that provides conversational AI-native experience for incident list configuration, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Categories

</td><td>

Categories and subcategories help with routing an incident to the right team. It helps reduce the troubleshooting time and bring the service to normalcy.

</td><td>

None

</td><td>

For information about incident categories and subcategories, see[Incident categories and subcategories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/r_CategorizingIncidents.md).For information about the Incident Category Configuration AI Agent that provides conversational AI-native experience for incident category configurations, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Agent inbox

</td><td>

Routing of incoming requests using filters to support service delivery requirements.

</td><td>

Incident routing to fulfiller’s inbox is auto-configured post installation. Configuration includes routing condition, work item size, max wait time, routing group, and so on.

</td><td>

Manage and configure the incident routing experience. For information about configuring this channel, see .

</td></tr><tr><td>

Routing

</td><td>

Identifying the right user group or user who is skilled to work on an incident by defining conditions and triggers to auto-assign cases and trigger relevant subflows.

</td><td>

None

</td><td>

For information about incident assignment rules, [Define assignment rules for incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/t_DefinAnAssignRuleIncidents.md).

 For information about business rules, see .

 For information about the Incident routing configuration agent that provides conversational AI-native experience for incident routing configurations, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Service Level Management

</td><td>

Service level agreements \(SLAs\) define the amount of time for a task to reach a certain condition, to verify that incidents are closed or resolved according to the expectations set for customers.

</td><td>

SLAs and their associated flows are preconfigured for Incident Management. Response and resolution SLAs are defined for incidents with priority P1 through P4.

</td><td>

Review and update the definitions, flows, and notifications that are available with Service Level Management according to the incident process. For information about SLAs, see [Service Level Agreement \(SLA\) definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-level-management/c_SLADefinitions.md).For information about the SLA Management AI Agent that provides conversational AI-native experience for SLA configuration, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Notifications

</td><td>

Keeping employees and fulfillers informed at every stage of incident resolution.

</td><td>

Notifications align with the default Employee Center notification template.

</td><td>

Configure the notification template. Update notification details such as who receives it, when it is sent, and what \(content\), and so on. For information about creating an incident notification, see .For information about the Notification Agent that provides conversational AI-native experience for notification configuration, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

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

Review and update the form layout based on business requirements. For information about requested items, see [Request Management architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/request-management/request-management-architecture.md).For information about the Implementation Plan Manager Agent that provides conversational AI-native experience for requested item form and list configurations, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Catalog task forms and lists

</td><td>

A catalog task helps fulfillers track and resolve an employee's request.

</td><td>

Catalog task form, list and related lists are preconfigured.

</td><td>

Review the form layout and update based on business need. For information about catalog tasks, see [Request Management architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/request-management/request-management-architecture.md).For information about the Implementation Plan Manager Agent that provides conversational AI-native experience for catalog task form and list configurations, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

</td></tr><tr><td>

Notifications

</td><td>

Keeping employees and fulfillers informed at every stage of request fulfillment.

</td><td>

Notifications align with the default Employee Center notification template.

</td><td>

Configure the notification template. Update notification details such as who receives it, when it is sent, and what \(content\), and so on. For information about creating a request notification, see .For information about the Notification Agent that provides conversational AI-native experience for notification configuration, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

</td></tr></tbody>
</table>## Major Incident Management

Accelerates the resolution of a major incident and minimizes the business impact. A major incident is a highest-impact, highest-urgency incident that affects a large number of users, depriving the business of one or more crucial services.

For information about configuring Major Incident Management from SOW Admin Center, see [Manage configurations in Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/manage-admin-console-sow-itsm.md).

## On-Call Scheduling

Ensures that the right person is available to assign an incident to, by rotation through a hierarchy of duty rosters.

For information about configuring On-Call Scheduling from SOW Admin Center, see [Manage configurations in Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/manage-admin-console-sow-itsm.md).

## Problem Management

Manages the life cycle of all problems and prevents problems and resulting incidents from happening. It also aims to eliminate recurring incidents and minimize the impact of incidents that can’t be prevented.

For information about configuring Problem Management from SOW Admin Center, see [Manage configurations in Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/manage-admin-console-sow-itsm.md).

## Walk-up Experience

Enhances the user experience by providing in-person as well as remote assistance to the users for their IT-related issues.

For information about configuring Walk-up Experience from SOW Admin Center, see [Manage configurations in Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/manage-admin-console-sow-itsm.md).

## Analytics

|Configuration|Description|Default configuration|Optional configurations|
|-------------|-----------|---------------------|-----------------------|
|Dashboard|Managing dashboards and data visualizations to track progress quickly.|Preconfigured dashboard on workspace landing page that provides visibility into agent workload with key metrics such as Assigned to you, Overdue, and Unassigned.|Edit the existing dashboard or create your own dashboard in Platform Analytics workspace. To create a dashboard using Platform Analytics, see [Platform Analytics KPIs and dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/operational-success-kpi.md).|

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

An agentic workflow is a coordinated, multi‑step process where AI agents plan, act, and collaborate to achieve a complex business goal. For information about agentic workflows in ITSM, see [Use agentic AI in Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-ai-agents-use-cases.md).

</td><td>

Prebuilt AI agents for requesters such as for incident creation, status checks, and approvals are enabled in the base system. Additionally, the following prebuilt AI agents are enabled in the base system to improve fulfiller productivity:-   AI-Assisted Incident Triage
-   Resolution and AI Recommendations

</td><td>

Remove an agent that is part of the agentic workflow or manage \(edit, deactivate, activate, or create\) the triggers associated with the agentic workflows. For information about modifying agentic workflows, see .

</td></tr><tr><td>

Now Assist skills

</td><td>

Prebuilt, LLM‑powered capabilities that surface in the right UI touchpoints and can be activated or configured by admins across workflow. For example, summarization, KB generation, and email drafting. For information about Now Assist skills in ITSM, see [Using Now Assist for IT Service Management \(ITSM\) Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/using-now-assist-for-itsm.md).

</td><td>

Now Assist skills such as KB generation, Incident summarization, Chat summarization, Resolution notes generation, and Email generation are enabled in the base system.

</td><td>

Activate or deactivate these skills based on business requirements. For information about modifying Now Assist skills, see .

</td></tr></tbody>
</table>## Change Management

<table id="table_xcv_3ms_w3c"><thead><tr><th>

Configuration

</th><th>

Description

</th><th>

Default configuration

</th><th>

Optional configurations

</th></tr></thead><tbody><tr><td>

Team roles

</td><td>

Team roles control who can approve, build, or review a change. They define each person's job so admins can control access and keep work organized.

</td><td>

None

</td><td>

Add the change managers and implementation group members.

</td></tr><tr><td>

Risk configuration

</td><td>

Survey, score, and assign a risk level and the appropriate response.

</td><td>

Risk assessment questions, responses, and threshold score boundaries for Moderate and High risk levels.

</td><td>

Review and update the pre-configured risk assessment questions, responses, and threshold score boundaries or create new ones.

</td></tr><tr><td>

Change Advisory Board \(CAB\)

</td><td>

Configure your Change Advisory Board \(CAB\) — the group that reviews and advises on significant changes before they're approved.

</td><td>

Recurring schedules for CAB meetings, and conditions that determine which change requests are routed to the CAB.

</td><td>

Assign CAB members.

 Review and update the recurring schedules for CAB meetings, and conditions that determine which change requests are routed to the CAB, or create new ones.

</td></tr><tr><td>

Change models

</td><td>

Change models automate the mechanics of change management so your team can focus on implementation. When a change is created, the model automatically determines who needs to approve it, what documentation is required, which tasks to create, and what notifications to send. This eliminates manual routing decisions and ensures nothing gets missed.

</td><td>

Core change models \(Normal, Standard, Emergency\) and Change Registration model.

</td><td>

For more information, see [Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md).

</td></tr><tr><td>

Change schedules

</td><td>

Change schedules are time-based rules that define when changes are allowed, restricted, or blacked out in your environment. They give change managers and CABs structured control over the timing of changes to minimize risk and service disruption.

</td><td>

Blackout and maintenance schedules.

</td><td>

Review and update the pre-configured schedules, or create new ones.

</td></tr><tr><td>

Notifications

</td><td>

Notifications keep users informed about approvals, status updates, and task assignments at key steps in the change process.

</td><td>

Notifications based on change definitions, showing each notification's name, active status, category, email template, and trigger conditions.

</td><td>

Review and update the pre-configured notifications, or create new ones.

</td></tr></tbody>
</table>For more information on Change Management, see [Configuring Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-change-management-experience-in-it-service-management.md).

-   **[Configuring Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-change-management-experience-in-it-service-management.md)**  
Configure Change Management through a guided experience that walks you through the core setup areas required to make Change Management operational.

**Parent Topic:**[Configure integrations and ITSM experiences in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-ai-native-itsm.md)

