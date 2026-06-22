---
title: Configure Event Management connectors
description: Event Management provides many connectors to pull or push events from external devices. Connectors are available from the ServiceNow store as well as from third parties. You can also create custom connectors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/connectors-and-listeners.html
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure Event Management connectors

Event Management provides many connectors to pull or push events from external devices. Connectors are available from the ServiceNow store as well as from third parties. You can also create custom connectors.

## Provided connectors \(pull\)

This table lists the connectors that are provided with Event Management.

**Note:**

-   The Azure Metrics and AWS CloudWatch Metrics connectors display in the base system only when the Operational Intelligence plugin \(com.snc.sa.metric\) is activated.
-   All connectors support external credential storage solutions. For details on configuring external credential storage, see [External credential storage configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/connections-and-credentials/external_cred_storage_configuration.md).

<table id="table_lzz_dcm_s1c"><thead><tr><th>

Connectors

</th><th>

Supported version

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Azure Monitor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-azure-bi-directional-connector.md)

</td><td>

 

</td><td>

Send alert state changes to the Azure Portal.

</td></tr><tr><td>

[HPOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigureHPOMConnector.md)

</td><td>

08.60.005

</td><td>

Receive events from the HP Operations Manager \(HPOM\).

</td></tr><tr><td>

[Hyperic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigureHypericConnectorJS.md)

</td><td>

5.8.4.0

</td><td>

Receive events from the VMware vRealize Hyperic server.

</td></tr><tr><td>

[Logicmonitor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-logic-monitor-connector.md)

</td><td>

156

</td><td>

Receive events from the Logicmonitor server.

</td></tr><tr><td>

[IBM Netcool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMUpgradeNetcoolConnector.md)

</td><td>

8.1.0

</td><td>

Receive events from IBM Netcool/OMNIbus Object Servers and Impact Servers.

</td></tr><tr><td>

[Icinga2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-icinga-connector.md)

</td><td>

2.4.1

</td><td>

Receive events from the Icinga2 server.

</td></tr><tr><td>

[Apache Kafka Consumer Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/apache-kafka-consumer-connector.md)

</td><td>

-   3.0.0
-   3.2.0

</td><td>

Receive events from the Apache Kafka server.

</td></tr><tr><td>

[ServiceNow Cloud Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-cloud-observability-event-collection.md)

</td><td>

2.1.1 or higher

</td><td>

Receive events from the ServiceNow Cloud Observability platform.

</td></tr><tr><td>

[NagiosXI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-nagios-connector.md)

</td><td>

5.5.2

</td><td>

Receive events from the Nagios XI server.

</td></tr><tr><td>

[NNMi](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-nnmi-connector.md)

</td><td>

10.30.653

</td><td>

Receive events from the NNMi server.

</td></tr><tr><td>

[OBM, also known as OMi v2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-obm-connector.md)

</td><td>

10.01, 10.10, 10.11, 10.12, 10.60, 10.61, and 11.01

</td><td>

Receive alerts from the OBM server.

</td></tr><tr><td>

[OMi](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-omi-connector.md)

</td><td>

10.01, 10.10, 10.11, 10.12, 10.60, and 10.61

</td><td>

Receive alerts from OMi server.

</td></tr><tr><td>

[Op5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-op5-connector.md)

</td><td>

7.3.15

</td><td>

Receive alerts from an OP5 Monitor.

</td></tr><tr><td>

[Opsview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-opsview-connector.md)

</td><td>

5.4.0

</td><td>

Receive alerts from an Opsview Monitor

</td></tr><tr><td>

[PRTG](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-prtg-connector.md)

</td><td>

21.3.71

</td><td>

Receive alerts from a Paessler PRTG Network Monitor source.

</td></tr><tr><td>

[SAP Solution Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-sapsolman-connector.md)

</td><td>

7.2 740 SP16

</td><td>

Receive alerts from an SAP Solution Manager Monitor source.

</td></tr><tr><td>

[SCOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigureSCOMConnector.md)

</td><td>

-   2007 – version 6.1.7221.0
-   2012 - version 7.1.10226.0
-   2016 - version 7.2.117190

</td><td>

Alert and metric collection from the Microsoft System Center Operations Manager \(SCOM\).

</td></tr><tr><td>

[SolarWinds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigureSolarwindsConnectorJS.md)

</td><td>

-   NPM 12.0
-   SAM 6.2.4

</td><td>

