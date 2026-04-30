---
title: Set up your ServiceNow AI Platform instance for the ArcSight ESM event ingestion integration
description: The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform instance prior to installing the application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [ArcSight ESM Event Ingestion for Security Operations integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up your ServiceNow AI Platform instance for the ArcSight ESM event ingestion integration

The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform® instance prior to installing the application from the ServiceNow Store.

## Before you begin

Role required: admin

## About this task

Refer to the following table and verify that you have completed all the listed tasks before you download and install the application to ensure a smooth installation and configuration.

<table id="table_evy_hpv_3fb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required ServiceNow AI Platform® and Security Incident Response \(SIR\) roles.

</td><td>

The following roles are required for the installation, setup, and use of the integration in your ServiceNow AI Platform® instance.

 -   A user with the ServiceNow AI Platform® administrator role \(admin\) installs the application from the ServiceNow Store and assigns the security incident administrator \(sn\_si.admin\) role.
-   A user with the sn\_si.admin role oversees the following tasks in the ServiceNow AI Platform®:
    -   Names, creates, and edits event profiles.
    -   Selects and maps values from ArcSight ESM correlation events to security incidents.
    -   Previews security incident details for accuracy prior to finalizing the configuration.
    -   Schedules on-going correlated event ingestion.
    -   Enables correlated event updates when a SIR incident is created and closed.
    -   Assigns the security incident analyst \(sn\_si.analyst\) role.
    -   Users with the sn\_si.analyst work with security incidents.

 For more information about roles and assigning roles to users, see Roles on the [Servicenow Product Documentation website](https://servicenow.com/docs).

</td></tr><tr><td>

Verify that you are using version 7.0.0.2436 or later of the ArcSight ESM Manager. Earlier versions are not supported.

</td><td>

If you have access to the ArcSight ESM Query Viewer, you have access to the API that is required for this integration. There is no other special setup required for the API.

</td></tr><tr><td>

Set up the Query Viewer in ArcSight ESM.

</td><td>

Before you can ingest correlation events, you must configure the Query Viewer in the ArcSight ESM console. See [Set up the ArcSight ESM Query Viewer](arcsight-esm-setup-queryviewer.md) for details.

</td></tr><tr><td>

**Optional** Create custom stages in ArcSight ESM for correlation event updates.

</td><td>

A correlation event goes through many stages in its life cycle before it is closed. ArcSight ESM provides default stages like Initial, Monitoring, Queued, and Closed. Some of these stages require user inputs but other stages are automatically applied to the event without any user intervention \(the **User Required** field is unchecked in the ArcSight ESM console. You can create custom stages that do not require any user intervention and use them in your ServiceNow AI Platform® instance. See [Additional options: Automate correlated event updates and closure based on SIR incident status](arcsight-esm-create-profile-additional.md) for details.

</td></tr><tr><td>

Verify that you have installed and configured a MID Server Application.

</td><td>

Configured MID Server ApplicationA MID Server in your ServiceNow AI Platform® instance is required to connect to the ArcSight ESM service if the ArcSight ESM server is deployed within your corporate network. See [Install and configure the ServiceNow application for the ArcSight ESM Event Ingestion integration](arcsight-esm-install-configure.md) for instructions on how to configure a MID Server Application.

 See the [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for information about MID Servers.

 If you are using a hosted or cloud service, that is Internet accessible, a MID Server is not required.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application for the integration.

</td><td>

Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

 1.  Security Incident Response
2.  Security Integration Framework
3.  Security Support Common
4.  Event and Alert Ingestion for Security Operations: This application requires:
    -   com.glide.hub.integration.runtime =&gt; ServiceNow IntegrationHub Runtime
    -   com.glide.hub.action\_step.rest =&gt; ServiceNow IntegrationHub Action Step - REST
5.  Threat Core

 For more information about installing the Security Operations core applications, see [Get entitlement for a Security Operations product or application](../../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr></tbody>
</table>## What to do next

You have successfully set up your ServiceNow AI Platform® instance for the integration. The next step is to install the ArcSight ESM Security Event Ingestion for Security Operations application from the ServiceNow Store for the integration.

