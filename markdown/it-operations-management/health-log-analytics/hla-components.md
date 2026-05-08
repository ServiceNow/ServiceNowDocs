---
title: Components installed with Health Log Analytics
description: Activating the Health Log Analytics, Health Log Analytics Viewer and Health Log Analytics Core plugins adds several components.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Components installed with Health Log Analytics

Activating the Health Log Analytics, Health Log Analytics Viewer and Health Log Analytics Core plugins adds several components.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

## Plugins

<table id="table_oh5_clh_2nb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health Log Analytics

</td><td>

Health Log Analytics is an AI-powered log analysis solution capable of preventing IT incidents before users are affected. It automatically identifies your environment and logs, predicts IT incidents, generates alerts, and provides expert suggestions for fixing issues. Health Log Analytics is a ServiceNow Store app. Once installed, the module is available, but you can choose not to interact with it.

 Dependency:

 -   Health Log Analytics Core
-   The ServiceNow® [Event Management](../../event-management/concept/c_EM.md) application

</td></tr><tr><td>

Health Log Analytics Viewer

</td><td>

Event Management operators use the Health Log Analytics Viewer plugin to browse logs by timestamp or time range. Health Log Analytics Viewer enables Event Management operators to search for a specific log text and visualize the frequency of hits in a particular time period.Dependency: The ServiceNow® [Event Management](../../event-management/concept/c_EM.md) application.

</td></tr><tr><td>

Health Log Analytics Core

</td><td>

This plugin contains essential components for Health Log Analytics, such as the AI Engine and Elasticsearch.Health Log Analytics Core is a ServiceNow Store app. Once installed, the module is available, but you can choose not to interact with it.

 Dependency: The ServiceNow® [Event Management](../../event-management/concept/c_EM.md) application.

</td></tr></tbody>
</table>## Roles

Health Log Analytics uses the following roles.

|Role title \[name\]|Description|
|-------------------|-----------|
|Event Management Administrator \[evt\_mgmt\_admin\]|Has read and write access to all Event Management features to configure Health Log Analytics.|
|Event Management Operator \[evt\_mgmt\_operator\]|Has read access to all Event Management features. Has write access to alerts to manage the alert life cycle. Has the itil role to manage incidents created from alerts. Can also activate operations on alerts, such as to acknowledge, close, and open an incident and run remediation.|

## Lists

Health Log Analytics adds the following lists.

<table id="table_qw5_22s_cnb"><thead><tr><th>

Table \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Advanced Log Alert Filtering \[sn\_occ\_advanced\_alert\_filtering\]

</td><td>

Controls processing of alert metrics with feedback options. Enables providing more complex feedback to the AI engine.Beginning with the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), this representation no longer displays.

</td></tr><tr><td>

Advanced Log Alert Filter \[sn\_occ\_advanced\_alert\_filter\]

</td><td>

Controls processing of alert metrics with feedback options. Enables providing more complex feedback to the AI engine.**Note:** This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td></tr><tr><td>

Data Inputs \[sn\_occ\_base\_data\_input\_config\]

</td><td>

Enables setting up data input connectors to stream log data into the instance.

</td></tr><tr><td>

Data Input Mapping \[sn\_occ\_event\_mapper\]

</td><td>

Enables mapping raw log data that streams into the instance to determine how Health Log Analytics processes it.

</td></tr><tr><td>

Data Input Preprocessor \[sn\_occ\_data\_input\_preprocess\_screen\]

</td><td>

Enables editing raw log data before the system maps and structures it.

</td></tr><tr><td>

Define Alert \[sn\_occ\_custom\_alert\]

</td><td>

Enables creating custom alerts based on a predefined set of rules.

</td></tr><tr><td>

Excluded Values \[sn\_occ\_auto\_service\_normalizer\]

</td><td>

Enables configuring Health Log Analytics to stop extracting specific log data that is not descriptive enough or contains redundant text or information.

</td></tr><tr><td>

