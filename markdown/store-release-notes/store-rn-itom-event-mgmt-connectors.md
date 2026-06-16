---
title: Event Management Connectors release notes
description: Version history for the IT Operations Management Event Management Connectors on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-event-mgmt-connectors.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 11
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Event Management Connectors release notes

Version history for the IT Operations Management Event Management Connectors on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.19.4 - June 2026**
    -   Changed:
        -   Enhanced OTel metric connector to support Kubernetes metrics out of the box.
        -   Enhanced OTel metric connector to support gzip compression to improve the performance.
        -   Added explicit dependency on API Key and HMAC Authentication, IntegrationHub Action Step - SSH, IntegrationHub Action Step - PowerShell plugins.
    -   Fixed:
        -   PRB2019385 - SOW Integrations Launchpad Metrics Pull Connector Overview tab does not load when connector gathers metrics for large number of hosts
        -   PRB1994893 - Incremental event fetching fails for IBM Netcool events lacking "hostAddress" causing repeated full data syncs instead of incremental updates and missing "serial" field in additional info
        -   PRB2000022 - Netcool connector bi-directional connection not working
        -   PRB2013093 - DataDog push connector instructions needs to be updated
        -   PRB2012580 - Sub Flows in Flow Designer related to the EM Connectors Plugin cannot be opened.
-   **Version 2.18.2 - March 2026**
    -   New:
        -   Implemented OTel Metric Push Connector to push metrics from OTel \(OpenTelemetry\) vendor-neutral open source Observability framework.
        -   DataDog metric connector is available under SOW Integration Launchpad
        -   Enhance SolarWind event connector to support collecting data from AlertHistory table on SolarWinds
    -   Changed: Added support for SCRAM SASL credential type in Kafka Consumer Metric connector
    -   Fixed:
        -   PRB1980000 - PRTG Connector Instance not polling/creating Events
        -   PRB1988250 - Time of event is not correct for custom mid connector when incoming time is in yyyy-MM-dd HH:mm:ss format and PST time zone
        -   PRB1971144 - SCRAM SASL credential type is not working for Kafka Consumer Metric connector
        -   PRB1990493 - MID WebService Event Listener Contexts is not required for Push Connector Metrics Connector
        -   PRB1947827 - LogicMonitor bi-directional update does not process all records in ECC Output Connector probe
        -   PRB1987116 - Dynatrace metric connector query window is always 60 mins irrespective of last\_kpi\_signature
        -   PRB1965410 - Missing advanced configuration options on some integrations for SRM users
        -   PRB1954224 - Severity is missing on Additional Information field on event for custom MID push Connector
-   **Version 2.17.1 - December 2025**
    -   New:
        -   Support OAuth for Kafka Connector - Starting in version 2.17.1, you can use OAuth authentication with the Kafka connector, allowing you to securely connect and manage access without storing or sharing static credentials.
        -   Kafka Metric Connector - Starting in version 2.17.1, you can use the new Kafka connector to stream time-series metric data from Kafka topics into ServiceNow Metric Intelligence for real-time monitoring, anomaly detection, and alerting.
        -   Datadog Metric Connector - Starting in version 2.17.1, you can use the out-of-the-box Datadog metric connector to integrate Datadog metrics with ServiceNow Metric Intelligence, enabling anomaly detection, metric visualization, enrichment, and correlation of metric anomalies with events and log alerts.
        -   Support AWS Event connector across subscriptions - Starting in version 2.17.1, you can forward events from thousands of AWS accounts through a single aggregator account using multi-account AWS SNS event routing, reducing manual setup from 2500 configurations to one and cutting onboarding effort by up to 90%.
        -   Integration Launchpad pages for Dynatrace metric connector - Starting in version 2.17.1, you can use the Dynatrace metric connector from the Integration Launchpad to bring metrics from Dynatrace into ServiceNow Metric Intelligence for visualization, enrichment, dynamic thresholds, and anomaly detection.
        -   SCOM 2025 version support - Starting in version 2.17.1, you can now check SCOM 2025 compatibility with the current code, ensuring that the connector setup, alert collection, and Metric Intelligence data ingestion work seamlessly with the latest SCOM release. This helps maintain integration reliability, reduces configuration errors, and ensures smooth upgrade readiness.
    -   Fixed:
        -   PRB1948286 - Last Event Forwarding Error message is not cleared even though forwarding is success in next attempt
        -   PRB1927558 - LogicMonitor Push Connector listener responds with an error if the payload includes New Zealand timezone abbreviation \(or other common timezones\)
        -   PRB1932728 - Use of unsupported api - GlideDateTime in custom MID push connector script
        -   PRB1916506 - SolarWinds connector pulling unexpected data on first run
        -   PRB1928054 - Zabbix Connector default port and protocols are inconsistent.