Receive events from the SolarWinds monitor.

</td></tr><tr><td>

[vCenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-vcenter-connector.md)

</td><td>

6.5

</td><td>

Receive events from your VMware vSphere environment.

</td></tr><tr><td>

[vRealize](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigurevRealizeConnectorJS.md)

</td><td>

VMware vRealize Operations ManagerSupported version: 8.10.0

</td><td>

Receive events from the vRealize Operations Log and Event Management servers.

</td></tr><tr><td>

[Zabbix](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigureZabbixConnector.md)

</td><td>

5.0.9

</td><td>

Receive alerts from the Zabbix server.

</td></tr></tbody>
</table>## Provided connectors \(push\)

This table lists the connectors that are provided with Event Management. Generic push connectors are also provided, one for event collection through the MID Server and the other through the instance.

Before you begin, ensure the Event Management Connectors plugin is installed in the ServiceNow AI Platform instance. You can download the plugin from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

<table id="table_lhg_dcz_nz"><thead><tr><th>

Connectors

</th><th>

Description

</th><th>

Supported authentication

</th></tr></thead><tbody><tr><td>

[AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/aws-events-transform-script.md)

</td><td>

Use the connector to process Amazon Web Services \(AWS\) alarms as events. The event collection is through the instance.

</td><td>

N/A

</td></tr><tr><td>

[Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/azure-integration.md)

</td><td>

Use OAuth authentication to process Azure platform event messages. The event collection is through the instance.

</td><td>

-   [Integrate Azure Monitor with OAuth authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/azure-events-authentication.md)
-   [Integrate Azure Monitor with basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/azure-events-webhook.md)

</td></tr><tr><td>

[Configure Azure Monitor Bi-directional connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-azure-bi-directional-connector.md)

</td><td>

Use the Azure Monitor Pull connector to send information from ServiceNow Event Management to the Azure Portal.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/azure-events-webhook.md)

</td></tr><tr><td>

[Microsoft Azure MID Push Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-collection-MicrosoftAzure.md)

</td><td>

Collect JSON formatted event messages sent from Microsoft Azure. The collection is through the MID Server.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-collection-MicrosoftAzure.md)

</td></tr><tr><td>

[BMC TrueSight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-collection-BMCTrueSight.md)

</td><td>

Collect JSON formatted event messages sent from BMC TrueSight Operations Management \(TrueSight\). The event collection is through the MID Server.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-collection-BMCTrueSight.md)

</td></tr><tr><td>

[New Relic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/new-relic-events-integration.md)

</td><td>

Collect JSON formatted event messages sent from New Relic. The event collection is through the instance.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/new-relic-events-integration.md)

</td></tr><tr><td>

[Dynatrace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/dynatrace-events-integration.md)

</td><td>

Collect JSON formatted event messages sent from Dynatrace. The event collection is through the instance.

</td><td>

-   [Integrate Dynatrace with OAuth authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/dynatrace-oauth-authentication.md)
-   [Integrate Dynatrace with basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/dynatrace-events-webhook.md)

</td></tr><tr><td>

[Datadog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/datadog-events-integration.md)

</td><td>

Collect JSON formatted event messages sent from Datadog. The event collection is through the instance.

</td><td>

-   [Integrate Datadog with OAuth authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/datadog-oauth-authentication.md)
-   [Integrate Datadog with basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/datadog-events-webhook.md)

</td></tr><tr><td>

[Catchpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/catchpoint-event-collection.md)

</td><td>

Configure the Catchpoint connector to receive Catchpoint events. Event Management can process the Catchpoint events as ServiceNow events.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/catchpoint-event-collection.md)

</td></tr><tr><td>

[Google Cloud Platform \(GCP\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/gcp-events-integration.md)

</td><td>

Collect JSON formatted event messages sent from GCP. The event collection is through the instance.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/gcp-events-integration.md)

</td></tr><tr><td>

[Google Cloud Platform \(GCP\) MID Push Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-collection-GCP.md)

</td><td>

Collect JSON formatted event messages sent from GCP. The event collection is through the MID Server.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-collection-GCP.md)

</td></tr><tr><td>

[Logicmonitor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/logicmonitor-events-integration.md)

</td><td>

Collect JSON formatted event messages sent from Logicmonitor. The event collection is through the instance.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/logicmonitor-events-integration.md)

</td></tr><tr><td>

[Logicmonitor MID Push Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-collection-logicmonitor.md)

