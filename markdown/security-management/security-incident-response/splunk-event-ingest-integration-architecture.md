---
title: Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration
description: The following topic outlines the integration architecture developed to support the ingestion of triggered alerts from the Splunk Enterprise console. This information clarifies, at a high level, the conceptual operation of the integration. It also explains why there are setup steps that are required prior to installing the application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration

The following topic outlines the integration architecture developed to support the ingestion of triggered alerts from the Splunk Enterprise console. This information clarifies, at a high level, the conceptual operation of the integration. It also explains why there are setup steps that are required prior to installing the application from the ServiceNow Store.

## Key terms used for this integration

The following key terms are used during the installation and configuration. For more information about these terms, see the [ServiceNow Product Documentation website](https://servicenow.com/docs) and the [Splunk website](https://www.splunk.com/) and resources on [Splunk Resources](https://www.splunk.com/en_us/resources/getting-started.html) page.

-   **ServiceNow AI Platform**

    An enterprise ServiceNow product. The ServiceNow AI Platform is the base upon which individual components such as Security Incident Response \(SIR\), IT Service Management \(ITSM\), and other products are built.

-   **ServiceNow Splunkbase Addon**

    A ServiceNow application that is installed on your Splunk Enterprise console that supports the manual event forwarding option of the integration. Manual event forwarding is an optional feature of the integration. This ServiceNow Splunkbase addon is not required for the automated alert ingestion that is provided by the integration.

-   **Security Incident Response \(SIR\)**

    A ServiceNow AI Platform application that tracks the progress of security incidents from discovery and initial analysis, through containment, eradication, and recovery, and into the final post incident review and closure.

-   **Splunk Enterprise**

    An automated security incident event management \(SIEM\) product or cloud service that collects data used for incident analysis and management. This service is on a host that is sometimes also referred to as a Splunk console in this guide.

-   **Splunk alert**

    A search that you configure and save in Splunk to scan for specific data based in the parameters you set up in the Splunk Enterprise service. When you pull alerts from Splunk, you also pull all the events associated with that alert.

-   **Splunk triggered alert**

    A configured search in the Splunk Enterprise console that returns results and flags these results as triggered alerts. The triggered alerts are ingested from the Splunk console into your ServiceNow AI Platform instance for this integration. Triggered alerts have one or more Splunk events.

-   **Splunk event**

    One or more data elements that result in the triggered alerts of the Splunk service. From your ServiceNow AI Platform instance, you can look up which Splunk events triggered ServiceNow AI Platform security incidents.

-   **MID Server**

    This application facilitates communication and movement of data between the ServiceNow AI Platform and external applications, data sources, and services. This application is typically required for integration with on-premises technologies, and, for this Splunk Enterprise Event Ingestion integration, the MID Server facilitates communication between the ServiceNow AI Platform and the on-premises instance of Splunk Enterprise. A MID Server is not required if you are integrating your ServiceNow AI Platform instance with a Splunk Cloud instance.

-   **Security incident admin \(sn\_si.admin\)**

    The user with this role oversees the configuration of the integration with the SIR product in your ServiceNow AI Platform instance.

-   **Security incident analyst \(sn\_si.analyst\)**

    The user with this role interacts with and analyzes security incidents in the ServiceNow Security Incident Response product.

-   **Security incident profile admin \(sn\_si.ingestion\_profile\_admin\)**

    The user with this role configures the plugin, create, edit, delete and maintain ingestion profiles for Azure Sentinel, Splunk and Splunk ES Integration for the SIR product in your ServiceNow AI Platform instance.


## External systems connection

An event profile is a container that you create, name, and configure for a singular connection and call to the Splunk service to pull the most current triggered alerts that match specific criteria. After triggered alerts that match your profile have been pulled from Splunk, you select which of these alerts you want displayed as a ServiceNow AI Platform Security Incident Response SIR security incident. A default view of the Splunk Enterprise alert fields is available, and you edit this mapping of alert fields to the fields on a SIR security incident to meet your needs. You preview your mapping to verify that you have all the required alert field values populated on the SIR security incident. To complete the configuration of the alert profile, you schedule the retrieval of alerts and then activate the profile. After you activate the profile in the ServiceNow AI Platform, you are ready to ingest historical and on-going Splunk alerts automatically.

As a user with the sn\_si.admin role, if you determine that a new triggered alert is similar to alerts previously ingested, you can aggregate new triggered alerts to existing SIR security incidents. You set criteria to specify matching target field values in the Splunk Enterprise alert profile that define when an existing security incident is updated and when a new security incident is created. If the aggregation feature is enabled in your event profile, when the import set is transformed, your ServiceNow AI Platform instance checks for an existing record in the target table that has the same value in the target and source fields. If an existing record with a matching value in the target table is found, that record is updated. If no matching record is found, a new record is created in the target table. If enabled, the aggregation option updates existing security incidents with new triggered alerts, and you avoid creating multiple security incidents. For more information about updating records using aggregation options, see [Updating records using coalesce](https://www.servicenow.com/docs/access?context=c_ImportSetCoalesce&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

This application uses the Splunk API service to retrieve information from the Splunk service. An outbound HTTPS connection from the MID server to this environment is necessary for the integration to work properly.

After it is connected to the Splunk service, the integration supports the pulling and ingestion of triggered alerts and events that trigger security incidents.

The basic data flow is illustrated in the following figures. In each figure, your ServiceNow AI Platform is pulling \(ingesting\) data. Splunk is not pushing data for scheduled alerts.

![Connection with single MID server.](../image/splunk-canvas-single-MID.png "Connection to on premises Splunk enterprise service with single MID server")

![Configuration two.](../image/splunk-canvas-1.png "Connection to a Splunk enterprise cloud instance")

![Multiple MID servers.](../image/splunk-canvas-multiple-MID.png "Multiple connections to the Splunk enterprise service using multiple MID servers")

-   **[Copy Splunk Enterprise Event Ingestion profiles from one instance to another using export/import functionality](../task/export-and-import-splunk-event-profile-data.md)**  
You can export and import Splunk Enterprise Event Ingestion profiles settings from one ServiceNow AI Platform instance to a different ServiceNow AI Platform instance.
-   **[Copy an event profile for the Splunk Enterprise Event Ingestion integration](../task/splunk-event-ingest-copy-a-profile.md)**  
Copy an existing profile and its associated settings instead of creating new profiles. If you are creating multiple profiles, and you want to reuse the settings of an existing profile, you might prefer to copy alarm profiles to save time.
-   **[Set up ServiceNow Event Ingestion Integration add-on](../task/splunk-event-ingest-setup-prereqs.md)**  
Install and set up the ServiceNow Event Ingestion Integration add-on in your Splunk enterprise console or Splunk Cloud instance.
-   **[Using ServiceNow Event Ingestion Integration add-on](../task/use-v2-addon.md)**  
Map alerts from Splunk console to create a Security Incident Response \(SIR\) on the ServiceNow instance.
-   **[Save searches in your Splunk Enterprise console for the Splunk Enterprise Event Ingestion integration](../task/splunk-event-ingest_save_search.md)**  
The following steps for saving searches in your Splunk Enterprise console are provided for a user with the Splunk Enterprise administrator role.
-   **[Use the script editor to format alert values for the Splunk Enterprise Event Ingestion integration](../task/splunk-event-ingest_script_editor.md)**  
Use the script editor to format field values on the security incident during the mapping step.
-   **[Checklist for the Splunk Enterprise Event Ingestion integration](../task/splunk-event-ingest_checklist.md)**  
Use this checklist to guide you through all the tasks of the integration. The following checklist includes setup and installation tasks and examples of use cases that include expected results for the integration.

**Parent Topic:**[Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow](splunk-event-ingest-overview.md)

**Previous topic:**[Schedule and retrieve alerts for the Splunk Enterprise Event Ingestion integration](../task/splunk-event-ingest-schedule.md)

**Next topic:**[Copy Splunk Enterprise Event Ingestion profiles from one instance to another using export/import functionality](../task/export-and-import-splunk-event-profile-data.md)

