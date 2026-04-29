---
title: Data Loss Prevention Incident Response Integration with Proofpoint
description: The Proofpoint DLP integration supports the ingestion of Data Loss Prevention incidents created on the Proofpoint Data Loss Prevention deployment. After ingestion, you can use the incident management functionalities to remediate the DLP incidents.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Data Loss Prevention Incident Response Integration with Proofpoint

The Proofpoint DLP integration supports the ingestion of Data Loss Prevention incidents created on the Proofpoint Data Loss Prevention deployment. After ingestion, you can use the incident management functionalities to remediate the DLP incidents.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Overview and key features

The Proofpoint DLP integration helps companies to track the usage and movement of sensitive data on various platforms.

This integration includes the following key features:

-   Multiple profile creation for different Proofpoint endpoints.
-   Automating the creation of DLP incidents.
-   Mapping of the Proofpoint DLP incident state field to DLP incident state field.
-   Filtering of Proofpoint DLP incidents.
-   Ingestion of incidents in your ServiceNow instance as soon as the incidents are created on Proofpoint DLP tenant.
-   Proofpoint DLP integration supports both endpoints and email type of incidents.
-   Automatic updates for the Proofpoint DLP incident status and comments for DLP incident creation, and for state change and closure on ServiceNow side.

## Learn about this integration

|Document identifier|Document title|
|-------------------|--------------|
|Proofpoint product documentation website|[Proofpoint product documentation](https://help.proofpoint.com/)|
|ServiceNow® product documentation website|[ServiceNow Product Documentation website](https://servicenow.com/docs)|

-   **[Getting started with Proofpoint integration for Data Loss Prevention](../reference/getting-started-with-proofpoint-integration-dlp.md)**  
The Proofpoint DLP integration supports the ingestion of Data Loss Prevention incidents created on the Proofpoint Data Loss Prevention tenant. After ingestion, the incident management functionalities that remediate the DLP incidents will be used.
-   **[Install and configure the Proofpoint integration for Data Loss Prevention](../task/install-configure-proofpoint-integration-dlp.md)**  
Install and configure the  Proofpoint DLP integration from the  ServiceNow® Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  Proofpoint DLP incident data.
-   **[Create an Application in Proofpoint and Obtain Client Credentials](../task/create-application-proofpoint-dlp.md)**  
Create an Application in Proofpoint and configure the required settings to obtain client credentials. These credentials enable secure access to Proofpoint's API for seamless integration and automation.
-   **[Create a Profile for Proofpoint DLP integration](../task/create-profile-proofpoint-dlp-integration.md)**  
Create an incident profile in your  ServiceNow AI Platform instance. Determine the  Proofpoint DLP incidents that are suitable for creating DLP incidents.
-   **[Map Proofpoint DLP incidents status with ServiceNow incident status](../task/map-proofpoint-dlp-incident-status.md)**  
Synchronize the status of the DLP incidents ingested on your ServiceNow instance and DLP incidents of the Proofpoint. Map the ServiceNow Incident status with the Proofpoint Incident status.
-   **[Configure Proofpoint DLP integration settings](../task/configure-proofpoint-dlp-integration-settings.md)**  
Modify the  Proofpoint DLP  integration default system properties.
-   **[Domain Separation in Proofpoint DLP integration](domain-separation-proofpoint-dlp-integration.md)**  
Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[DLP integrations](../../data-loss-prevention/concept/dlp-integrations.md)

**Related topics**  


[Symantec Integration for Data Loss Prevention Incident Response](../../dlp-symantec/concept/symantec-dlp-integration.md)

[Data Loss Prevention Incident Response Integration with Netskope](../../dlp-netskope/concept/dlp-incident-response-integration-netskope.md)

[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](../../dlp-icap-zscaler/concept/icap-dlp-integration.md)

[Data Loss Prevention Incident Response with Microsoft](../../dlp-microsoft/concept/dlp-integration-microsoft.md)

