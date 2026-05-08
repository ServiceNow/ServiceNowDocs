---
title: Configuring the employee experience in Simplified IT Service Management
description: Enable an AI-first comprehensive employee experience focused on a simplified portal with an AI-first chat approach to find answers, order items, check status, and create incidents.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configuring the employee experience in Simplified IT Service Management

Enable an AI-first comprehensive employee experience focused on a simplified portal with an AI-first chat approach to find answers, order items, check status, and create incidents.

The following experiences are available after configuring the employee experience:

-   Simplified Employee Center portal supporting AI chat, catalog, and knowledge content.
-   Now Assist Virtual Agent enhanced with prebuilt AI agents for requesters, enabling incident creation, status checks, and approvals in their preferred channels such as Microsoft Teams.
-   Prebuilt content such as taxonomy, catalog items, and record producers to resolve common IT issues and requests.

For information about available AI agents for employee configurations, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

## Service channels

Service channels provide customer support by automatically routing incoming work to agents. You can specify additional conditions to filter the work items that are handled in the channel, change the agent capacity \(workload\) for the channel, set the inbox layouts that your agents use in Workspace, and view associated work item queues.

<table id="table_jzz_k5p_whc"><thead><tr><th>

Configuration

</th><th>

Description

</th><th>

Default configuration

</th><th>

Optional configurations

</th></tr></thead><tbody><tr><td>

Chat

</td><td>

Routing and assigning chat interactions

</td><td>

Live Agent chat is auto-configured post installation. It includes routing condition, work item size, maximum wait time, routing group, and so on.

</td><td>

Manage and configure the live agent chat experience. For information about configuring this channel, see Create or configure a service channel.

</td></tr><tr><td>

Email

</td><td>

Routing requests from emails. Email action helps in registering requests or issues when an employee sends an email to registered email accounts. Email accounts can be configured from the Platform module in Product Configuration Console.

</td><td>

Email actions are preconfigured with Simplified ITSM.

</td><td>

Review the email actions available in the base system and update them based on the business process and requirement. For information about inbound email actions, see Inbound email actions.

</td></tr><tr><td>

Phone

</td><td>

Routing requests from phone interactions by integrating your ServiceNow instance with a third-party phone provider such as Amazon Connect and Genesys.

</td><td>

None

</td><td>

For information about integrating ServiceNow Voice with Amazon Connect, see Integrate ServiceNow Voice with Amazon Connect.For information about integrating ServiceNow voice assistant with Genesys, see Integrate ServiceNow voice assistant with Genesys Cloud service.

</td></tr></tbody>
</table>## Virtual Agent

The Virtual Agent platform provides user assistance through conversations within an intelligent messaging interface. You can design and build automated conversations that help your users quickly obtain information, decide, and perform common work tasks with Virtual Agent.

|Configuration|Description|Default configuration|Optional configurations|
|-------------|-----------|---------------------|-----------------------|
|VA configuration|Virtual Agent features, components, and integrations that are essential to provide support to your employees, IT teams, and customers.|ServiceNow Virtual Agent is preconfigured with default general settings and branding, live agent chat configuration, and Now Assist Virtual Agent configurations.|Review and configure settings to align the run-time experience of Virtual Agent with your requirements. For information about these configurations, see Configuring Virtual Agent.|
|VA for MS Teams|Integrating Virtual Agent with Microsoft Teams to enable users create their requests from within Microsoft Teams.|None|For information about Microsoft Teams integration, see Configure Virtual Agent for Microsoft Teams.|
|VA for Slack|Integrating Virtual Agent with Slack to enable users create their requests from within Slack.|None|For information about Slack integration, see Integrating ServiceNow Virtual Agent with Slack.|

## Taxonomy

|Configuration|Description|Default configuration|Optional configurations|
|-------------|-----------|---------------------|-----------------------|
|Taxonomy|Taxonomy for employee content maps the content of your product or services to the taxonomy hierarchy.|Predefined set of taxonomies for easy discovery of catalog items and knowledge on Employee Center.|Review, edit, remove, or add taxonomies that align with the business hierarchy of your organization. For information about taxonomy, see Create taxonomy.|

## Catalog items

|Configuration|Description|Default configuration|Optional configurations|
|-------------|-----------|---------------------|-----------------------|
|Catalog items|Services or product offerings available for your users.|Prebuilt catalog items and record producer with fulfillment workflows covering common IT issues and requests are active. For information about prebuilt catalog items, see [Catalog items installed with Simplified IT Service Management](../reference/catalog-items-base-system.md).|Review and edit a catalog item or create a catalog item using the native catalog builder experience. For information about adding a catalog item using Catalog Builder, see Create a catalog item using a template.|

## Surveys

<table id="table_ssv_kmq_whc"><thead><tr><th>

Configuration

</th><th>

Description

</th><th>

Default configuration

</th><th>

Optional configurations

</th></tr></thead><tbody><tr><td>

Surveys

</td><td>

Surveys help you create, send, and collect responses from your users to improve their experience.

</td><td>

Preconfigured employee satisfaction surveys to gather feedback post incident resolution and request fulfillment.

</td><td>

Create or edit an existing survey using Survey Designer. For information about configuring surveys, see Survey designer.For information about the Implementation Plan Manager Agent that provides conversational AI-native experience for survey configuration, see [AI agents and agentic workflows in Simplified IT Service Management](../reference/agents-ai-native-it-service-desk.md).

</td></tr></tbody>
</table>