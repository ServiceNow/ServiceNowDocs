---
title: Install and configure the Symantec DLP integration for Data Loss Prevention
description: Install and configure the  Symantec DLP integration from the  ServiceNow Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  Symantec DLP incident data.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Symantec Integration for Data Loss Prevention Incident Response, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Install and configure the Symantec DLP integration for Data Loss Prevention

Install and configure the  Symantec DLP integration from the  ServiceNow® Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  Symantec DLP incident data.

## Before you begin

Role required: sn\_dlir.admin

## Procedure

1.  Download the  Symantec DLP integration from the  ServiceNow® Store and install it.

2.  Navigate to **Security Operations** &gt; **Integrations ** &gt; **Integration Configurations**.

3.  Search for the  DLP Incident Response Integration with Symantec tile and click  **Configure**.

    ![Click Configure button for Symantec.](../../data-loss-prevention/image/dlp-symantec.png)

4.  On the form, fill in the fields.

<table id="table_efq_dph_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Symantec DLP integration configuration.

</td></tr><tr><td>

Endpoint URL

</td><td>

Symantec REST API endpoint.

</td></tr><tr><td>

Username

</td><td>

Symantec account name. For information on the Roles and Permissions required, see [Roles and Permissions](https://techdocs.broadcom.com/us/en/symantec-security-software/information-security/data-loss-prevention/15-8/DLP-Enforce-REST-APIs-overview/overview/Creating-a-user-and-roll-for-an-Incident-Reporting-API-client.html).

</td></tr><tr><td>

Password

</td><td>

Symantec account password.

</td></tr><tr><td>

On-Premises Deployment

</td><td>

Option that you can select if your Symantec is deployed in an on-premises instance. When you select this option, you must use the MID Server to connect to Symantec.

</td></tr><tr><td>

MID Server Application

</td><td>

The MID Application name that is used to communicate with Symantec.This field is needed when you select the **On-Premises Deployment** option.

</td></tr></tbody>
</table>    ![Configure the DLP Incident Response integration with Symantec.](../../data-loss-prevention/image/dlp-symantec-config.png)

5.  Click **Submit**.


## Result

**Note:** Please connect symantec sub prod to the ServiceNow sub prod. Keep all the username and passwords in sync across the instances to avoid accounts getting logged out.

After you successfully validate and submit the configuration, the Symantec DLP Integration is saved on the Security Integrations page as a tile.

**Parent Topic:**[Symantec Integration for Data Loss Prevention Incident Response](../concept/symantec-dlp-integration.md)

