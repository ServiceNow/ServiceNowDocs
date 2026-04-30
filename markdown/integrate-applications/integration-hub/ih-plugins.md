---
title: Integration Hub plugins
description: Request Integration Hub plugins included in your subscription.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2025-07-15"
reading_time_minutes: 3
breadcrumb: [Request Integration Hub, Configuring Integration Hub, Integration Hub, Creating integrations with applications]
---

# Integration Hub plugins

Request Integration Hub plugins included in your subscription.

## Integration Hub Installer plugins

The following Integration Hub Installer plugins are the main plugins for the Starter, Professional, and Enterprise Integration Hub subscriptions. For a list of what's included in each subscription level, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

-   ServiceNow IntegrationHub Starter Pack Installer \[com.glide.hub.integrations\]
-   ServiceNow IntegrationHub Standard Pack Installer \[com.glide.hub.integrations.standard\]
-   ServiceNow IntegrationHub Professional Pack Installer \[com.glide.hub.integrations.professional\]
-   ServiceNow IntegrationHub Enterprise Pack Installer \[com.glide.hub.integrations.enterprise\]

<table id="table_ny4_kkr_hbb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ServiceNow IntegrationHub Content - Deprecated \[com.glide.hub.integration.content\]

</td><td>

Workflow Studio actions to integrate with Slack, HipChat, Microsoft AD, Microsoft Azure, Microsoft Teams, and ServiceNow eBonding

</td></tr><tr><td>

Flow Designer Action Step - Payload Builder \[com.glide.hub.action\_step.payload\]

</td><td>

Enable action designers to easily create name-value pairs in JSON and XML payloads using dynamic data.

</td></tr><tr><td>

ServiceNow IntegrationHub Action Step - JDBC \[com.glide.hub.action\_step.jdbc\]

</td><td>

Create a reusable action to send SQL commands to a relational database.

</td></tr><tr><td>

ServiceNow IntegrationHub Action Step - REST\[com.glide.hub.action\_step.rest\]

</td><td>

Enables the REST action step in Workflow Studio.

</td></tr><tr><td>

ServiceNow IntegrationHub Action Step - PowerShell\[com.glide.hub.action\_step.powershell\]

</td><td>

Enables the PowerShell action step in Workflow Studio.

</td></tr><tr><td>

ServiceNow IntegrationHub Action Step - SOAP \[com.glide.hub.action\_step.soap\]

</td><td>

Enables the SOAP action step in Workflow Studio.

</td></tr><tr><td>

ServiceNow IntegrationHub Action Step - SSH \[com.glide.hub.action\_step.ssh\]

</td><td>

The SSH step executes SSH commands on an external \*nix system through a ServiceNow® MID Server. The step also stores scripts and commands for the \*nix systems.

</td></tr><tr><td>

ServiceNow IntegrationHub Action Step - XML Parser \[com.glide.hub.action\_step.xmlparser\]

</td><td>

Enables the XML parser action step in Workflow Studio.

</td></tr><tr><td>

ServiceNow IntegrationHub Action Template - Data Stream \[com.glide.hub.action\_type.datastream\]

</td><td>

Send REST, SOAP, or JDBC requests from Workflow Studio to APIs that return a stream of response data larger than 10 MB, or that return paginated results. Parse stream data into a series of complex object outputs and use the data pills in other actions in a flow.

</td></tr><tr><td>

HipChat Spoke for ServiceNow IntegrationHub \[com.sn.hipchat.ah\]

</td><td>

The HipChat Spoke for ServiceNow IntegrationHub provides actions that a process analyst can use when designing flows. The actions allow them to automate the creation of conversations, add users to a conversation, and send messages to a conversation.**Note:** This integration is deprecated.

</td></tr><tr><td>

Slack Spoke for ServiceNow IntegrationHub \[com.sn.slack.ahv2\]

</td><td>

The Slack Spoke for ServiceNow IntegrationHub provides actions that a process analyst can use when designing flows. Send messages about incidents and problems to a channel.

</td></tr><tr><td>

Slack Webhooks Spoke for ServiceNow IntegrationHub\[com.sn.slack.ah\]

</td><td>

Use Slack webhooks to post messages and record details for ServiceNow incidents, problems, and changes to Slack channels.

</td></tr><tr><td>

Microsoft SCCM Spoke for IntegrationHub \[com.sn.sccm.spoke\]

</td><td>

Provides actions that a process analyst can use to automate the management of user collections, device collections, and application deployments.

</td></tr><tr><td>

Microsoft Teams Spoke for ServiceNow IntegrationHub\[com.sn.ms\_teams.ah\]

</td><td>

Provides actions that a process analyst can use when designing flows to automate sending messages about ServiceNow incident and problem records to a Microsoft Teams channel.

</td></tr><tr><td>

Microsoft Azure AD Spoke for IntegrationHub\[com.sn.azure\_ad.spoke\]

</td><td>

Manage users, security groups, and office groups. Apply licenses and provision users in Office 365.

</td></tr><tr><td>

ServiceNow eBonding Spoke for ServiceNow IntegrationHub\[com.glide.sn.ebonding.ah\]

</td><td>

The ServiceNow ebonding Spoke for the ServiceNow IntegrationHub provides Actions that enable process analysts to compose flows that help in ebonding with remote ServiceNow instances.

</td></tr><tr><td>

Integration Hub Designer Core\[com.glide.ihub.designer.core\]

</td><td>

Enables automation of data imports through the Integration Hub - Import environment. Installs with the ServiceNow Integration Hub Action Template - Data Stream \[com.glide.hub.action\_type.datastream\] plugin.

</td></tr><tr><td>

ServiceNow Stream Connect Installer\[com.glide.hub.stream\_connect.installer\]

</td><td>

Enables the licensed components for working with message-based streaming data in [Stream Connect for Apache Kafka](../concept/stream-connect-apache-kafka.md).

 Activating this plugin activates the following plugins.

-   ServiceNow IntegrationHub Flow Trigger - Kafka \[com.glide.hub.flow\_trigger.kafka\]: Enables the ability to consume a Kafka message for a topic within a flow.
-   ServiceNow IntegrationHub Action Step - Kafka Producer \[com.glide.hub.action\_step.kafka\]: Enables the ability to produce a Kafka message for a topic within a flow.
-   ServiceNow Integration Hub Kafka Consumer \[com.glide.hub.kafka\_consumer\]: Provides IntegrationHub components for working with Kafka.
-   ServiceNow IntegrationHub ETL Consumer - Kafka \[com.glide.hub.etl\_consumer.kafka\]: Enables the ability to consume Kafka messages from a topic using RTE, a transform map, or a script.
-   ServiceNow Stream Connect Replication - Kafka \[com.glide.hub.stream\_connect.replication.kafka\]: Enables support for replicating Stream Connect topics via a MID Server with a customer Kafka cluster.
-   ServiceNow Integration Hub Stream Connect Schema \[com.glide.hub.stream\_connect.schema\]: Enables importing and creating schemas to send and receive messages in an Apache Avro format.

</td></tr></tbody>
</table>**Parent Topic:**[Request Integration Hub](../../flow-designer/concept/request-ih-overview.md)