-   **Version 2.16.1 - August 2025**
    -   New: Added support for SolarWinds metric connector in Integration Launchpad.
    -   Fixed:
        -   PRB1879082 - Zabbix Connector Event Loss Risk - implement retry for failure cases
        -   PRB1877907 - Event Forwarding not carrying over domain and domain path
        -   PRB1904380 - NagiosXI\_V2 Connector Definition ecc agent script include prints apikey in clear text in Mid Server logs
        -   PRB1877907 - Event Forwarding not carrying over domain and domain path
-   **Version 2.15.1 - May 2025**
    -   Starting with the May release, you can configure metric connector instances for Nagios, SolarWinds, and Zabbix monitoring tools to receive metrics directly from these monitoring tools.
    -   New:
        -   Nagios Metrics Connector
        -   SolarWinds Metrics Connector
        -   Zabbix Metrics Connector
    -   Changed: Certified SolarWinds Events Connector to support SolarWinds version 2024.1
    -   Fixed:
        -   PRB1851380 Kafka Consumer connector error:org.apache.kafka.common.KafkaException: Failed to construct kafka consumer
        -   PRB1830633 Metric name and type is UUID rather than readable text for source "vRealize"
        -   PRB1825234 Zabbix Event Management Connector Does Not Work OOTB With Zabbix Servers Installed With Front End NGINX Web Server
        -   PRB1854696 Azure Monitor Bi directional connector not working with multiple tenant ID
    -   Removed:
        -   Known Issues: Metrics are duplicated in Metric Types and Metric to CI tables, if both Old and New MI Connectors are used simultaneously.
        -   KE Article: KB2054552
-   **Version 2.12.0 - November 2024**
    -   New:
        -   Added API Key authentication support for push connectors
        -   Handled tags for Dynatrace and Datadog connectors - extracted tags from payload and added them to additional info of the event.
        -   Refactor OOB AWS push connector event rules to support 'apply additional matching rules'
        -   Refactor OOB pull connector event rules to support 'apply additional matching rules'
    -   Fixed:
        -   PRB1806047 - ICINGA EM Connector is not able to pull events from source.
        -   PRB1792787 - Time of event is not being correctly populated
        -   PRB1784956 - VMWare vRealize event pull connector not returning Node field for certain event types
        -   PRB1798193 - The getComponents function to query Solarwinds event fetch fails if there too many values for the query
        -   PRB1789798 - Integrations Launchpad error if there is MID Web server context is not configured
-   **Version 2.11.2 - August 2024**
    -   New: Dynatrace Metric Connector
    -   Updated:
        -   Refactored OOB push connector event rules to support 'apply additional matching rules'
        -   Certified other authentication support for below connectors
            -   Dynatrace Event Connector
            -   DataDog Event Connector
    -   Fixed:
        -   vRealize event pull connector doesn't support different authentication types
        -   SolarWinds EM Connector goes OutOfMemory when loading in too many records
        -   Apache Kafka Consumer Connector Instance Fails event collection when JSON contains null values
        -   The script "AWS Events Transform Script" is throwing error with custom domain implementation when using "sn\_em\_connector/em/inbound\_event/aws" endpoint
        -   Dynatrace Monitor push connector to support new Dynatrace payload format
    -   Known Issues: VMWare vRealize event pull connector not returning Node field for certain event types
