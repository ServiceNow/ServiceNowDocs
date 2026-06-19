---
title: Configuring the employee experience in Simplified IT Service Management
description: Enable an AI-first comprehensive employee experience focused on a simplified portal with an AI-first chat approach to find answers, order items, check status, and create incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configuring-employee-experience-ai-native-itsm.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configuring the employee experience in Simplified IT Service Management

Enable an AI-first comprehensive employee experience focused on a simplified portal with an AI-first chat approach to find answers, order items, check status, and create incidents.

The following experiences are available after configuring the employee experience:

-   Simplified Employee Center portal supporting AI chat, catalog, and knowledge content.
-   Now Assist Virtual Agent enhanced with prebuilt AI agents for requesters, enabling incident creation, status checks, and approvals in their preferred channels such as Microsoft Teams.
-   Prebuilt content such as taxonomy, catalog items, and record producers to resolve common IT issues and requests.

For information about available AI agents for employee configurations, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

## Employee Slate

Employee Slate provides an AI-first employee experience that brings search, requests, tasks, knowledge, and communications together in one intuitive destination. Employees can easily find information, manage requests and tasks, stay informed through communications and news, connect with teams, and get work done faster.

**Note:** For upgrading instances, if the Employee Slate is installed, the **Taxonomy** section is hidden from the employee experience configuration.

|Configuration|Description|Default configuration|Optional configurations|
|-------------|-----------|---------------------|-----------------------|
|Employee Slate Moveworks|Employee Slate and Moveworks integration combines the Moveworks AI assistant with key Employee Slate features such as conversation-first home page, the interactive split view, Enterprise Search, and Inbox. Enables employees to handle work tasks, find information, and get things done faster with the Moveworks AI assistant.|None|Configure the branding, the Moveworks AI Assistant connection, the canvas configuration, and the update set package that promotes configurations between environments. For information about Employee Slate for Moveworks, see .|
|Employee Slate Now Assist|Employee Slate and Now Assist integration provides intelligent assistance throughout the Employee Slate experience. The AI assistant offers proactive suggestions, automates routine tasks, and provides contextual help based on your chat conversations and activities. Enable employees to get AI-powered assistance for everyday work tasks through intelligent suggestions, automated workflows, and contextual support.|None|Configure the branding and data sources, internal and external search sources, conversational assistant configurations, canvas, and other features. For information about Employee Slate for Now Assist, see .|

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

Manage and configure the live agent chat experience. For information about configuring this channel, see .

</td></tr><tr><td>

Email

</td><td>

Routing requests from emails. Email action helps in registering requests or issues when an employee sends an email to registered email accounts. Email accounts can be configured from the Platform module in Product Configuration Console.

</td><td>

Email actions are preconfigured with Simplified ITSM.

</td><td>

Review the email actions available in the base system and update them based on the business process and requirement. For information about inbound email actions, see .

</td></tr><tr><td>

Phone

</td><td>

Routing requests from phone interactions by integrating your ServiceNow instance with a third-party phone provider such as Amazon Connect and Genesys.

</td><td>

None

</td><td>

For information about integrating ServiceNow Voice with Amazon Connect, see .For information about integrating ServiceNow voice assistant with Genesys, see .

</td></tr></tbody>
</table>## Virtual Agent

The Virtual Agent platform provides user assistance through conversations within an intelligent messaging interface. You can design and build automated conversations that help your users quickly obtain information, decide, and perform common work tasks with Virtual Agent.

|Configuration|Description|Default configuration|Optional configurations|
|-------------|-----------|---------------------|-----------------------|
|VA configuration|Virtual Agent features, components, and integrations that are essential to provide support to your employees, IT teams, and customers.|ServiceNow Virtual Agent is preconfigured with default general settings and branding, live agent chat configuration, and Now Assist Virtual Agent configurations.|Review and configure settings to align the run-time experience of Virtual Agent with your requirements. For information about these configurations, see .|
|VA for MS Teams|Integrating Virtual Agent with Microsoft Teams to enable users create their requests from within Microsoft Teams.|None|For information about Microsoft Teams integration, see .|
|VA for Slack|Integrating Virtual Agent with Slack to enable users create their requests from within Slack.|None|For information about Slack integration, see .|

## Taxonomy

|Configuration|Description|Default configuration|Optional configurations|
|-------------|-----------|---------------------|-----------------------|
|Taxonomy|Taxonomy for employee content maps the content of your product or services to the taxonomy hierarchy.|Predefined set of taxonomies for easy discovery of catalog items and knowledge on Employee Center.|Review, edit, remove, or add taxonomies that align with the business hierarchy of your organization. For information about taxonomy, see .|

## Catalog items

|Configuration|Description|Default configuration|Optional configurations|
|-------------|-----------|---------------------|-----------------------|
|Catalog items|Services or product offerings available for your users.|Prebuilt catalog items and record producer with fulfillment workflows covering common IT issues and requests are active. For information about prebuilt catalog items, see [Catalog items installed with Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/catalog-items-base-system.md).|Review and edit a catalog item or create a catalog item using the native catalog builder experience. For information about adding a catalog item using Catalog Builder, see .|

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

Create or edit an existing survey using Survey Designer. For information about configuring surveys, see .For information about the Implementation Plan Manager Agent that provides conversational AI-native experience for survey configuration, see [AI agents and agentic workflows in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/agents-ai-native-it-service-desk.md).

</td></tr></tbody>
</table>**Parent Topic:**[Configure integrations and ITSM experiences in Simplified IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-ai-native-itsm.md)

