---
title: Microsoft Teams Spoke
description: The Microsoft Teams spoke provides actions which post messages and ServiceNow incident, problem, and change record details to Microsoft Teams channels.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Teams Spoke

The Microsoft Teams spoke provides actions which post messages and ServiceNow incident, problem, and change record details to Microsoft Teams channels.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

**Important:** Starting with the Yokohama release, Microsoft Teams Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Microsoft Teams Graph Spoke provides the latest experience for this functionality.

For more information, search for the term `Microsoft Teams Spoke for ServiceNow IntegrationHub` in [Plugins planned for deprecation](https://www.servicenow.com/docs/access?context=plugin-changes&version=zurich&pubname=zurich-release-notes&section=plugins-planned-for-deprecation&ft:locale=en-US).

## Spoke version

Microsoft Teams spoke v1.1.3 is the latest version.

## Microsoft Teams actions

The Microsoft Teams spoke is an available integration through Integration Hub. You can specify the following Microsoft Teams actions within a flow:

|Action|Description|
|------|-----------|
|Post a Message|Send a message to a Microsoft Teams channel using a Webhook Connector. Specify the Webhook URL, Title, and Message to send.|
|Post Change Details|Send details about a ServiceNow change record to a Microsoft Teams channel using a Webhook Connector. Specify the Webhook URL and Change record to send.|
|Post Incident Details|Send details about a ServiceNow incident record to a Microsoft Teams channel using a Webhook Connector. Specify the Webhook URL and Incident record to send.|
|Post Problem Details|Send details about a ServiceNow problem record to a Microsoft Teams channel using a Webhook Connector. Specify the Webhook URL and Problem record to send.|

## Microsoft Teams Inputs

The following inputs are common to the Microsoft Teams actions:

|Input|Description|
|-----|-----------|
|\[Required\] Webhook URL|The Microsoft Teams webhook for sending a message. Set up the webhook before configuring this action. Refer to the custom incoming webhook for Microsoft Teams documentation.|
|\[Optional\] Title|Title of the message.|
|\[Optional\] Additional Message|Add a message before the record details.|
|\[Optional\] Override Default Fields|You can provide a comma-separated list of field names to send instead of the default fields. Default fields are Short Description, Category, State, Priority, and Assignment Group.|
|\[Optional\] Theme Color \(Hex\)|Hex code value of color to highlight the message.|
|\[Optional\] Action URL|URL to the page that opens when you click the button. For more information, see [https://learn.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/connectors-using?tabs=cURL](https://learn.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/connectors-using?tabs=cURL).|
|\[Optional\] Action Name|Name of the action that you can automate with the flow.|

## Example

You can add a Microsoft Teams Post Incident Details action to a flow which identifies newly created high priority incidents and a specified theme color.

![Post Incident Details action added to a flow](../images/example-msteams-action.png)

