---
title: Data Loss Prevention Incident Response Integration with Netskope
description: The Netskope DLP integration supports the ingestion of Data Loss Prevention incidents created on the Netskope Data Loss Prevention deployment. Netskope DLP helps companies to track the usage and movement of sensitive data on various platforms.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Data Loss Prevention Incident Response Integration with Netskope

The Netskope DLP integration supports the ingestion of Data Loss Prevention incidents created on the Netskope Data Loss Prevention deployment. Netskope DLP helps companies to track the usage and movement of sensitive data on various platforms.

After ingestion, you can use the incident management functionalities to remediate the DLP incidents.

## Key features

This integration includes the following key features:

-   Multiple profile creation for different Netskope tenants.
-   Automating the creation of ServiceNow DLP incidents from Netskope DLP incidents.
-   Filtering of Netskope DLP incidents.
-   Scheduled ingestion of Netskope DLP incidents that create DLP incidents in ServiceNow.
-   Automatically update object status on Netskope when the DLP state changes in your ServiceNow instance.
-   View the forensic details \(violating content\) of the DLP Incident on DLP IR Analyst workspace and DLP End user workspace.

    **Note:** The violating content doesn’t persist in ServiceNow. The content is pulled when the incident is in opened in the workspace.

-   Downloading evidence file directly from Netskope on demand.

    **Note:** The evidence file doesn’t persist in ServiceNow. The evidence file is pulled when the analyst click on the **Download File** in the workspace.

-   Notification via email to DLP Admin users on Netskope token expiration.
-   Notification via email is sent to DLP Admin users if it exceeds the defined retry limit for incident API call failures.
-   Netskope also supports integration run process. For more information, see [Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md).

-   **[Getting started with Netskope DLP integration for Data Loss Prevention](../reference/getting-started-netskope-dlp-integration.md)**  
Review the following information before you start setting up your Netskope DLP integration for Data Loss Prevention.
-   **[Install and configure the Netskope DLP integration for Data Loss Prevention](../task/install-configure-netskope-dlp-integration.md)**  
Install and configure the Netskope DLP integration from   ServiceNow Store   ServiceNow AI Platform instance. You can start investigating DLP incidents using the  Netskope DLP incident data.
-   **[Create a Profile for Netskope DLP integration](../task/create-profile-netskope-dlp-integration.md)**  
Create an incident profile in your ServiceNow AI Platform instance.
-   **[Mapping DLP incident status with Netskope](../task/map-incident-status.md)**  
The incident status mapping section enables the users to provide the mappings between the DLP Incident status in ServiceNow and Netskope Object status.
-   **[Configure Netskope DLP integration settings](../task/configure-netskope-dlp-integration-settings.md)**  
Modify the  Netskope DLP  integration default system properties.
-   **[Download evidence files](../task/download-files-netskope.md)**  
Download files that violate the DLP policy on Netskope. Download this file onto your local machine from the DLP IR Analyst workspace and DLP IR End user workspace for approvers.
-   **[Preview evidence files](../task/preview-files-netskope.md)**  
Preview DLP incident evidence files in the DLP IR Analyst workspace.
-   **[Notifications for users on retry mechanism](notifications-retry-limit.md)**  
Netskope integration will retry the configured number of times in case of API failures during DLP Incident ingestion.
-   **[Email notifications on credential expiration](../task/notification-users-credential-expiration.md)**  
When the token used in the ServiceNow instance expires, Netskope integration sends out an email notification to users with the DLP Admin \(sn\_dlir.admin\) role.
-   **[Domain Separation in Netskope DLP integration](domain-separation-netskope-dlp-integration.md)**  
Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[DLP integrations](../../data-loss-prevention/concept/dlp-integrations.md)

**Related topics**  


[Symantec Integration for Data Loss Prevention Incident Response](../../dlp-symantec/concept/symantec-dlp-integration.md)

[Data Loss Prevention Incident Response Integration with Proofpoint](../../dlp-proofpoint/concept/dlp-incident-response-integration-proofpoint.md)

[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](../../dlp-icap-zscaler/concept/icap-dlp-integration.md)

[Data Loss Prevention Incident Response with Microsoft](../../dlp-microsoft/concept/dlp-integration-microsoft.md)

