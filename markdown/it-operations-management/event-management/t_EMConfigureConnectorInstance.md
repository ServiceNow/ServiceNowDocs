---
title: Configure a pull connector
description: Configure a pull connector to schedule the frequency of event collection.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure a pull connector

Configure a pull connector to schedule the frequency of event collection.

## Before you begin

Before starting this procedure:

-   Locate or define a connector definition.
-   Create the credentials to connect to the event source.
-   If the connector instance is to be used for the collection of Metric Intelligence metric data, the Metric Intelligence plugin must be activated.

Role required: evt\_mgmt\_admin

## About this task

You can use a connector instance to control the location and manner in which events arrive from external sources. You can optionally select to collect Metric Intelligence information from the external sources that you are connecting to. The Metric Intelligence feature is for the analysis of trends, threshold definitions, and anomaly detection. You can run a test to confirm that connector instance parameters let the MID Server receive events from a supported external event source to the Event \[em\_event\] table. The test also confirms:

-   The MID Server is running.
-   The host is running on the IP address that is in the **Host IP** field.
-   Both the MID Server and the host are running in the same domain.
-   The connector instance value fields are valid.
-   A connection can be made to the event source, using API, to retrieve events.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Click **New**.

3.  Fill in the fields, as appropriate.

<table id="table_knf_tbx_yq"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td id="entry_Name">

Name

</td><td id="entry_NameDescription">

A unique name for the connector instance record, such as the name of event source host.

</td></tr><tr><td id="entry_Description">

Description

</td><td id="entry_DescriptionDescription">

Any optional information that the administrator wants to use to identify this record.

</td></tr><tr><td id="entry_ConnectorDefinition">

Connector definition **Note:** Metric Intelligence connectors \(such as the AWS CloudWatch and AzureConnector\), appear in the base system only if the Metric Intelligence plugin \(com.snc.sa.metric\) is activated.

</td><td>

The vendor and protocol used to gather events from the external event source. Select the connector definition that matches the source of external events. The options available in the base system are, for example: -   AWS CloudWatch
-   AzureConnector
-   HPOM
-   IBM Netcool
-   NagiosXI
-   NNMi
-   OMi
-   SCOM
-   SolarWinds
-   Op5
-   PRTG
-   vCenter
-   Zabbix
For a list of the connector definitions available in the base system, see [Configure Event Management connectors](../reference/connectors-and-listeners.md).

</td></tr><tr><td>

Host IP

</td><td>

The IP address of the event source host. The system uses this IP address to select the appropriate MID Server for communicating with the event source host.

</td></tr><tr><td id="entry_Credential">

Credential

</td><td id="entry_CredentialDesc">

The record from the Credentials \[discovery\_credentials\] table containing valid credentials to the event source host.

</td></tr><tr><td>

Event collection last run time

</td><td>

The date and time of the most recent event import. The value of this field is automatically populated.

</td></tr><tr><td>

Last event collection status

</td><td>

The status of the last import. The value of this field is automatically populated. -   **None** - A valid connection has not yet been established.
-   **Success** - A successful connection was established.
-   **Error** - A connection was established. However the external event source was not updated.


</td></tr><tr><td>

Event collection schedule \(seconds\)

</td><td>

The frequency in seconds that the system checks for new events from the external event source. This value cannot be lower than the minimum schedule property, which by default is 120 seconds.

</td></tr><tr><td id="entry_LastErrorMessage">

Last error message

</td><td id="entry_LastErrorMessageDesc">

Last error message received by the connector. If the test connector fails, an error message appears in this field.

</td></tr><tr><td>

Active

</td><td>

This option appears only after the form has been saved. Do not select this check box until after you test the connection between the MID Server and the connector.

 Select this check box to enable pulling events from this external event source.

</td></tr><tr><td>

Bi-directional

</td><td>

Select to invoke the bi-directional option. This option is available only when the specified connector definition has been configured with bi-directional values. When selected, this option enables the bi-directional exchange of values to-and-from the external event source. The **Last bi-directional status** option appears only when this option is selected. This option appears only if the connector definition that is selected is SCOM.

</td></tr><tr><td>

Last bi-directional status

</td><td>

The value of this field is automatically populated. The status values are: -   **None** - A valid connection has not yet been established.
-   **Success** - A successful connection was established.
-   **Error** - A connection was established. However the external event source was not updated.
 This option appears only if the connector definition that is selected is SCOM.

</td></tr><tr><td id="entry_MetricsCollection">

Metrics collection

</td><td id="entry_MetricsCollectionDescription">

