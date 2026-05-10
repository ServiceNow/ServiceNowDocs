---
title: AI agents and agentic workflows in Simplified IT Service Management
description: Use conversational AI-native experience for administrators, employees, and fulfillers using Simplified IT Service Management \(Simplified ITSM\). AI agents and agentic workflows provide a step-by-step approach to configure ITSM workflows with validated inputs and preview.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-31"
reading_time_minutes: 4
breadcrumb: [Reference, Simplified IT Service Management, IT Service Management]
---

# AI agents and agentic workflows in Simplified IT Service Management

Use conversational AI-native experience for administrators, employees, and fulfillers using Simplified IT Service Management \(Simplified ITSM\). AI agents and agentic workflows provide a step-by-step approach to configure ITSM workflows with validated inputs and preview.

## AI agents for ITSM workflow configurations

These AI agents help administrators configure ITSM workflows seamlessly from a single admin UI page using natural language.

For information about admin configurations applicable for Simplified ITSM, see [Platform module configuration in Now Assist for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-config-platform-il.md).

For information about employee configurations in Simplified ITSM, see [Configuring the employee experience in Simplified IT Service Management](../concept/configuring-employee-experience-ai-native-itsm.md).

For information about fulfiller configurations in Simplified ITSM, see [Configuring the fulfiller experience in Simplified IT Service Management](../concept/configuring-fulfiller-experience-ai-native-itsm.md).

<table id="table_ckp_xzv_t3c"><thead><tr><th>

AI Agent

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Admin configurations

</td></tr><tr><td>

AI Search Configuration Agent

</td><td>

Configures AI Search for ServiceNow internal tables by defining internal search sources, search profiles, and table mappings through conversation.

</td></tr><tr><td>

AI Search XCC Agent

</td><td>

Configures external content connectors for AI Search for public websites \(for example, Zoom, Apple Support, and Okta\) and SharePoint repositories.The agent guides with connector discovery that aligns with user requirements, authentication, content scope, crawl scheduling, search profile mapping, and error recovery.

</td></tr><tr><td>

Group and roles assignment agent

</td><td>

Provides user access through group-based associations. Creates a user group, manages users in a group, assigns roles to a group, and adds users to a role.

</td></tr><tr><td>

IA Operational Data Workflow Agent

</td><td>

Enables a streamlined data import process for operational data, that is, user groups, locations, users, and departments by creating data sources, import sets, and transform maps.

</td></tr><tr><td>

SSO Configuration Agent

</td><td>

Configures Single Sign-On \(SSO\) authentication for SSO providers such as Microsoft Azure and Okta using SAML and OpenID Connect \(OIDC\) protocols for ServiceNow instances.It collects and validates identity provider details, creates authentication configurations, and guides a user through review, testing, and activation to ensure an accurate SSO setup experience.

</td></tr><tr><td class="sub-head" colspan="2">

Employee configurations

</td></tr><tr><td>

Implementation Plan Manager Agent

</td><td>

Configures surveys to create, send, and collect responses that improve the user experience.

</td></tr><tr><td class="sub-head" colspan="2">

Fulfiller configurations

</td></tr><tr><td>

Implementation Plan Manager Agent

</td><td>

Configures the following fulfiller forms and views:-   Incident list
-   Catalog task list
-   Requested item list
-   Incident form layout
-   Catalog task form layout
-   Requested item form layout

</td></tr><tr><td>

Incident routing configuration agent

</td><td>

Manages assignment rules that determine how an incident is routed to appropriate teams.The following capabilities are available:

-   Helps create, modify, and deactivate assignment rules for incident routing
-   Helps activate business rules and assignment rules in the base system
-   Generates AI-powered recommendations for rules

</td></tr><tr><td>

Incident Category Configuration AI Agent

</td><td>

Configures incident categories and subcategories.It recommends industry-specific categories, supports bulk import via an Excel or CSV file, and provides a preview of changes before committing. It also supports editing categories in the base system.

</td></tr><tr><td>

Notification Agent

</td><td>

Creates and edits email notification records.

</td></tr><tr><td>

SLA Management AI Agent

</td><td>

Configures Service Level Agreement \(SLA\) definitions of the SLA type for an incident.

</td></tr></tbody>
</table>## AI agents for employee usage

These AI agents help employees with their ITSM needs using natural language.

<table id="table_zfh_nnt_53c"><thead><tr><th>

AI agent

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Incident AI Agent

</td><td>

Manages the life cycle of an IT support issue, from the initial diagnosis to the final resolution or an incident creation. It helps an employee resolve the issue with self-service solutions, reach out to a live agent, or create an incident or requested item if further assistance is required.

</td></tr><tr><td>

Approval Assistance Agent

</td><td>

Manages approval requests relevant to the logged-in user. It has the following capabilities:-   Retrieves and filters pending approvals relevant to the user
-   Provides information about each approval
-   Generates a checklist of conditions required to approve or reject a request. This information is based on relevant knowledge base articles and the requester's user’s details and assets.
-   Supports approving or rejecting approval records

</td></tr><tr><td>

Request Status Agent

</td><td>

Manages the logged-in user's ServiceNow tickets \(incident, task, or request\) created by the logged-in user. It has the following capabilities:-   Retrieves a filtered list of open or closed tickets
-   Provides the latest status and activity
-   Answers questions based on the ticket's comment history
-   Supports adding comments, uploading attachments, and running follow-up actions on tickets

**Note:** It does not create a request, but works on existing requests only.

</td></tr></tbody>
</table>## Agentic workflows for fulfiller usage

These AI agents help fulfillers with their ITSM tasks using natural language.

|Agentic workflow|Description|
|----------------|-----------|
|Investigate and resolve ITSM incidents|Provides recommendations to resolve an incident based on the incident number. Checks for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident. For information about this agentic workflow, see [IT Service Management AI agent collection Investigate and resolve ITSM incidents agentic workflow](../../now-assist-itsm/concept/now-assist-itsm-aiagents-incident-resolver-workflow.md).|
|Triage and categorize ITSM incidents|Assigns incident categories and subcategories based on its short description. After categorizing the incident, assigns the service, service offering, and configuration item \(CI\) related to the incident. It also automatically links incidents to major incidents or known problems. For information about this agentic workflow, see [IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow](../../now-assist-itsm/concept/now-assist-itsm-aiagents-catincidents-usecase.md).|

**Parent Topic:**[Simplified IT Service Management reference](../concept/ai-native-it-service-desk-reference.md)

**Related topics**  


[Explore Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-ai-agents.md)

