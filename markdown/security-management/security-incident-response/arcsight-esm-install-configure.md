---
title: Install and configure the ServiceNow application for the ArcSight ESM Event Ingestion integration
description: Before you run the integration on your ServiceNow AI Platform instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/arcsight-esm-install-configure.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up instance, ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure the ServiceNow application for the ArcSight ESM Event Ingestion integration

Before you run the integration on your ServiceNow AI Platform® instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  If you have not installed the ArcSight ESM application from the ServiceNow Store for the integration, see [Install a Security Operations integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/install-non-core-apps.md) and follow the steps to install it.

2.  After you have successfully installed the application, navigate to **Integrations** &gt; **Integrations Configurations** and locate the ArcSight ESM tile.

3.  To configure the application, select **New**.

4.  Alternatively, if a **Configure** button is displayed on a tile, select it to edit an existing configuration.

5.  On the form, fill in the fields.

<table id="choicetable_rrp_bwk_kdb"><thead><tr><th align="left" id="d306438e142">

Field

</th><th align="left" id="d306438e145">

Description

</th></tr></thead><tbody><tr><td id="d306438e151">

**Name**

</td><td>

Unique name for the ArcSight ESM Manager that will be used in the integration profile configuration to distinguish amongnst multiple ArcSight ESM Manager sources if required.Spaces are supported for names, but parentheses are not supported.

</td></tr><tr><td id="d306438e169">

**ArcSight API Endpoint URL**

</td><td>

URL for your ArcSight ESM Manager server. Note that the URL should include the API port, for example: `https://arcsight-esm.com:8443`

</td></tr><tr><td id="d306438e184">

**API Account User Name**

</td><td>

User name that you created for your API user account in the ArcSight ESM Manager console.

</td></tr><tr><td id="d306438e196">

**API Password**

</td><td>

Password that you created for your API user account in the ArcSight ESM Manager console.

</td></tr><tr><td id="d306438e209">

**On Premises Deployment**

</td><td>

Default is unchecked. If you are using the cloud-based version of ArcSight ESM that has direct Internet access, verify that the check box is cleared.

 For an on-premises deployment, select this check box and specify the MID Server Application.

</td></tr><tr><td id="d306438e227">

**MID Server Application**

</td><td>

Specify a MID Server Application name here. This MID Server Application can point to any of the MID Servers that have been configured and any MID Server that is available will be used.If you do not have a Mid Server Application configured, you must create a new MID Server Application for this integration.

 **Note:** The MID Server Application can be configured only by users with system administrator role.

</td></tr></tbody>
</table>    To create a new MID Server Application, follow these steps:

    1.  Navigate to **Mid Server** &gt; **Applications** and select **New**.
    2.  Enter a name for the MID Server Application and select a MID Server to be used as the default.
    3.  Deselect the Included in application ALL check box and select **Save**.

        \[Omitted image "ibm-arcsight-config-midserver.png"\] Alt text: ArcSight ESM: Create MID Application

    4.  Select **Edit**. In the **Edit Members** page, select all available MID Servers, move them to the MID Servers List, and select **Save**.
    5.  The selected MID Servers will be listed.
    Depending on the availability, one of the MID Servers configured with the MID Server Application will be used.

6.  Enter the configuration details in the **ArcSight ESM - Event Ingestion Configuration** tile and specify the MID Server Application you have created.

    Each correlation event that you ingest from your ArcSight ESM Manager console requires a unique event profile in your instance. However, the ArcSight ESM source that you configure on the Event Ingestion Configuration form can be reused for multiple profiles as long as each profile ingests unique correlation event types.

7.  Select **Submit**.

    After it is successfully validated and submitted, each ArcSight ESM server configuration is saved on the Security Integrations page as a tile. If your saved configuration tiles are not displayed on the Security Integrations page, on the top right corner of the page, from the Show Configurations choice list, select **Yes**.


## What to do next

You have successfully installed and configured the application. The next step is to create an event profile.

