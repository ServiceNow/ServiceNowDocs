---
title: Set up your ServiceNow AI Platform instance for the IBM QRadar offense ingestion integration
description: The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform instance prior to installing the application from the ServiceNow Store.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up your ServiceNow AI Platform instance for the IBM QRadar offense ingestion integration

The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform® instance prior to installing the application from the ServiceNow Store.

## Before you begin

Role required: sn\_si.admin

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
    -   Names, creates, and edits offense profiles.
    -   Selects and maps IBM QRadar offense data fields to the security incident fields.
    -   Previews security incident details for accuracy prior to finalizing the configuration.
    -   Schedules on-going offense ingestion.
    -   Enables offense updates when a SIR incident is created and closed.
    -   Assigns the security incident analyst \(sn\_si.analyst\) role.
    -   Users with the sn\_si.analyst work with security incidents.

 For more information about roles and assigning roles to users, see Roles on the [Servicenow Product Documentation website](https://servicenow.com/docs).

</td></tr><tr><td>

Verify that you are using the following versions:-   IBM QRadar version 7.3.2 or later.
-   IBM QRadar API version 10 or later.

Earlier versions are not supported.

</td><td>

If you have access to the IBM QRadar console, you have access to the API that is required for this integration. There is no other special setup required for the API.

</td></tr><tr><td>

Verify that you have installed and configured a MID Server Application.

</td><td>

Configured MID Server Application.A MID Server in your ServiceNow AI Platform® instance is required to connect to the IBM QRadar service if the IBM QRadar server is deployed within your corporate network. See the [ServiceNow Product Documentation website](https://servicenow.com/docs) for information about MID Servers.

 If you are using the IBM QRadar Cloud service, a MID Server is not required.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application for the integration.

</td><td>

Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

 1.  Security Incident Response
2.  Event and Alert Ingestion for Security Operations: This application requires:

    -   com.glide.hub.integration.runtime =&gt; ServiceNow IntegrationHub Runtime
    -   com.glide.hub.action\_step.rest =&gt; ServiceNow IntegrationHub Action Step - REST
**Note:** The Integration Hub components are installed along with the Event and Alert Ingestion plugin. If these are not installed, contact Customer Support for assistance.


 For more information about installing the Security Operations core applications, see [Get entitlement for a Security Operations product or application](../../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr></tbody>
</table>## What to do next

You have successfully set up your ServiceNow AI Platform® instance for the integration. The next step is to install the IBM QRadar application from the ServiceNow Store for the integration.

