---
title: Install and configure the ServiceNow application for the Splunk Enterprise Event Ingestion integration
description: Before you run the integration on your ServiceNow AI Platform instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform instance.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure the ServiceNow application for the Splunk Enterprise Event Ingestion integration

Before you run the integration on your ServiceNow AI Platform® instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform® instance.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  If you have not installed the Splunk Enterprise Event Ingestion application from the ServiceNow Store for the integration, see [Install a Security Operations integration](../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

2.  After you have successfully installed the application, navigate to **Integrations** &gt; **Integrations Configurations** and locate the Splunk Event Ingestions tile.

3.  To configure the application, click **New**.

    ![Splunk new configuration tile.](../image/Splunktile_new.png)

4.  Alternatively, if a **Configure** button is displayed on a tile, click it to edit an existing configuration.

5.  In the Event Ingestions Configuration dialog that is displayed, fill in the fields.

<table id="choicetable_rrp_bwk_kdb"><thead><tr><th align="left" id="d232951e168">

Field

</th><th align="left" id="d232951e171">

Description

</th></tr></thead><tbody><tr><td id="d232951e177">

**Name**

</td><td>

Name of the Splunk Enterprise console or Splunk Cloud instance used for the integration.Spaces are supported for names, but parentheses are not supported. For example, enter `HQ-USA`, or `HQ USA`.

</td></tr><tr><td id="d232951e201">

**Splunk API Base URL**

</td><td>

URL for your Splunk Enterprise console or Splunk Cloud instance.

</td></tr><tr><td id="d232951e216">

**Basic Authentication**

</td><td>

Default is disabled.If you are using API Account User Name and API Password for configuration, enable the check box.

</td></tr><tr><td id="d232951e228">

**API Account User Name**

</td><td>

User name that you created for your individual user account on the Splunk Enterprise console.

</td></tr><tr><td id="d232951e241">

**API Password**

</td><td>

Password that you created for your individual user account on the Splunk Enterprise console.

</td></tr><tr><td id="d232951e253">

**Token Based \(available from version 12.0.0\)**

</td><td>

Token based authentication that you created for your API user account on the Splunk Enterprise console.

</td></tr><tr><td id="d232951e268">

**Token**

</td><td>

Token that you created for your API user account on the Splunk Enterprise console.

</td></tr><tr><td id="d232951e280">

**MID Server**

</td><td>

Specific MID Server that is set up in your environment. Only MID Servers that are active and validated are available from this choice list.

</td></tr><tr><td id="d232951e289">

**On Premises Deployment**

</td><td>

Default is disabled. If you are using the cloud-based version of Splunk Enterprise, verify that the check box is cleared.

 If this option is enabled, the MID Server choice list is displayed. If you are using an on-premises version of Splunk Enterprise, follow these steps to select a MID Server.

 1.  Select the check box.

A choice list is displayed. Default is **Any**.

2.  Select **Any** only if this MID server is configured for the Splunk Enterprise Event Ingestion integration.
3.  From the choice list, select the ServiceNow AI Platform® MID server that you configured in your instance for this specific integration.


</td></tr></tbody>
</table>    The following figure is an example of a completed form for a configuration of an on-premises version of Splunk Enterprise with a MID Server.

    ![Configuration form with fields populated.](../image/splunk-event-ingestion-auth.png)

    Each Splunk Enterprise alert that you ingest from your Splunk Enterprise console requires a unique event profile in your ServiceNow AI Platform® instance. However, the source that you configure on the Event Ingestions Configuration form can be reused for multiple ServiceNow AI Platform® profiles as long as each profile ingests unique Splunk triggered alerts.

6.  Click **Submit**.

    After validation is successfully completed, the Security Integrations page is displayed with each of your configurations. On each valid configuration tile, **Configure** and **Delete** buttons are displayed as shown in the following figure.

    **Note:** You have to use either Basic Authentication or Token Based Authentication only. Enable one of the authentications and enter the corresponding authentication details. Enabling both will display an error.

    After it is successfully validated and submitted, each Event Ingestions Splunk server configuration is saved on the Security Integrations page as a tile. If your saved configuration tiles are not displayed on the Security Integrations page, on the top right corner of the page, from the Show Configurations choice list, click **Yes**.

    ![Configuration form for Splunk Enterprise event ingestion configuration.](../image/splunk_214_ConfigurationScreen.png)


If an error message is displayed after you click **Submit**, enter your information again and click **Submit**.

## What to do next

You have successfully installed and configured the application. The next step is to create an event profile.

-   **[Configure Splunk Enterprise Event Ingestion settings](configure-splunk-enterprise-event-ingestion-settings.md)**  
Use the Splunk Enterprise Event Ingestion settings to modify the preset configurations and their values as per your requirements.

**Parent Topic:**[Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow](../concept/splunk-event-ingest-overview.md)

**Previous topic:**[Set up your ServiceNow AI Platform instance for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-setup-sn.md)

**Next topic:**[Configure Splunk Enterprise Event Ingestion settings](configure-splunk-enterprise-event-ingestion-settings.md)

