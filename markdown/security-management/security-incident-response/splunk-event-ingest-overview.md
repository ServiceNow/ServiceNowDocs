---
title: Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow
description: The Splunk Enterprise event and alert data integration with the Security Incident Response \(SIR\) product allows security incident analysts to collect and process security logs and related event data.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow

The Splunk Enterprise event and alert data integration with the Security Incident Response \(SIR\) product allows security incident analysts to collect and process security logs and related event data.

## Overview of Splunk Enterprise Event Ingestion

Data is collected in real-time, and it is used by analysts to identify and report on potential cyber threats. The security events that are collected can be processed into triggered alerts that are ingested automatically with this integration. Also, individual security events can be manually forwarded on-demand from the Splunk Enterprise search and reporting interface into the Security Incident Response product of the ServiceNow AI Platform to create security incidents. You can retrieve notable events from Splunk Enterprise search with the search head cluster configuration. You can achieve this by using the URL and API port of any search head that is a part of the cluster.

This integration provides a security operations center \(SOC\) analyst with visibility to events and related alert data. This data can be integrated into ServiceNow AI Platform Security Incident Response \(SIR\) security incidents for further investigation and remediation. Profiles for Splunk ongoing ingested alerts and forwarded events are created in your ServiceNow AI Platform instance. These profiles customize how different Splunk alert and event fields are displayed on SIR security incidents. A default mapping of alert fields is provided that can be edited and augmented to meet customer-specific needs.

## Key features

This integration includes the following key features:

-   Create multiple alert ingestion profiles to create SIR security incidents for specific types of threats such as phishing and malware.
-   Create multiple event profiles for on-demand event forwarding from your Splunk console to create SIR security incidents.
-   Drag-and-drop mapping of Splunk alert and event field values to associated SIR security incident fields.
-   A preview of the SIR security incident layout based on sample alerts or events to validate profile configuration.
-   Ingest historical alerts as well as ongoing, future alerts on configurable intervals.
-   Aggregate events or alerts to existing SIR security incidents based on matching field values to avoid duplicate security incidents.

## Supported ServiceNow AI Platform versions

The com.snc.si\_dep plugin is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before installing and activating the other Security Operations applications.

The following Security Operations applications must be installed and activated from the ServiceNow Store. Install and then activate one application at a time in the order listed below to ensure a smooth installation:

1.  Security Integration Framework
2.  Security Support Common
3.  Security Support Orchestration
4.  Security Incident Response

For more information about installing the Security Operations core applications, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

## ServiceNow Addons

The ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise is required only if you prefer to forward events manually from your Splunk Enterprise console into your ServiceNow AI Platform instance. This ServiceNow addon is available in [splunkbase](https://splunkbase.splunk.com/).

This ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise application in splunkbase is not required for the automated alert ingestion that is supported by the integration.

## Splunk Supported versions

This integration supports version 6.0 or later of Splunk Enterprise. The integration also supports the Splunk Enterprise Cloud service.

## MID Server

This integration requires an installed and configured MID Server in your ServiceNow AI Platform® instance to connect to the Splunk service if the Splunk server is deployed within your corporate network. If you are using the Splunk Cloud service, a MID Server is not required. For more information about MID Servers, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Integration architecture and systems connection

For more information about the architecture of the integration including key terms and external systems connection details, see [Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-integration-architecture.md).

## Checklist

For a printable checklist of these topics, see [Checklist for Splunk Enterprise Security Notable Event Ingestion integration](../task/splunk-event-ingest-checklist-security.md). You can use this list to monitor your progress as you work through the tasks of the integration.

The images used in the following topics were generated for the Kingston release of the ServiceNow AI Platform. For information about the San Diego user interface, see [Manage security threats using the Security Analyst Workspace](../../security-incident-response/concept/sir-new-ui.md).

The following topics are numbered. Follow the topics listed below in the order that they are presented for a smooth installation and configuration of the application.

1.  [Set up your ServiceNow AI Platform instance for the Splunk Enterprise Event Ingestion integration](../task/splunk-event-ingest-setup-sn.md)  
The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform® instance prior to installing the application from the ServiceNow Store.
2.  [Install and configure the ServiceNow application for the Splunk Enterprise Event Ingestion integration](../task/splunk-event-ingest-install-and-configure.md)  
Before you run the integration on your ServiceNow AI Platform® instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform® instance.
3.  [Create and name an event profile](../task/splunk-event-ingest-create-profile.md)  
Create an event profile in your ServiceNow AI Platform instance and determine which Splunk alerts create security incidents.
4.  [Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-integration-architecture.md)  
The following topic outlines the integration architecture developed to support the ingestion of triggered alerts from the Splunk Enterprise console. This information clarifies, at a high level, the conceptual operation of the integration. It also explains why there are setup steps that are required prior to installing the application from the ServiceNow Store.

**Parent Topic:**[Security Incident Response integrations](../../security-incident-response/concept/sir_integrations.md)

