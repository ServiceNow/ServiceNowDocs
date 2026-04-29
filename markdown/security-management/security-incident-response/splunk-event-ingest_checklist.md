---
title: Checklist for the Splunk Enterprise Event Ingestion integration
description: Use this checklist to guide you through all the tasks of the integration. The following checklist includes setup and installation tasks and examples of use cases that include expected results for the integration.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration architecture and external systems connection, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Checklist for the Splunk Enterprise Event Ingestion integration

Use this checklist to guide you through all the tasks of the integration. The following checklist includes setup and installation tasks and examples of use cases that include expected results for the integration.

## Before you begin

Role required: admin

## About this task

Track your progress with the setup, installation, and configuration of the integration with the following table. Complete all the tasks for a step before moving on to the next step. Each row of the table lists tasks and identifies the roles that are required to perform the tasks. Numbered topics of the installation and configuration guide are also referenced.

Roles required: Roles are listed for each step below.

## Procedure

1.  As a user with the ServiceNow AI Platform admin role, set up your ServiceNow AI Platform instance.

    -   Assign users with the **sn\_si.ingestion\_profile\_admin** \(or sn\_si.admin\) and sn\_si.analyst roles as required.
    -   Install and configure a MID Server if the Splunk server is deployed within your corporate network.
    -   Verify that the ServiceNow Security Incident Response plugins are activated for your release of the ServiceNow AI Platform.
    -   If you want to forward events manually from your Splunk Enterprise console into your ServiceNow AI Platform instance, verify that you have assigned the \(sn\_sec\_splunk\_v2.api\_account\_access\) role to a user with the Splunk Enterprise enterprise administrator permission.
    For more information, see [Set up your ServiceNow AI Platform instance for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-setup-sn.md).

    You have successfully completed the set up steps and verified expected results for the integration.

2.  As a user with the ServiceNow AI Platform admin role, install and configure the Splunk Enterprise Event Ingestion application from the ServiceNow Store.

    1.  Download and install the application on your ServiceNow AI Platform instance.
    2.  Configure the application and connect to your Splunk Enterprise console.
    For more information, see [Install and configure the ServiceNow application for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-install-and-configure.md).

3.  If you intend to export events manually from your Splunk Enterprise console to your ServiceNow AI Platform instance, perform the following tasks:

    1.  As a Splunk Enterprise administrator, install, set up, and enable the ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise from splunkbase in your Splunk Enterprise console.

    2.  As a Splunk Enterprise administrator, if not already configured, save searches as alerts in your Splunk Enterprise console.

        For more information, see [Set up ServiceNow Event Ingestion Integration add-on](splunk-event-ingest-setup-prereqs.md) and [Save searches in your Splunk Enterprise console for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest_save_search.md).

4.  As a user with the ServiceNow AI Platform **sn\_si.ingestion\_profile\_admin** role, create and name an event profile.

    Select the profile type from the choice list. Options are a scheduled alert profile that you use to ingest sample data, or, an event profile that you use to export attachment data manually from your Splunk Enterprise console.

    -   For a scheduled alert, select an available alert.
    -   For profile for manually exported data, create a new map or copy an existing map.
    For more information, see [Create and name an event profile](splunk-event-ingest-create-profile.md).

5.  As a user with the ServiceNow AI Platform **sn\_si.ingestion\_profile\_admin** role, map values ingested or attachment data that is exported from Splunk Enterprise to ServiceNow AI Platform security incidents.

    1.  Fetch sample data for a scheduled alert.
    2.  Export attachment data manually from Splunk Enterprise for an event.
    3.  Edit the default mapping configuration.
    4.  Optionally add filtering criteria, append an alert to an existing security incident, and use the script editor.
    For more information, see [Mapping alerts and events for the Splunk Enterprise Event Ingestion integration](../concept/splunk-event-ingest-mapping.md) and [Map alerts for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-map-alerts.md).

6.  As a user with the ServiceNow AI Platform **sn\_si.ingestion\_profile\_admin** role, preview the data from Splunk Enterprise that is displayed on a ServiceNow AI Platform security incident.

    Fix any errors or add any missing data so that no error messages are displayed.

    For more information, see [Preview security incident for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-preview.md).

7.  As a user with the ServiceNow AI Platform **sn\_si.ingestion\_profile\_admin** role, schedule alert retrieval for a profile with a scheduled alert.

    For more information, see [Schedule and retrieve alerts for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-schedule.md).


**Parent Topic:**[Integration architecture and external systems connection for the Splunk Enterprise Event Ingestion integration](../concept/splunk-event-ingest-integration-architecture.md)