Extracted Values \[sn\_occ\_auto\_service\_mapper\]

</td><td>

Enables configuring Health Log Analytics to extract a specific term found in a field and map it to a specified component.

</td></tr><tr><td>

Features \[sn\_occ\_features\]

</td><td>

Lists all Health Log Analytics features. The features can be activated and deactivated.

</td></tr><tr><td>

Lexical Keywords \[sn\_occ\_lexical\_keywords\]

</td><td>

Shows all default lexical keywords that Health Log Analytics looks for in log data.

</td></tr><tr><td>

Log Correlator \[sn\_occ\_log\_correlator\]

</td><td>

Shows all correlators that determine whether to correlate different alerts to the same group. Enables adding correlators to Health Log Analytics.

</td></tr><tr><td>

Log Sources \[sn\_occ\_sources\]

</td><td>

Provides a view of all data input sources when the log data has been mapped. Enables controlling properties and correlators for these sources.

</td></tr><tr><td>

Muted Metrics \[sn\_occ\_metric\_state\]

</td><td>

Shows all muted alert metrics together with the muted components. Enables reactivating the muted alert metrics.

</td></tr><tr><td>

Source Type \[sn\_occ\_source\_type\]

</td><td>

Contains the source types extracted in the mapping process.

</td></tr><tr><td>

Source Type Structure \[sn\_occ\_source\_type\_structure\]

</td><td>

Enables fine-tuning the source type structure. Provides a view of all source types when the log data has been mapped. Source types define how Health Log Analytics treats specific sources and how it parses the logs.

</td></tr><tr><td>

Streaming Sources \[sn\_occ\_log\_streaming\_source\_stats\]

</td><td>

Enables monitoring all entities that stream log data to the instance.

</td></tr><tr><td>

System Health – Notifications \[sn\_occ\_health\_check\]

</td><td>

Shows all system health notifications together and enables updating their status.

</td></tr><tr><td>

System Properties \[sn\_occ\_system\_settings\]

</td><td>

Displays system properties and enables customizing their values.

</td></tr><tr><td>

Timestamp Formats \[sn\_occ\_timestamp\_formats\]

</td><td>

Displays predefined timestamp formats. Enables defining and adding timestamp formats.

</td></tr><tr><td>

Time Zones \[sn\_occ\_time\_zones\]

</td><td>

Enables deleting records in sn\_occ\_time\_zones for users with the evt\_mgmt\_admin role.

</td></tr></tbody>
</table>## Forms

Health Log Analytics adds the following forms.

|Table \[name\]|Description|
|--------------|-----------|
|Beats Data Input \[sn\_occ\_data\_input\_config\_filebeat\]|Enables configuring advanced settings for Beats data input connectors.|
|Beats Linux \(Filebeat\) \[sn\_occ\_data\_input\_connector\_filebeat\]|Enables configuring Filebeat data input connectors.|
|Elasticsearch Data Input \[sn\_occ\_data\_input\_config\_elastic\]|Enables configuring an Elasticsearch data input.|
|MID Server Data Input \[sn\_occ\_data\_input\_config\_midserver\]|Enables configuring a MID Server data input.|
|Rsyslog \[sn\_occ\_data\_input\_connector\_rsyslog\]|Enables configuring Rsyslog data input connectors.|
|Rsyslog Data Input \[sn\_occ\_data\_input\_config\_rsyslog\]|Enables configuring advanced settings for Rsyslog data input connectors.|
|TCP Data Input Configuration \[sn\_occ\_data\_input\_config\_tcp\]|Enables configuring advanced settings for TCP data input connectors.|
|Windows Beats \[sn\_occ\_data\_input\_connector\_winbeat\]|Enables configuring Windows Beats data input connectors.|
|WinLog Beats \[sn\_occ\_data\_input\_connector\_winlogbeat\]|Enables configuring WinLog Beats data input connectors.|

**Parent Topic:**[Health Log Analytics reference](../concept/hla-reference.md)

