---
title: Install and configure the Servicenow application for Microsoft Graph Security API alert ingestion integration
description: Before you run the integration on your ServiceNow AI Platform instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform instance.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up instance, Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure the Servicenow application for Microsoft Graph Security API alert ingestion integration

Before you run the integration on your ServiceNow AI Platform® instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  If you have not installed the Microsoft Graph Security API application from the ServiceNow Store for the integration, see [Install a Security Operations integration](../../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

2.  After you have successfully installed the application, navigate to **Integrations** &gt; **Integrations Configurations** and locate the Microsoft Graph Security API - Alert Ingestion tile.

    ![Microsoft Graph Security API: configure](../image/ms-graph-config-tile.png)

3.  To configure the application, click **Configure**.

4.  In the Alert Ingestions Configuration dialog that is displayed, fill in the fields.

<table id="choicetable_rrp_bwk_kdb"><thead><tr><th align="left" id="d63829e138">

Field

</th><th align="left" id="d63829e141">

Description

</th></tr></thead><tbody><tr><td id="d63829e147">

**Name**

</td><td>

Name of the Microsoft Azure Cloud instance. You can enter only alphanumeric values and hyphens \(-\) in this field.

</td></tr><tr><td id="d63829e162">

**Tenant ID**

</td><td>

The Microsoft Azure Tenant ID. This is the instance from which all the alerts in the Microsoft Azure portal are retrieved.

</td></tr><tr><td id="d63829e177">

**Client ID**

</td><td>

The Client ID for the application that you have registered in the Microsoft Azure portal. See [Configure the Microsoft Azure portal](ms-graph-configure-azure.md) for details.

</td></tr><tr><td id="d63829e202">

**Client Secret**

</td><td>

The password for your registered application.

</td></tr></tbody>
</table>5.  Click **Submit**.

    After it is successfully validated and submitted, each alert ingestions server configuration is saved on the Security Integrations page as a tile. If your saved configuration tiles are not displayed on the Security Integrations page, on the top right corner of the page, from the Show Configurations choice list, click **Yes**.


## What to do next

You have successfully installed and configured the application. The next step is to create an alert profile.