Designates collection of Metric Intelligence metric data. **Note:** The metrics connector supports working against the SCOM database \(MSSQL\) that is configured to work with SSL.

 This option appears only if the connector definition supports metric collection, such as SCOM.

</td></tr><tr><td id="entry_MetricsLastRunTime">

Metrics collection last run time

</td><td id="entry_MetricsLastRunTimeDesc">

The date and time of the most recent metric data collection. The value of this field is automatically populated.

</td></tr><tr><td id="entry_LastMetricsCollectionStatus">

Last metrics collection status

</td><td id="entry_LastMetricsCollectionStatusDesc">

Status of the metric data collection activity. The value of this field is automatically populated.This option appears only if the connector definition that is selected supports metric collection \(such as SCOM\) and if the **Metrics collection** option is selected.

</td></tr><tr><td id="entry_MetricsCollectionSchedule">

Metrics collection schedule \(seconds\)

</td><td id="entry_MetricsCollectionScheduleDesc">

The time, in seconds, to repeat the metric data collection scheduled job.This option appears only if the connector definition that is selected supports metric collection \(such as SCOM\) and when the **Metrics collection** option is selected.

</td></tr><tr><td id="entry_MetricsDBHost">

Metrics database host

</td><td>

Enter either the IP address or the host name of the metrics database host.This option appears only if the connector definition that is selected supports metric collection \(such as SCOM\).

</td></tr><tr><td id="entry_ConnectNamedInstance">

Connect using a named instance

</td><td>

Select to specify the MSSQL named instance to connect to.This option appears only if the connector definition that is selected is SCOM.

</td></tr><tr><td>

Metrics database named instance

</td><td>

The name of the metrics database instance.This option appears only if the connector definition that is selected supports metric collection \(such as SCOM\).

</td></tr><tr><td id="entry_MetricsDBPort">

Metrics database port

</td><td>

The port used by the metric database. The connection is made using JDBC. The base system value is 1,433.This option appears only if the connector definition that is selected supports metric collection \(such as SCOM\).

</td></tr><tr><td id="entry_DBLoginWinAuth">

Database login with Windows authentication

</td><td>

Perform database login with the credentials of the log-on user that is defined on the MID Server service.This option appears only if the connector definition that is selected is SCOM.

</td></tr><tr><td>

Metrics collection running

</td><td>

When selected, indicates that the Metric Intelligence collection is running. This option appears only if the connector definition that is selected supports metric collection \(such as SCOM\).

</td></tr><tr><td id="entry_MetricsDBCredential">

Metrics database credential

</td><td>

Credentials for the metric database.This option appears only if the connector definition that is selected supports metric collection \(such as SCOM\).

</td></tr><tr><td>

Connector Instance Values

</td><td>

The related list containing connection parameters for the event source host. The list of parameters depends on the selected connector definition.

</td></tr><tr><td>

MID Servers for Connectors

</td><td>

The name of theMID Server to process events from the event server.

</td></tr></tbody>
</table>4.  Right-click the form header and select **Save**.

5.  Click **Test connector** to verify that the MID Server can communicate with the external server host.

6.  If the test fails, follow the instructions on the page to correct the problem and then run another test. The description of the reason for failure is shown in the MID Server log, according to the type of error, such as Events, Metrics, or Bi-Directional.

7.  After a successful test, select the **Active** check box and then click **Update**.

8.  Confirm that Event Management processes events using this connector instance by manually creating an event.


