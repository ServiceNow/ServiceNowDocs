---
title: DLP integrations
description: The Data Loss Prevention Incident Response base system includes integrations to third-party data loss prevention software packages.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response, Security Operations]
---

# DLP integrations

The Data Loss Prevention Incident Response base system includes integrations to third-party data loss prevention software packages.

This section provides instructions for activating the plugins and configuring both ServiceNow and third-party integrations. Also included are some basic guidelines for developing your own integrations, as well as details on specific integrations included in the base system.

## Integration Configurations

The base system includes a series of cards for each of the integration implementations you can activate and use. Also, cards are displayed for any integrations posted on the ServiceNow Store that have dependencies on Security Operations plugins. The integration cards can be viewed by selecting **Security Operations** &gt; **Integration Configurations**.

Data Loss Prevention Incident Response supports the following third-party data loss prevention software packages:

-   **[Symantec Integration for Data Loss Prevention Incident Response](../../dlp-symantec/concept/symantec-dlp-integration.md)**  
The Symantec DLP integration supports the ingestion of Data Loss Prevention Incident Response incidents created on the Symantec Data Loss Prevention Incident Response deployment. After ingestion, you can use the incident management functionalities to remediate the DLP incidents.
-   **[Data Loss Prevention Incident Response Integration with Proofpoint](../../dlp-proofpoint/concept/dlp-incident-response-integration-proofpoint.md)**  
The Proofpoint DLP integration supports the ingestion of Data Loss Prevention incidents created on the Proofpoint Data Loss Prevention deployment. After ingestion, you can use the incident management functionalities to remediate the DLP incidents.
-   **[Data Loss Prevention Incident Response Integration with Netskope](../../dlp-netskope/concept/dlp-incident-response-integration-netskope.md)**  
The Netskope DLP integration supports the ingestion of Data Loss Prevention incidents created on the Netskope Data Loss Prevention deployment. Netskope DLP helps companies to track the usage and movement of sensitive data on various platforms.
-   **[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](../../dlp-icap-zscaler/concept/icap-dlp-integration.md)**  
The Internet Content Adaption Protocol \(ICAP\) DLP integration supports the ingestion of Data Loss Prevention Incident Response alerts, allows the fetching of match content, and evidence files from Amazon S3 created on the ICAP supported Data Loss Prevention Incident Response deployment.
-   **[Data Loss Prevention Incident Response with Microsoft](../../dlp-microsoft/concept/dlp-integration-microsoft.md)**  
The Data Loss Prevention Incident Response with Microsoft provides a core framework to import Data Loss Prevention \(DLP\) incidents from multiple sources, such as Microsoft Purview apps, Microsoft Teams, Exchange Online, SharePoint Online, OneDrive for Business, and other event types.

