---
title: Health Log Analytics release notes
description: The ServiceNow Health Log Analytics application helps you predict IT issues before they impact users by ingesting, analyzing, and correlating machine-generated log data in real time. When Health Log Analytics detects a deviation from a normal pattern, it alerts you of a possible issue. Health Log Analytics was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# Health Log Analytics release notes

The ServiceNow® Health Log Analytics application helps you predict IT issues before they impact users by ingesting, analyzing, and correlating machine-generated log data in real time. When Health Log Analytics detects a deviation from a normal pattern, it alerts you of a possible issue. Health Log Analytics was enhanced and updated in the Yokohama release.

## Health Log Analytics highlights for the Yokohama release

-   Use the enhanced Splunk data input to ingest data from Splunk in a preprocessed structured format. You can also pull data from Splunk regularly using the new Splunk Polling data input.
-   Take advantage of a unified interface for convenient data input integration by setting up integrations from the Integrations Launchpad.
-   Streamline HLA data ingestion with tools for handling large log volumes by using dedicated Cribl and Edge Delta data inputs.
-   Configure log data integrations for Splunk TCP/UDP, Splunk Poller, MID Server, Apache Kafka, Microsoft Azure Log Analytics, REST API, and Amazon Data Firehose conveniently from the Integrations Launchpad.
-   Generate a description of Health Log Analytics alerts using Now Assist.

See [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.

**Important:** [Health Log Analytics](health-log-analytics-rn.md) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Pull data from Splunk regularly using the Splunk Polling data input](https://www.servicenow.com/docs/access?context=hla-data-input-splunk-polling&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Make your data workflows more consistent and productive by fetching data consistently over time using the Splunk Polling data input, which sends recurring queries \(polls\) to Splunk. Handling most configurations on the HLA side means you need minimal additional stakeholder involvement, which enables swift integration with your existing Splunk setup. This enhancement accelerates proofs of concept \(POCs\) and enables faster iterations using real data.

-   **[Use your Splunk data input to ingest preprocessed data from Splunk](https://www.servicenow.com/docs/access?context=hla-data-input-splunk&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Ingest data from Splunk in a preprocessed, structured format using your existing Splunk data input.

-   **[Integrate with log data connectors from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=hla-data-input-setup-integrations&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Take advantage of the Integrations Launchpad's unified interface for convenient integration with log data connectors that feed raw log data from external sources into your instance. You set up log data connectors for HLA from the Event Management Integrations Launchpad in Service Operations Workspace for ITOM. In this release, the Integrations Launchpad enables integration with the following connectors: Elasticsearch, ServiceNow System Logs, UDP, and TCP.

-   **[Use Cribl and Edge Delta data inputs to streamline HLA data ingestion with tools handling large log volumes](https://www.servicenow.com/docs/access?context=hla-data-input-setup-manual&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Use dedicated data inputs to facilitate data ingestion from Cribl or Edge Delta when using these tools to handle large volumes of log data from multiple sources before sending it to HLA.

-   **[Configure log data integrations from the Integrations Launchpad](https://www.servicenow.com/docs/access?context=hla-data-input-setup-integrations&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 36.0.19, benefit from additional log data integrations for Splunk TCP/UDP, Splunk Poller, MID Server, Apache Kafka, Microsoft Azure Log Analytics, and REST API that can be easily set up through the Integrations Launchpad.

-   **[Set up an Amazon Data Firehose integration for real-time log data streaming from multiple sources](https://www.servicenow.com/docs/access?context=il-connector-hla-firehose&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 36.0.19, leverage an integration for streaming log data from Amazon Data Firehose directly to the collector service in ITOM Gateway, where it is queued and then processed by Health Log Analytics. This integration doesn't run on a MID Server and can be configured from the Integrations Launchpad.


## Changed in this release

-   **[Component-based alert grouping is deprecated](https://www.servicenow.com/docs/access?context=hla-op-log-analytics-alert-types&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in version 36.0.19, the adoption of a streamlined two-tier alert model, Log Analytics Group to Single Alert, has replaced component-based alert groups, which have been removed. This model aligns alert representation with the service-level anomalies identified by Health Log Analytics, rather than individual host CIs. The update improves alert visibility, simplifies correlation, and enhances overall alert management efficiency.


## UI changes

-   **[ServiceNow System Logs data input](https://www.servicenow.com/docs/access?context=hla-data-input-glide-syslog&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The Glide Syslog data input has been renamed ServiceNow System Logs data input.


## Activation information

Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Localization information

The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.

## Related ServiceNow applications and features

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The Event Management application uses events generated by Health Log Analytics. When Health Log Analytics detects an anomaly in your log data, it sends an event to Event Management. Event Management receives the event and generates an alert based on event and alert management rules.

-   **[Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Agent data inputs beginning in Health Log Analytics Version 21.0.1 - September 2021 use Agent Client Collector to stream logs to your ServiceNow instance.

-   **[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Health Log Analytics uses the ServiceNow® MID Server product to stream logs to your ServiceNow instance.

-   **[Service Operations Workspace](https://www.servicenow.com/docs/access?context=sow-landing-page-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Health Log Analytics generates alerts in the ServiceNow Service Operations Workspace, a configurable workspace that provides a unified experience for multiple IT Operations Management workflows.