-   **Version 2.10.0 - June 2024**
    -   New: Grouping Azure Monitor alerts using the 'Alert Processing Rules Correlate Events' feature in the Azure Portal.
    -   Fixed:
        -   Azure Monitor Bi-directional connector throws "Alert Updation Failed" error and stays like that even after getting new Alerts
        -   Incorrect timestamp conversion for the OBM connector, which is causing not able to query for the events and create in instance
        -   IBM Netcool connector bi directional not working when alert identifier has underscores
        -   Push connector "Azure Monitor Push Connector" binds it with object\_id\_1 instead of object\_id causing binding to fail
        -   Zabbix pull connector is changing the severity of closing events to 'clear' instead of maintaining the same severity as the original event payload
-   **Version 2.9.1 - April 2024**
    -   Fixed:
        -   Security fix
        -   SCOM featured metrics are not working if Event Management Connectors app is installed prior to Metrics Intelligence plugin
        -   Netcool connector generated incorrect mapping in event's additional\_info
        -   OBM Connector provides \\\\\\\\n instead of \\n in the event additional information
        -   Issue in vRealizeJS\_v2 script : vRealize\_V2 connection stops working for one event - em\_event not created
        -   Azure Alert auto-close from Closing events not working
        -   Custom mid type connector event is giving old time.
    -   New:
        -   Assignment Group \(Team-based integration\) support added from Integration Launchpad.
        -   SCOM Metric Connector
    -   Changed: Renamed Now on Now Connector job name from 'Event Sync' to 'Event Forwarding'
-   **Version 2.7.0 - November 2023**
    -   New:
        -   Now on Now connector
        -   BMC Truesight V2 connector
    -   Changed:
        -   Changed Kafka Pull Connector to support SSL and SASL\_SSL authentication types
        -   Changed Lightstep Push Connector to support ServiceNow Destination type on the Lightstep platform
        -   Changed Zabbix connector to support Zabbix 6.0+ version
        -   Changed NewRelic connector to support NewRelic version6.4.6.
    -   Fixed:
        -   All things Zabbix \(6.0+\) need to be updated as per their documentation
        -   Alerts not being sent to SN instance/ erroring out when the timezone is IST.
        -   Connector instance Event collection failure after Event Management Connectors plugin upgrade to v2.6
-   **Version 2.6.0 - August 2023**
    -   New:
        -   Custom domain separation support for Push Connectors \(Vancouver only\)
        -   Custom domain separation support for Pull Connectors in store \(Vancouver only\)
        -   Connector instances support for Push Connectors \(\*MID Push Connector instances are supported from Vancouver\)
        -   Tags support for Connectors \(Only works with Integration Launchpad\)
        -   Allow Event Mgmt Admin user to create/modify push connector parameters
    -   Fixed:
        -   Event Management Azure Monitor Not Correlating Events to Alerts Correctly
        -   Bi-directional script is causing Azure Alerts to "Closed" even when the Alert state is "Open".
        -   ThousandEyes sending event with error state after deleting sys\_id from Url
        -   Aws push connector is throwing wrong response if header is missing
        -   Fixed empty JSON string error in ThousandEyes connector
-   **Version 2.5.0 - February 2023**
    -   Changed:
        -   Grafana push connector \(upkeep\): Grafana 9.2.5 version certified
        -   vRealize push connector \(upkeep\): vRealize 8.10 version certified
    -   Fixed: Azure Monitor - ServiceHealth Alert with Subscription not working
-   **Version 2.4.0 - November 2022**
    -   New:
        -   Zabbix V2 Pull Connector
        -   Localization \(i18n\) on-boarding for stored apps
    -   Fixed:
        -   Security fix
        -   Azure Monitor Connector default message key not working.
        -   Existing Event Rules/Event Field mappings not working for V2 Connectors.
-   **Version 2.3.0 - August 2022**
    -   New:
        -   ScoutAPM push connector
        -   Honeycomb push connector
        -   Kafka pull connector
        -   Remediation actions using IH spokes
    -   Changed:
        -   Certify a new version of OpsView pull connector
        -   Certify new version of P5 pull connector \(upkeep\)
    -   Fixed: vCenter connector stuck in attempt status when receiving deleted alarms
    -   Known Issues: Remediation actions: When we have multiple credentials in credential alias, the Powershell action will pick the credentials randomly and fails.
