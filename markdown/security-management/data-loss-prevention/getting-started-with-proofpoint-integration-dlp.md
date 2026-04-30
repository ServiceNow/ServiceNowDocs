---
title: Getting started with Proofpoint integration for Data Loss Prevention
description: The Proofpoint DLP integration supports the ingestion of Data Loss Prevention incidents created on the Proofpoint Data Loss Prevention tenant. After ingestion, the incident management functionalities that remediate the DLP incidents will be used.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response Integration with Proofpoint, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Getting started with Proofpoint integration for Data Loss Prevention

The Proofpoint DLP integration supports the ingestion of Data Loss Prevention incidents created on the Proofpoint Data Loss Prevention tenant. After ingestion, the incident management functionalities that remediate the DLP incidents will be used.

## Checklist

Review the following information before you start setting up your Proofpoint DLP integration for Data Loss Prevention.

<table id="table_opd_dxv_3tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify you have assigned the required ServiceNow AI Platform and Data Loss Prevention Incident Response application roles.

</td><td>

The following roles are used across the Proofpoint DLP integration on the ServiceNow AI Platform: -   The administrator \(admin\) installs the applications from the ServiceNow® Store and assigns the Data loss prevention admin \(sn\_dlir.admin\).
-   The user with sn\_dlir.admin role can configure the integration and set up the incident profiles.
-   The users with sn\_dlir.analyst role have read roles across the integration.

</td></tr><tr><td>

Assign the required Proofpoint DLP user roles.

</td><td>

Review the Proofpoint DLP integration roles and permissions.

</td></tr><tr><td>

Verify you are using Proofpoint DLP 1.0.1 or later.

</td><td>

The Proofpoint DLP integration for Data Loss Prevention is tested with Proofpoint Data Loss Prevention, version 1.0.1 or later.

</td></tr><tr><td>

Verify that the end-user core application required to support the Proofpoint DLP integration is installed and activated.

</td><td>

Verify that the following DLP applications and security support common applications are installed and activated from ServiceNow Store. If not installed, install, and activate on application. -   Security Support Common
-   Data Loss Prevention Incident Response

</td></tr></tbody>
</table>**Parent Topic:**[Data Loss Prevention Incident Response Integration with Proofpoint](../concept/dlp-incident-response-integration-proofpoint.md)

