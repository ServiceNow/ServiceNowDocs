---
title: Set up your ServiceNow AI Platform instance for the Secureworks CTP ticket ingestion integration
description: The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform instance prior to installing the application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Secureworks CTP Ticket Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up your ServiceNow AI Platform instance for the Secureworks CTP ticket ingestion integration

The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform instance prior to installing the application from the ServiceNow Store.

## Before you begin

Role required: sn\_si.admin

## About this task

Refer to the following table and verify that you have completed all the listed tasks before you download and install the application to ensure a smooth installation and configuration.

<table id="table_evy_hpv_3fb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required ServiceNow AI Platform and Security Incident Response roles.

</td><td>

The following roles are required for the installation, setup, and use of the integration in your ServiceNow AI Platform instance.

 -   A user with the ServiceNow AI Platform administrator role \(admin\) installs the application from the ServiceNow Store and assigns the SIR administrator \(sn\_si.admin\) role.
-   A user with the sn\_si.admin role oversees the following tasks in the ServiceNow AI Platform:
    -   Names, creates, and edits profiles.
    -   Selects and maps Secureworks CTP ticket fields to the security incident fields.
    -   Previews security incident details for accuracy prior to finalizing the configuration.
    -   Schedules on-going ticket ingestion.
    -   Enables ticket updates when a SIR SIR incident is created and closed.
    -   Assigns the security incident analyst \(sn\_si.analyst\) role.
    -   Users with the sn\_si.analyst work with security incidents.

 For more information about roles and assigning roles to users, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td></tr><tr><td>

Verify that you are using the following versions: -   Secureworks Ticket API 4.0
-   Secureworks Event API 1.0
-   Secureworks Enrichment API 1.0

</td><td>

If you have access to the Secureworks CTP portal, you have access to the API that is required for this integration. There is no other special setup required for the API.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application for the integration.

</td><td>

Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

 1.  Security Incident Response
2.  Event and Alert Ingestion for Security Operations \(Required for SIEM integrations\): This application requires:

    -   com.glide.hub.integration.runtime =&gt; ServiceNow IntegrationHub Runtime
    -   com.glide.hub.action\_step.rest =&gt; ServiceNow IntegrationHub Action Step - REST
**Note:** The Integration Hub components are installed along with the Event and Alert Ingestion plugin. If these are not installed, contact Customer Support for assistance.


 For more information about installing the Security Operations core applications, see [Get entitlement for a Security Operations product or application](../../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr></tbody>
</table>