</td><td>

Collect JSON formatted event messages sent from Logicmonitor. The event collection is through the MID Server.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-collection-logicmonitor.md)

</td></tr><tr><td>

[Oracle Cloud Push Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/oracle-cloud-events-integration.md)

</td><td>

Use basic authentication to process Oracle Cloud alarms. The event collection is through the instance.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/oracle-cloud-events-integration.md)

</td></tr><tr><td>

[Prometheus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/prometheus-events-integration.md)

</td><td>

Collect JSON formatted event messages sent from Prometheus. The event collection is through the instance.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/prometheus-events-integration.md)

</td></tr><tr><td>

[Sentry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/sentry-events-collection.md)

</td><td>

Configure the Sentry connector to receive Sentry events. Event Management can process the Sentry events as ServiceNow events.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/sentry-events-collection.md)

</td></tr><tr><td>

[SNMP traps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMSNMPTrapEvent.md)

</td><td>

Process SNMP traps as events.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMSNMPTrapEvent.md)

</td></tr><tr><td>

[ThousandEyes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/thousandeyes-events-integration.md)

</td><td>

Collect JSON formatted event messages sent from ThousandEyes. The event collection is through the instance.

</td><td>

-   [Integrate ThousandEyes with OAuth authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-collection-thousandeyes-oauth.md)
-   [Integrate ThousandEyes with basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/event-collection-thousandeyes-oauth.md)

</td></tr><tr><td>

[Email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigureEmailConnector.md)

</td><td>

Configure an inbound email action to send email notifications when events and alerts are triggered.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigureEmailConnector.md)

</td></tr><tr><td>

[Oracle Enterprise Manager trap collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-snmp-trap-listener.md)

</td><td>

Configure the SNMP trap connector to receive Oracle Enterprise Manager Cloud Control SNMP traps. Event Management can process these traps as events.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/configure-snmp-trap-listener.md)

</td></tr><tr><td>

[Grafana](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/grafana-events-integration.md)

</td><td>

Collect JSON formatted event messages sent from Grafana. The event collection is through the instance.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/grafana-events-integration.md)

</td></tr><tr><td>

[EIF listener](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/eif-events-integration.md)

</td><td>

Configure the EIF listener context to receive EIF events. Event Management can process these EIF events as ServiceNow events.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/eif-events-integration.md)

</td></tr><tr><td>

[Integrate Honeycomb events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/honeycomb-event-integration.md)

</td><td>

Configure the Event Management environment for the collection of events from Honeycomb by authenticating Honeycomb as a data source. In the Honeycomb platform, set your ServiceNow AI Platform as the rest endpoint using a webhook.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/honeycomb-event-integration.md)

</td></tr><tr><td>

[Integrate Instana events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/instana-events-integration.md)

</td><td>

Configure Instana with Event Management by adding a standard webhook in the Instana console.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/instana-events-integration.md)

</td></tr><tr><td>

[Integrate Scout APM events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/integrate-scout-apm-events.md)

</td><td>

Enable the collection of events from Scout APM by authenticating Scout APM as a data source to integrate it with Event Management

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/integrate-scout-apm-events.md)

</td></tr><tr><td>

[Integrate Panopta as a data source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/integrate-with-panopta.md)

</td><td>

Configure the Panopta cloud-based monitoring solution with Event Management.

</td><td>

[Basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/integrate-with-panopta.md)

</td></tr><tr><td>

URL format for generic JSON This URL can be used as-is and requires an event rule to be configured.

</td><td>

Configure this generic JSON target URL and configure an event rule to collect events:`https://<<INSTANCE>>/api/sn_em_connector/em/inbound_event?source=genericJson`

</td><td>

N/A

</td></tr></tbody>
</table>## ServiceNow store - connectors

