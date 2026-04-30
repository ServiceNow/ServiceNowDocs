---
title: Data Loss Prevention Incident Response with Microsoft
description: The Data Loss Prevention Incident Response with Microsoft provides a core framework to import Data Loss Prevention \(DLP\) incidents from multiple sources, such as Microsoft Purview apps, Microsoft Teams, Exchange Online, SharePoint Online, OneDrive for Business, and other event types.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Data Loss Prevention Incident Response with Microsoft

The Data Loss Prevention Incident Response with Microsoft provides a core framework to import Data Loss Prevention \(DLP\) incidents from multiple sources, such as Microsoft Purview apps, Microsoft Teams, Exchange Online, SharePoint Online, OneDrive for Business, and other event types.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Overview and key features

The Data Loss Prevention Incident Response integration with Microsoft enables organizations to gain a unified view of incidents across email, network, endpoint, and cloud sources. Endpoint devices enable remediation workflow involving end users, managers, and  DLP  operations team with automated incident assignment and escalations.

Use the key features of this integration to do the following actions:

-   Create multiple profiles for different accounts.
-   Automate the creation of DLP IR incidents.
-   Map the Microsoft DLP IR event fields to DLP IR incident fields.
-   Filter Microsoft DLP IR events.
-   Schedule the ingestion of DLP IR events that create DLP IR incidents periodically.
-   Store the matching content of each Microsoft DLP event in external cloud storage.
-   Delete matching content at external cloud storage on the deletion of the DLP IR incident in ServiceNow.
-   Download files for DLP IR incidents of type Exchange, OneDrive, and SharePoint.
-   Store evidence files for DLP IR incidents of type Exchange, OneDrive and SharePoint in the internal ServiceNow storage.

## Learn about this integration

|Document identifier|Document title|
|-------------------|--------------|
|Microsoft product documentation website|[Microsoft Product Documentation website](https://learn.microsoft.com/en-us/microsoft-365/compliance/dlp-learn-about-dlp)|
|ServiceNow product documentation website|[ServiceNow Product Documentation website](https://servicenow.com/docs)|

-   **[Getting started with Microsoft DLP IR integration for data loss prevention](../reference/getting-started-microsoft-integration.md)**  
Review the following information before you start setting up your Microsoft DLP IR integration for data loss prevention.
-   **[Install and configure the Microsoft DLP integration](../task/install-configure-microsoft-dlp-integration.md)**  
Install and configure the  DLP Incident Response integration with Microsoft DLP from the  ServiceNow® Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  Microsoft DLP event data.
-   **[Create a new incident profile for Microsoft DLP integration](../task/create-profile-microsoft-dlp-integration.md)**  
Create an incident profile in your  ServiceNow AI Platform instance to retrieve the data from the Microsoft Purview and add the data into the ServiceNow DLP IR incident table.
-   **[Configure Microsoft DLP IR integration settings](../task/configure-microsoft-integration-settings.md)**  
Modify the  Microsoft DLP IR  integration default system properties.
-   **[Configure evidence file storage for Microsoft](../task/dlp-config-file-storage-msft.md)**  
Configure evidence file storage to securely store the evidence file in the ServiceNow instance for the Microsoft incidents of type OneDrive, Exchange and SharePoint.
-   **[Request release email from quarantine](../task/request-email-from-quarantine.md)**  
Use this feature to release the email that is quarantined from the Microsoft Purview compliance portal.
-   **[Download files for DLP incidents of type Exchange Online, OneDrive, and SharePoint](../task/download-file-dlp-microsoft.md)**  
Download files or email that violates the DLP policy on Microsoft Purview. Download this file or email on to your local machine from the DLP IR Incident view. You can download the files for DLP IR incidents of type Scan source Exchange Online, OneDrive, and SharePoint.
-   **[Preview Evidence files for DLP incidents of type Exchange Online, OneDrive, and SharePoint](../task/preview-file-dlp-microsoft.md)**  
Preview Data Loss Prevention Incident Response evidence files in the DLP IR Analyst workspace.
-   **[Domain separation in Microsoft DLP integration](domain-separation-microsoft-dlp.md)**  
Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[DLP integrations](../../data-loss-prevention/concept/dlp-integrations.md)

**Related topics**  


[Symantec Integration for Data Loss Prevention Incident Response](../../dlp-symantec/concept/symantec-dlp-integration.md)

[Data Loss Prevention Incident Response Integration with Proofpoint](../../dlp-proofpoint/concept/dlp-incident-response-integration-proofpoint.md)

[Data Loss Prevention Incident Response Integration with Netskope](../../dlp-netskope/concept/dlp-incident-response-integration-netskope.md)

[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](../../dlp-icap-zscaler/concept/icap-dlp-integration.md)

