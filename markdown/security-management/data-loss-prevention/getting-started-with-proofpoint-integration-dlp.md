---
title: Getting started with Proofpoint integration for Data Loss Prevention
description: The Proofpoint DLP integration supports the ingestion of Data Loss Prevention alerts created on the Proofpoint dashboard. After ingestion, the incident management functionalities that remediate the DLP incidents will be used.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Data Loss Prevention Incident Response Integration with Proofpoint, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Getting started with Proofpoint integration for Data Loss Prevention

The Proofpoint DLP integration supports the ingestion of Data Loss Prevention alerts created on the Proofpoint dashboard. After ingestion, the incident management functionalities that remediate the DLP incidents will be used.

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

Assign any High Level access or Granular access to the created DLP User.**High level access**: Assign either of the below listed access policy.

-   **Analytics Activity Exploration:** Explore and manage all activity monitored by Information and Cloud Security Platform. This includes the ability to view screenshots, snippets, and raw email data and to manage saved explorations.

![Analytics Activity Exploration - Access policies](../image/dlp-analytics-activity-exploration-access-levels.png "Analytics Activity Exploration - Access Polices") ![]( "Analytics Activity Exploration - Access Polices")

-   **Activity Exploration:** Explore and manage all activity in analytics application monitored by Information and Cloud Security Platform. This includes the ability to view screenshots, snippets and raw email data and to manage saved explorations.

![Activity Exploration - access policies](../image/dlp-proofpoint-activity-exploration.png "Activity Exploration - Access policies")

-   **Granualar access:**: Assign all the below listed access policies.
    -   **Notification View**: View notifications including email, instant messaging, and webhooks for external system integrations.
    -   **Activity View**: View all activity monitored by Information and Cloud Security Platform.
    -   **Alert and Activity Management**: Manage alerts and activities, including workflows, comments and remediations.

![Granualar access policies](../image/dlp-proofpoint-access-polices.png "Granualar access - Access Policies")


For more information navigate to Administration &gt; User Management &gt; Access Policies &gt; Predefined Access Policies Descriptions on Proofpoint Documentation.

</td></tr><tr><td>

Verify that the end-user core application required to support the Proofpoint DLP integration is installed and activated.

</td><td>

Verify that the following DLP applications and security support common applications are installed and activated from ServiceNow Store. If not installed, install, and activate on application. -   Security Support Common
-   Data Loss Prevention Incident Response

</td></tr></tbody>
</table>**Parent Topic:**[Data Loss Prevention Incident Response Integration with Proofpoint](../concept/dlp-incident-response-integration-proofpoint.md)