Connectors are available from the ServiceNow store. Download the required content from [ServiceNow Store](https://store.servicenow.com/$appstore.do#!/store/search?q=event%20management).

## Third party connectors

Connectors are also available from third parties. For further information, contact your sales representative for available connectors and listeners.

<table id="table_v1b_bnd_sz"><thead><tr><th>

Third party connectors

</th><th>

Link

</th></tr></thead><tbody><tr><td>

AppDynamics Service Model IntegrationUse this integration to enable your instance to have AppDynamics Application Performance Monitoring data fed into Event Management.

</td><td>

[AppDynamics Service Model Integration](https://store.servicenow.com/$appstore.do#!/store/application/3671b358db0d2200b141d6fdbf9619de/3.0.9?referer=sn_appstore_store.do%23!%2Fstore%2Fsearch%3Fq%3Dappdynamics)

</td></tr><tr><td>

Juniper Mist

 Use this integration to managed service providers and large enterprises the ability to integrate real-time events and alerts from Juniper Mist with ServiceNow platform's Event Management. This capability provides a standardized approach to transform and persist Juniper Mist events in the Events Management table. The events data in ServiceNow allows customers to create their own incidents based on default or user defined alert rules without interacting with the Mist dashboard.

</td><td>

[https://store.servicenow.com/$appstore.do\#!/store/application/e89296eb1b95561019a8a753604bcb24/1.0.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary\_app%25253Bcertified\_apps%25253Bcontent%25253Bindustry\_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative\_ai%25253Bsnow\_solution%26q%3DJuniper%2520Mist&amp;sl=sh](https://store.servicenow.com/$appstore.do#!/store/application/e89296eb1b95561019a8a753604bcb24/1.0.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3DJuniper%2520Mist&sl=sh)

</td></tr><tr><td>

NetScout - nGeniusONE Alert integration

 The NETSCOUT integration module enables nGeniusONE to generate enhanced alerts to ServiceNow ITOM with a contextual launch capability for service triage. ServiceNow ITOM users can launch queries into nGeniusONE from any other alert with that context. nGeniusONE dashboards and reports will support the visualization of those alert conditions to and from ServiceNow ITOM

</td><td>

[NetScout - nGeniusONE Alert integration](https://store.servicenow.com/sn_appstore_store.do/sn_appstore_store.do#!/store/application/f8cfb6bc47b6b810506159f2846d43a1/6.3.3?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DNETSCOUT&sl=sh)

</td></tr><tr><td>

Panopta IntegrationIntegrate with this application for one-directional transfer of events from Panopta to Event Management.

</td><td>

[Panopta integration](https://docs.fortinet.com/product/fortimonitor/24.3)

</td></tr><tr><td>

Splunk IntegrationIntegrate the Splunk Add-on with ServiceNow to enable Splunk users to create incidents and events in Event Management. For more information about the configuration of this integration, see [Splunk Add-on for ServiceNow](http://docs.splunk.com/Documentation/AddOns/released/ServiceNow/ConfigureServiceNowtointegratewithSplunkEnterprise).

</td><td>

[Splunk Integration](https://store.servicenow.com/$appstore.do#!/store/application/bac6db564f6a3100a0fc7d2ca310c721/1.1.7?referer=%2Fstore%2Fsearch%3Fapptype%3Dintegrations%25253Bnonintegrations%26q%3DSplunk%2520Integration&sl=sh)

</td></tr><tr><td>

ScienceLogicIntegrate with this application for one-directional transfer of events from ScienceLogic to Event Management

</td><td>

[ScienceLogic Integration](https://docs.sciencelogic.com/latest/Content/Web_Content_Dev_and_Integration/IS_ServiceNow_Events/is_snow_events_title_web.htm)

</td></tr><tr><td>

SevOneIntegrate with this application for one-directional transfer of events from SevOne to Event Management

</td><td>

[SevOne Integration](https://www.sevone.com/resources/industry-partner/servicenow-alliance/)

</td></tr><tr><td>

Site24X7Integrate with this application for one-directional transfer of events from Site24x7 to Event Management

</td><td>

[Site24x7 Integration](https://www.site24x7.com/help/admin/third-party-integration/servicenow.html)

</td></tr></tbody>
</table>-   **[Create a custom pull connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMCreateCustomConnectorDefinition.md)**  
You can create a customized pull connector that requires a script, connector definition, and connector instance, to retrieve events on behalf of an event source.
-   **[Configure a pull connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigureConnectorInstance.md)**  
Configure a pull connector to schedule the frequency of event collection.
-   **[Configure event collection for SNMP traps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMSNMPTrapEvent.md)**  
The SNMP listener runs on the MID Server, which acts as a collection endpoint for SNMP traps. The MID Server sends the traps to the ServiceNow instance for further processing as an event by Event Management.
-   **[Configure event collection from email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/t_EMConfigureEmailConnector.md)**  
Configure an inbound email action to send email notifications when events and alerts are triggered.

**Parent Topic:**[Event Management Integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/c_EMEvent.md)

