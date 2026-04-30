---
title: Install and configure the ServiceNow application for the Secureworks CTP ticket ingestion integration
description: Before you run the integration on your ServiceNow AI Platform instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform instance.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setup instance, Secureworks CTP Ticket Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure the ServiceNow application for the Secureworks CTP ticket ingestion integration

Before you run the integration on your ServiceNow AI Platform instance, complete these installation and configuration steps so the application properly integrates with the Security Incident Response and Security Operations products on your ServiceNow AI Platform instance.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  If you have not installed the Secureworks CTP ticket application from the ServiceNow Store for the integration, see [Install a Security Operations integration](../../../security-incident-response/task/install-non-core-apps.md) and follow the steps to install it.

2.  After you have successfully installed the application, navigate to **Integrations** &gt; **Integrations Configurations** and locate the Secureworks CTP Ticket Ingestion Integration tile.

    ![Secureworks CTP: Configure](../image/secureworks-config.gif)

3.  To configure the application, click **New**.

4.  Alternatively, if a **Configure** button is displayed on a tile, click it to edit an existing configuration.

5.  In the dialog that is displayed, fill in the fields.

<table id="choicetable_rrp_bwk_kdb"><thead><tr><th align="left" id="d268763e154">

Field

</th><th align="left" id="d268763e157">

Description

</th></tr></thead><tbody><tr><td id="d268763e163">

**Name**

</td><td>

Name of the Secureworks CTP instance used for the integration. You can enter only alphanumeric values and hyphens \(-\) in this field.

</td></tr><tr><td id="d268763e178">

**Description**

</td><td>

Enter a description for the user account.

</td></tr><tr><td id="d268763e187">

**Username**

</td><td>

Enter the username for the Secureworks CTP API account. Note that the username is case sensitive. To find the username, follow these steps:

-   Login to the Secureworks CTP portal.
-   Navigate to **Account** &gt; **Account Management** &gt; **API Credentials**. The username is displayed on the API Credential page.


</td></tr><tr><td id="d268763e225">

**API Password**

</td><td>

Enter the Secureworks CTP API Password. To find the API Password, follow these steps:

-   Login to the Secureworks CTP portal.
-   Navigate to **Account** &gt; **Account Management** &gt; **API Credentials**. The API Password is displayed on the API Credential page.
For more information on how to obtain the username and API password, follow the steps in the Generating a Persistent API Key section of the Secureworks Ticketing API Guide.

</td></tr></tbody>
</table>6.  Click **Submit**.

    After it is successfully validated and submitted, each configuration is saved on the Security Integrations page as a tile.


## Result

If your saved configuration tiles are not displayed on the Security Integrations page. On the top right corner of the page, from the **Show Configurations** choice list, click **Yes**.

