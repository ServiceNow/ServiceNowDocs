---
title: Configure a push connector
description: You can configure listeners and connectors to push event information to the instance or MID Server.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure a push connector

You can configure listeners and connectors to push event information to the instance or MID Server.

Event Management receives external events through a push connector or script. If you are using a script to collect events, no configuration is required. All other methods of collecting events require configuration.

After event collection configuration, Event Management can collect events that are sent directly to the instance, or via the MID Server, SNMP trap, or email.

**Note:** Integrating with push connectors is only available by installing the Event Management Connector plugin from the ServiceNow Store.

## Standard event form

All events must use a standard event form, regardless of how they arrive at the instance. For more information, see [Event field format for event collection](c_EMIntegrateRequirementEvent.md).

## Event collection

Event Management facilitates communication and movement of data between external applications, data sources, services, and the ServiceNow AI Platform instance.

<table id="simpletable_av2_cxd_gz"><thead><tr><th>

Event collection modes

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provided by the base system

</td><td>

Listeners and connectors provided with the Event Management application:-   AWS CloudWatch, see [Integrate AWS platform as a data source](../task/aws-events-transform-script.md).
-   Azure event messages, see [Integrate Azure Monitor as an authenticated data source](azure-integration.md).
-   BMC TrueSight events, see [Event collection from BMC TrueSight and BMC TrueSight\_v2](../task/event-collection-BMCTrueSight.md).
-   Datadog events, see [Integrate Datadog platform events](datadog-events-integration.md).
-   Dynatrace events, see [Integrate Dynatrace platform events](dynatrace-events-integration.md).
-   Google Cloud Platform \(GCP\) events, see [Integrate Google Cloud Platform \(GCP\) events](../task/gcp-events-integration.md)
-   New Relic events, see [Integrate New Relic platform events](../task/new-relic-events-integration.md).
-   Generic event collection through the MID Server.
-   Generic event collection through the instance.

Where event messages are received in XML, you can base your script on the example XML transform script provided with the base system.

</td></tr><tr><td>

Via MID WebService

</td><td>

You can configure the MID WebService Event Collector to push event messages to the MID Server. For more information, see [Pushing events to the MID Server using web service API](event-collection-via-MID-using-push.md).

</td></tr><tr><td>

Create your own content

</td><td>

You can configure your own listener:-   Via MID WebServer API. See [Pushing events to the instance using web service API](../task/send-events-via-web-service.md).
-   Via Custom Transformation. See [Event collection from custom payloads](../task/event-collection-custom-payloads.md).

</td></tr><tr><td>

Via SNMP

</td><td>

SNMP listeners provided with the Event Management application:Generic SNMPv2. See [Configure event collection for SNMP traps](../task/t_EMSNMPTrapEvent.md).

In addition, you can create your own custom listener. See [Integrate with push connectors](../task/configure-listener-transform-script.md).

</td></tr><tr><td>

Via Email

</td><td>

Email listener. See [Configure event collection from email](../task/t_EMConfigureEmailConnector.md).

</td></tr></tbody>
</table>**Related topics**  


[Push connector instance form](../reference/push-connector-instance-form.md)

