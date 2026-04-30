---
title: Set up your ServiceNow AI Platform instance for the Splunk Enterprise Event Ingestion integration
description: The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform instance prior to installing the application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up your ServiceNow AI Platform instance for the Splunk Enterprise Event Ingestion integration

The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform® instance prior to installing the application from the ServiceNow Store.

## Before you begin

Role required: admin

## About this task

Refer to the following table and verify that you have completed all the listed tasks before you download and install the application to ensure a smooth installation and configuration.

## Procedure

1.  Verify that you have assigned the required ServiceNow AI Platform® and Security Incident Response \(SIR\) roles.

    The following roles are required for the installation, setup, and use of the integration in your ServiceNow AI Platform® instance.

    -   A user with the ServiceNow AI Platform® administrator role \(admin\) installs the application from the ServiceNow Store and assigns the security incident administrator \(sn\_si.admin\) role.
    -   If you want to forward events manually from Splunk Enterprise for this integration, a user with the ServiceNow AI Platform® admin role assigns a user with the \(sn\_sec\_splunk\_v2.api\_account\_access\) role in the ServiceNow AI Platform®. This role permits a user with the Splunk Enterprise administrator role to access the API in the ServiceNow AI Platform® that is required for manual event forwarding for this integration.

        The \(sn\_sec\_splunk\_v2.api\_account\_access\) role is not required for the integration if you are ingesting alerts automatically from Splunk Enterprise into your ServiceNow AI Platform® instance.

    -   A user with the sn\_si.admin role oversees the following tasks in the ServiceNow AI Platform®:
        -   Names, creates, and edits alert and event profiles.
        -   Selects and maps values from alerts and events to ServiceNow AI Platform® security incidents.
        -   Previews security incident details for accuracy prior to finalizing the configuration.
        -   Schedules on-going alert ingestion.
        -   Assigns the security incident analyst \(sn\_si.analyst\) role.
        -   Users with the sn\_si.analyst work with security incidents.
    For more information about roles and assigning roles to users, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

2.  Verify that you are using version 6.0 or later of the Splunk API.

    If you have access to the Splunk Enterprise console, you have access to the API that is required for this integration. There is no other special setup required for the API.

3.  Verify that you have installed and configured a MID Server.

    A MID Server in your ServiceNow AI Platform® instance is required to connect to the Splunk service if the Splunk server is deployed within your corporate network. For more information about MID servers, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

    If you are using the Splunk Cloud service, a MID Server is not required.

4.  Verify that the ServiceNow core applications required to support the integration are installed and activated.

    The Security Incident Response Dependency plugin \(com.snc.si\_dep\) is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications required by the integration.

    Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

    1.  Security Incident Response
    2.  Security Integration Framework
    3.  Security Support Common
    4.  Security Support Orchestration
    For more information about installing the Security Operations core applications, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).


## What to do next

You have successfully set up your ServiceNow AI Platform® instance for the integration. The next step is to install the Splunk Enterprise Event Ingestion application from the ServiceNow Store for the integration. For more information, see [Install and configure the ServiceNow application for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-install-and-configure.md).

If you have not saved searches in your Splunk Enterprise console for ingestion, or if you are performing the initial setup for this integration in your Splunk Enterprise console and the Security Operations product of your ServiceNow AI Platform® instance simultaneously, see [Save searches in your Splunk Enterprise console for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest_save_search.md) for more information.

If you want to export events manually and on-demand from your Splunk Enterprise console for the integration, see [Set up ServiceNow Event Ingestion Integration add-on](splunk-event-ingest-setup-prereqs.md) for more information.

**Parent Topic:**[Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow](../concept/splunk-event-ingest-overview.md)

**Previous topic:**[Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow](../concept/splunk-event-ingest-overview.md)

**Next topic:**[Install and configure the ServiceNow application for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-install-and-configure.md)

