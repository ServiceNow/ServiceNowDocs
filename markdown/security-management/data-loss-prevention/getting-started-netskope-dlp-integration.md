---
title: Getting started with Netskope DLP integration for Data Loss Prevention
description: Review the following information before you start setting up your Netskope DLP integration for Data Loss Prevention.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response Integration with Netskope, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Getting started with Netskope DLP integration for Data Loss Prevention

Review the following information before you start setting up your Netskope DLP integration for Data Loss Prevention.

<table id="table_qcy_4fw_vbc"><thead><tr><th>

Setup Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify you have assigned the required Now platform, Data Loss Prevention Application.

</td><td>

The following roles are used across the Netskope DLP integration on the ServiceNow AI Platform:-   The Administrator \(admin\) installs the applications from the ServiceNow Store and assigns the Data loss prevention admin \(sn\_dlir.admin\).
-   The user with sn\_dlir.admin role can configure the integration and set up the incident profiles.
-   The users with sn\_dlir.analyst role will have read roles across the integration.

</td></tr><tr><td>

Assign the required privileges for Netskope API v2 token.

</td><td>

The following endpoint privileges are used across the Netskope API v2 tokenization.-   Read: /api/v2/incidents/dlpincidents
-   Read: /api/v2/events/dataexport/events/incident
-   Read + Write: /api/v2/incidents/update

</td></tr><tr><td>

Verify that the end-user core application required to support the Netskope DLP integration is installed and activated.

</td><td>

Verify that the following DLP applications and security support common applications are installed and activated from ServiceNow Store. If not installed, install, and activate on application. -   Security Support Common
-   Data Loss Prevention Incident Response

</td></tr></tbody>
</table>**Parent Topic:**[Data Loss Prevention Incident Response Integration with Netskope](../concept/dlp-incident-response-integration-netskope.md)

