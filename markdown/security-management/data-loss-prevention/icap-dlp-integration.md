---
title: Internet Content Adaption Protocol \(ICAP\) integration for DLP IR
description: The Internet Content Adaption Protocol \(ICAP\) DLP integration supports the ingestion of Data Loss Prevention Incident Response alerts, allows the fetching of match content, and evidence files from Amazon S3 created on the ICAP supported Data Loss Prevention Incident Response deployment.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2024-09-03"
reading_time_minutes: 3
breadcrumb: [DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Internet Content Adaption Protocol \(ICAP\) integration for DLP IR

The Internet Content Adaption Protocol \(ICAP\) DLP integration supports the ingestion of Data Loss Prevention Incident Response alerts, allows the fetching of match content, and evidence files from Amazon S3 created on the ICAP supported Data Loss Prevention Incident Response deployment.

After the alerts are ingested, you can use the DLP workspace to view the required key information such as match content, alert severity, and various incident management functionalities to remediate the DLP incidents.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Overview and key features

The Internet Content Adaption Protocol \(ICAP\) integration helps you to track the usage and movement of sensitive data on various platforms.

This integration includes the following key features:

-   Ingestion of DLP Alerts: Users would be able to configure and schedule the ingestion of DLP alerts from specified Amazon S3 buckets. This includes the capability to perform delta imports to ensure only new data is ingested.
-   Display ingested alerts in the DLP Workspace: Once the alerts are ingested, they should be displayed in the DLP workspace, providing key details about each alert such as match content, alert severity, and relevant metadata.
-   Match content: Sensitive information records are created during ingestion, match content is fetched when the record is opened.
-   Evidence file download: The system would allow users to download associated evidence files directly from the DLP workspace for further investigation or review.
-   Ability to customize and define the severity mapping between ICAP DLP incidents with ServiceNow incidents.

-   **[Getting started with ICAP DLP integration for Data Loss Prevention](getting-started-icap-integration.md)**  
Before you can use the integration, you must download it from the ServiceNow® Store
-   **[Install and configure the ICAP DLP integration](install-icap-dlp-integration.md)**  
Install and configure the  provider ICAP DLP integration from the  ServiceNow® Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  provider ICAP DLP incident data.
-   **[Create a profile for ICAP DLP integration](../task/create-profile-for-icap.md)**  
Create an incident profile in your  ServiceNow AI Platform instance. Determine the  ICAP DLP alerts that are suitable for creating DLP incidents.
-   **[View sensitive information for DLP alerts](../task/view-match-content.md)**  
View the detected sensitive information for DLP alerts.
-   **[Download evidence files for DLP alerts](../task/download-icap-evidence-files.md)**  
Download files that violate the DLP policy on provider that supports ICAP. Download this file onto your local machine from the DLP IR Analyst workspace and DLP IR End user workspace for approvers.
-   **[Preview evidence files for ICAP](../task/preview-file-icap.md)**  
Preview DLP incident evidence files in the DLP IR Analyst workspace.
-   **[Review the ICAP DLP integration settings](../task/review-the-icap-dlp-integration-settings.md)**  
Review the provider ICAP DLP integration settings and modify the default system properties to suit your environment.

**Parent Topic:**[DLP integrations](../../data-loss-prevention/concept/dlp-integrations.md)

**Related topics**  


[Symantec Integration for Data Loss Prevention Incident Response](../../dlp-symantec/concept/symantec-dlp-integration.md)

[Data Loss Prevention Incident Response Integration with Proofpoint](../../dlp-proofpoint/concept/dlp-incident-response-integration-proofpoint.md)

[Data Loss Prevention Incident Response Integration with Netskope](../../dlp-netskope/concept/dlp-incident-response-integration-netskope.md)

[Data Loss Prevention Incident Response with Microsoft](../../dlp-microsoft/concept/dlp-integration-microsoft.md)

