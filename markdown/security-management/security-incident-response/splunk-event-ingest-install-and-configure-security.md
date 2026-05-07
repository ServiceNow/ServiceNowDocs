---
title: Install and configure Splunk Enterprise Security Notable Event Ingestion integration
description: Install and configure Splunk Enterprise Security Notable Event Ingestion integration for Security Operations application from the ServiceNow Store on your ServiceNow AI Platform instance.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure Splunk Enterprise Security Notable Event Ingestion integration

Install and configure Splunk Enterprise Security Notable Event Ingestion integration for Security Operations application from the ServiceNow Store on your ServiceNow AI Platform® instance.

## Before you begin

Role required: ess\_analyst

Assign a Security Analyst \(ess\_analyst\) user role in Splunk ES to perform all integration-related activities on the Splunk server.

## About this task

Configure Splunk ES- Event Ingestion integration 

## Procedure

1.  If you have not installed the Splunk Enterprise Security Event Ingestion application from the ServiceNow Store for the integration, see [Install a Security Operations integration](../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

2.  After you have successfully installed the application, navigate to **All** &gt; **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

3.  Search for **Splunk Enterprise Security- Event Ingestion** tile, and select **Configure**.

4.  On the form, fill in the fields.

<table id="choicetable_rrp_bwk_kdb"><thead><tr><th align="left" id="d259029e155">

Field

</th><th align="left" id="d259029e158">

Description

</th></tr></thead><tbody><tr><td id="d259029e164">

**Name**

</td><td>

Name of the Splunk Enterprise Security console or Splunk Cloud instance used for the integration.Spaces are supported for names, but parentheses are not supported. For example, enter `SplunkES2`.

</td></tr><tr><td id="d259029e185">

**Splunk API Base URL**

</td><td>

URL for your Splunk Enterprise Security console or Splunk Cloud instance. The URL should include the API port, for example: `https://mysplunkserver.com:8089`

</td></tr><tr><td id="d259029e203">

**Basic Authentication**

</td><td>

Default is disabled.If you are using API Account User Name and API Password for configuration, enable the check box.

</td></tr><tr><td id="d259029e215">

**API Account User Name**

</td><td>

User name that you created for your API user account on the Splunk Enterprise Security console.

</td></tr><tr><td id="d259029e228">

**API Password**

</td><td>

Password that you created for your API user account on the Splunk Enterprise Security console.

</td></tr><tr><td id="d259029e240">

**Token Based \(available from version 12.0.0\)**

</td><td>

Token that you created for your API user account on the Splunk Enterprise Security console.

</td></tr><tr><td id="d259029e249">

**Token**

</td><td>

Token that you created for your API user account on the Splunk Enterprise Security console.

</td></tr><tr><td id="d259029e261">

**On Premises Deployment**

</td><td>

Default is disabled. If you’re using an on-premise based version of Splunk Enterprise Security, verify that this check box is selected.

</td></tr><tr><td id="d259029e275">

**MID Server**

</td><td>

Option to choose a particular MID Server to set up in your environment, which will be used by this integration to pull notable events into ServiceNow. You can select a specific MID Server from the list or select **Any** to enable an auto-selection of a valid MID Server from the list for this integration.

**Note:**

-   The MID Server selected during this configuration time applies throughout this integration.
-   Only MID Servers that are active and validated are displayed on this list. By default, the value is set to **Any**.
For example, there are three MID Servers A, B, and C. If you select **Any**, then one of these MID Servers is auto-selected and applies throughout this integration. If you select a specific MID Server, say C, then the selected MID Server C applies throughout this integration.

If you want to change the MID Server, then you have to reconfigure it from the App Configuration tile.

</td></tr></tbody>
</table>    Each Splunk Enterprise Security notable event type that you ingest from your Splunk Enterprise Security incident review console requires a unique event profile in your ServiceNow AI Platform® instance. However, the source that you configure on the Event Ingestion Configuration form can be reused for multiple ServiceNow AI Platform® profiles as long as each profile ingests unique notable event types.

5.  Select **Submit**.

    The configured integration tile displays.


## What to do next

[Create and name an event profile for the Splunk Enterprise Security event ingestion integration](splunk-event-ingest-create-profile-security.md)