-   **[Configure a default MID Server for connectors](t_EMSetDefaultConnector.md)**  
You can set a default MID Server for connectors to ensure that there is always a MID Server available to receive external events.
-   **[Configure the Dynatrace metrics connector instance](configure-dynatrace-connector.md)**  
Configure the Dynatrace connector instance to receive Metric Intelligence raw data from the Dynatrace server.
-   **[Configure the Datadog metrics connector instance](configure-datadog-connector.md)**  
The Datadog Metrics connector retrieves performance metrics from your Datadog environment and sends them to your ServiceNow instance. Users can use SN anomaly detection capabilities and correlate metric anomalies with events and logs alerts.
-   **[Configure the Kafka metrics connector instance](configure-kafka-metrics-connector.md)**  
Configure the Kafka metric consumer connector instance to read message send to Kafka server over topic.
-   **[Configure the Nagios metrics connector instance](configure-nagios-metrics-connector.md)**  
Configure the Nagios metric connector instance to receive Metric Intelligence raw data from the Nagios server.
-   **[Configure the Zabbix metrics connector instance](configure-zabbix-metrics-connector.md)**  
Configure the Zabbix Metric connector instance to receive Metric Intelligence raw data from the Zabbix server.
-   **[Configure the SolarWinds metrics connector instance](configure-solarwinds-connector.md)**  
Configure the SolarWinds connector instance to receive Metric Intelligence raw data from the SolarWinds server.
-   **[Configure event collection from HP OMi](configure-omi-connector.md)**  
Configure the HP Operations Manager \(OMi\) connector instance to receive alerts from the HP OMi server.
-   **[Configure event collection from HPOM](t_EMConfigureHPOMConnector.md)**  
Configure the HPOM connector instance to receive events from HP Operations Manager \(HPOM\).
-   **[Configure event collection from Hyperic](t_EMConfigureHypericConnectorJS.md)**  
Configure the Hyperic connector instance to receive events from the VMware vRealize Hyperic server.
-   **[Configure event collection from IBM Netcool](t_EMUpgradeNetcoolConnector.md)**  
Configure the IBM Netcool\_V2 connector to receive events from IBM Netcool/OMNIbus Object Servers and Impact Servers. The IBM Netcool\_V2 connector uses REST API calls and is bidirectional.
-   **[Configure event collection from an Icinga2 connector](configure-icinga-connector.md)**  
Configure the Icinga 2 \(Icinga\) connector instance to receive events while monitoring your network resources.
-   **[Configure event collection from Logicmonitor](configure-logic-monitor-connector.md)**  
The Logicmonitor pull connector sends information from Event Management to Logicmonitor. It sends responses received from a Push connector in a bi-directional environment to Logicmonitor.
-   **[Configure event collection from NNMi](configure-nnmi-connector.md)**  
Configure the HP Network Node Manager i \(NNMi\) connector instance to receive events while monitoring your network resources.
-   **[Configure event collection from NagiosXI](configure-nagios-connector.md)**  
Configure the NagiosXI connector instance to receive events from the Nagios Core monitor.
-   **[Configure event collection from OBM](configure-obm-connector.md)**  
Configure the Operation Bridge Manager \(OBM\), also known as OMi v2, connector instance to receive alerts from the OBM server. The OBM connector script OBM v2 will be available after installing the Event Management Connectors app.
-   **[Configure OP5 or OP5\_v2 connector](configure-op5-connector.md)**  
Configure the OP5 or OP5\_v2 Monitor connector instance to receive alerts from an OP5 Monitor source.
-   **[Configure Opsview\_v2 connector](configure-opsview-connector.md)**  
Configure the Opsview\_V2 connector instance to receive alerts from an Opsview Monitor source.
-   **[Configure PRTG connector](configure-prtg-connector.md)**  
Configure the PRTG connector instance to receive alerts from a Paessler PRTG Network Monitor source.
-   **[Apache Kafka Consumer Connector](../concept/apache-kafka-consumer-connector.md)**  
The Apache Kafka Consumer connector instance enables you to create events from messages collected from the Apache Kafka topic as a JSON payload that contains essential information in a data block.
-   **[Configure SAP Solution Manager connector](configure-sapsolman-connector.md)**  
Configure the SAP Solution Manager \(Solman\) connector instance to enable communication between the SAP Solution Manager and Event Management.
-   **[Configure alert collection from SCOM](t_EMConfigureSCOMConnectorInstance.md)**  
Alerts from the Microsoft System Center Operations Manager \(SCOM\) are collected using the SCOM connector instance.
-   **[Configure event collection from SolarWinds monitor](t_EMConfigureSolarwindsConnectorJS.md)**  
Configure the SolarWinds monitor connector instance to receive events from the SolarWinds monitor.
-   **[Configure event collection from vCenter](configure-vcenter-connector.md)**  
Configure the VMware vCenter Server \(vCenter or vCenter\_V2\) connector instance to receive events from your VMware vSphere environment.
-   **[Configure event collection from vRealize](t_EMConfigurevRealizeConnectorJS.md)**  
Configure the VMware vRealize Operations \(vRealize or vRealize\_V2\) connector instance to receive events from the vRealize Operations Log and Event Management servers. vRealize uses basic authentication. vRealize\_V2 uses token-based authentication.
-   **[Configure event collection from Zabbix server](t_EMConfigureZabbixConnector.md)**  
Configure the Zabbix server connector instance to receiving alerts from the Zabbix server.

**Parent Topic:**[Configure Event Management connectors](../reference/connectors-and-listeners.md)

**Related topics**  


[Configure Event Management connectors](../reference/connectors-and-listeners.md)