-   **Version 2.2.0 - May 2022**
    -   New:
        -   Sentry push connector
        -   Catchpoint push connector
        -   IBM Instana push connector
-   **Version 2.0.0 - February 2022**
    -   New: Sumologic push connector
    -   Changed:
        -   Realize pull connector \(upgrade\)
        -   vCenter pull connector \(upgrade\)
        -   Added support of severity and timezone in ThousandEyes connector
    -   Fixed:
        -   Time variable is not defined in the Icinga connector script getIcingaTime function
        -   Netcool\_V2 causing failure records in em\_connector\_update\_queue table
        -   API 'thresholdValue' not being used in additional info for googlemonitor source
-   **Version 1.9.0 - December 2021**
    -   Changed:
        -   Nagios XI \(Version: 5.8.6\)
        -   Icinga2 \(Version: 2.13\)
        -   PRTG \(Version: 21.3\)
-   **Version 1.8.2 - October 2021**
    -   New:
        -   Oracle Cloud connector
        -   Prometheus connector
        -   ThousandEyes connector
    -   Changed: Azure monitoring connector enhacements - bi-directional connector
    -   Fixed: OBM connector - error handling for authentication failure
-   **Version 1.7.0 - September 2021**

    New: Lightstep connector

-   **Version 1.6.0 - August 2021**
    -   New: Logicmonitor push connector \(bi-directional\)
    -   Changed:
        -   OBM connector changes - handling duplicate events and source field
        -   AWS push connector - closing events changes
        -   GCP push connector changes - update severity and incident id
    -   Fixed:
        -   PRB1510348 - When OBM server is down test connector fails with "TypeError: Cannot convert null to an object" error &amp; Last event collection status will be success.
        -   PRB1509225 - Unable to get AWS events into em\_event table when using a Gov-Cloud AWS SNS Endpoint
        -   PRB1507379 - OBM connector fails with "OBM API Connection Error when getting Events" error
        -   PRB1501455 - SAP connector not receiving clear events
        -   PRB1497851 - Azure "Log Analytics workspace" alerts are binded to workspace object, instead of the computer set in the dimension
        -   PRB1489389 - Nagios Connector creates unnecessary Critical events.
-   **Version 1.5.0 - June 2021**
    -   New: Azure connector on MID GCP connector on MID OBM connector
    -   Changed: Optimized Event Rules and Event Mapping Update all connectors to consistently return the sys\_id of the event created Datadog connector returns the sys\_id of the event created Azure Common Schema - Changes on Configuration Item Event Management Connector - Binding Rules \(Azure , Datadog , DynaTrace , New Relic\) Fixed Removed
-   **Version 1.4.0 - April 2021**

    New: Grafana webhook connector.

-   **Version 1.3.1 - February 2021**
    -   Two new integrations have been enabled with third party systems through the Push Connector mechanism.
        -   Datadog: Allows integration between the Datadog monitoring system and the ServiceNow Event Management system.
        -   Google Cloud Platform: Enables integration with GCP Monitor, and the pushing of alerts to ServiceNow using rest endpoints.
    -   Additional changes include:
        -   Changed event process to allow a flattened structure of the payload. This provides additional flexibility when using event rules for binding and alert creation.
        -   Upgraded the Netcool Pull Connector integration with the bi-directional feature. This integration uses the REST APIs from Netcool and it updates the Netcool system when an alert is acknowledged in a ServiceNow instance.
-   **Version 1.2.0 - December 2020**
    -   New: Connector for New Relic and DynaTrace monitoring systems
    -   Fixed:
        -   Azure deduping issues for log alerts and metrics
        -   Fixed AWS script for multiple dimensions
-   **Version 1.1.0 - October 2020**
    -   New:
        -   Integration for collection of events from Azure Monitor to Event Management
        -   SolarWinds connector; support for NetObject types added
        -   BMC TrueSight connector
        -   Amazon CloudWatch connector

**Parent Topic:**[ServiceNow Store - ITOM AIOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-ai-ops-landing.md)

