---
title: Symantec Integration for Data Loss Prevention Incident Response
description: The Symantec DLP integration supports the ingestion of Data Loss Prevention Incident Response incidents created on the Symantec Data Loss Prevention Incident Response deployment. After ingestion, you can use the incident management functionalities to remediate the DLP incidents.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Symantec Integration for Data Loss Prevention Incident Response

The Symantec DLP integration supports the ingestion of Data Loss Prevention Incident Response incidents created on the Symantec Data Loss Prevention Incident Response deployment. After ingestion, you can use the incident management functionalities to remediate the DLP incidents.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Overview and key features

The Symantec DLP integration helps companies to track the usage and movement of sensitive data on various platforms.

This integration includes the following key features:

-   Ability to create multiple integration profiles for different Symantec API endpoints.
-   Scheduled ingestion of DLP incidents from Symantec into your ServiceNow instance.
-   Ability to apply API filters to retrieve the incidents that match the filter criteria and also specify the filter for Symantec DLP incidents that are required to be imported.
-   Mapping the DLP incident states in your ServiceNow instance to DLP incident states in Symantec.
-   Automatically update incident status in Symantec when the state changes in your ServiceNow instance.
-   Ability to customize and define the severity mapping between Symantec DLP incidents with ServiceNow incidents.

To learn more about the integration, see the [Symantec product documentation](https://techdocs.broadcom.com).

-   **[Getting started with Symantec DLP integration for Data Loss Prevention](getting-started-symantec-dlp-integration-dlp.md)**  
Before you can use the integration, you must download it from the ServiceNow® Store.
-   **[Install and configure the Symantec DLP integration for Data Loss Prevention](../task/install-configure-symantec-dlp-integration.md)**  
Install and configure the  Symantec DLP integration from the  ServiceNow® Store on your  ServiceNow AI Platform instance. Start investigating DLP incidents using the  Symantec DLP incident data.
-   **[Create a profile for Symantec DLP integration](../task/create-profile-symantec-dlp.md)**  
Create an incident profile in your  ServiceNow AI Platform instance. Determine the  Symantec DLP incidents that are suitable for creating DLP incidents.
-   **[Severity mapping between Symantec DLP incidents with ServiceNow incidents](../task/severity-mapping.md)**  
Use the severity mapping feature to configure and synchronize the mapping between Symantec incidents and ServiceNow AI Platform® incidents.
-   **[Configure Smart Response Rules](../task/config-smart-response-rules.md)**  
Configure the Symantec smart response rule\(s\) to perform response actions on the ingested Symantec DLP Incidents.
-   **[Execute Smart Response Rules](../task/execute-smart-response-rules.md)**  
Use this feature to execute Smart Response Rules for the Symantec DLP incidents.
-   **[Configure the Symantec DLP  integration settings](../task/modify-symantec-dlp-system-properties.md)**  
Modify the  Symantec DLP  integration default system properties.
-   **[Domain Separation in the Symantec DLP integration](domain-seperation-symantec-dlp-integration.md)**  
Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[DLP integrations](../../data-loss-prevention/concept/dlp-integrations.md)

**Related topics**  


[Data Loss Prevention Incident Response Integration with Proofpoint](../../dlp-proofpoint/concept/dlp-incident-response-integration-proofpoint.md)

[Data Loss Prevention Incident Response Integration with Netskope](../../dlp-netskope/concept/dlp-incident-response-integration-netskope.md)

[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](../../dlp-icap-zscaler/concept/icap-dlp-integration.md)

[Data Loss Prevention Incident Response with Microsoft](../../dlp-microsoft/concept/dlp-integration-microsoft.md)

