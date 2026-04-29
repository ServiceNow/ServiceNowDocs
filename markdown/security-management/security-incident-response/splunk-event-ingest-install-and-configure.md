---
title: Install and configure the ServiceNow application for the Splunk Enterprise Event Ingestion integration
description: Install and configure Splunk Enterprise security- Event Ingestion integration from the ServiceNow Store on your ServiceNow AI Platform instance.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure the ServiceNow application for the Splunk Enterprise Event Ingestion integration

Install and configure Splunk Enterprise security- Event Ingestion integration from the ServiceNow Store on your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  If you have not installed the Splunk Enterprise Event Ingestion application from the ServiceNow Store for the integration, see [Install a Security Operations integration](../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

2.  Navigate to **All** &gt; **Integrations** &gt; **Integrations Configurations**

3.  Search for **Splunk Enterprise security- Event Ingestion** tile, and select **Configure**.

4.  On the form, fill in the fields.

<table id="choicetable_rrp_bwk_kdb"><thead><tr><th align="left" id="d234475e135">

Field

</th><th align="left" id="d234475e138">

Description

</th></tr></thead><tbody><tr><td id="d234475e144">

**Name**

</td><td>

Name of the Splunk Enterprise console or Splunk Cloud instance used for the integration.Spaces are supported for names, but parentheses are not supported. For example, enter `HQ-USA`, or `HQ USA`.

</td></tr><tr><td id="d234475e168">

**Splunk API Base URL**

</td><td>

URL for your Splunk Enterprise console or Splunk Cloud instance.

</td></tr><tr><td id="d234475e183">

**Basic Authentication**

</td><td>

Default is disabled.If you are using API Account User Name and API Password for configuration, enable the check box.

</td></tr><tr><td id="d234475e195">

**API Account User Name**

</td><td>

User name that you created for your individual user account on the Splunk Enterprise console.

</td></tr><tr><td id="d234475e208">

**API Password**

</td><td>

Password that you created for your individual user account on the Splunk Enterprise console.

</td></tr><tr><td id="d234475e220">

**Token Based \(available from version 12.0.0\)**

</td><td>

Token based authentication that you created for your API user account on the Splunk Enterprise console.

</td></tr><tr><td id="d234475e235">

**Token**

</td><td>

Token that you created for your API user account on the Splunk Enterprise console.

</td></tr><tr><td id="d234475e247">

**MID Server**

</td><td>

Specific MID Server that is set up in your environment. Only MID Servers that are active and validated are available from this choice list.

</td></tr><tr><td id="d234475e256">

**On Premises Deployment**

</td><td>

Default is disabled. If you are using the cloud-based version of Splunk Enterprise, verify that the check box is cleared.

 If this option is enabled, the MID Server choice list is displayed. If you are using an on-premises version of Splunk Enterprise, follow these steps to select a MID Server.

 1.  Select the check box.

A choice list is displayed. Default is **Any**.

2.  Select **Any** only if this MID server is configured for the Splunk Enterprise Event Ingestion integration.
3.  From the choice list, select the ServiceNow AI Platform® MID server that you configured in your instance for this specific integration.


</td></tr></tbody>
</table>    Each Splunk Enterprise alert that you ingest from your Splunk Enterprise console requires a unique event profile in your ServiceNow AI Platform® instance. However, the source that you configure on the Event Ingestions Configuration form can be reused for multiple ServiceNow AI Platform® profiles as long as each profile ingests unique Splunk triggered alerts.

5.  Select **Submit**.

    The configured integration tile displays.


If an error message is displayed after you click **Submit**, enter your information again and click **Submit**.

## What to do next

You have successfully installed and configured the application. The next step is to create an event profile.

-   **[Configure Splunk Enterprise Event Ingestion settings](configure-splunk-enterprise-event-ingestion-settings.md)**  
Use the Splunk Enterprise Event Ingestion settings to modify the preset configurations and their values as per your requirements.

**Parent Topic:**[Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow](../concept/splunk-event-ingest-overview.md)

**Previous topic:**[Set up your ServiceNow AI Platform instance for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-setup-sn.md)

**Next topic:**[Configure Splunk Enterprise Event Ingestion settings](configure-splunk-enterprise-event-ingestion-settings.md)

