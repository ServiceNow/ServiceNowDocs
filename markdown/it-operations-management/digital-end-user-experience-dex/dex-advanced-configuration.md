---
title: DEX advanced configuration
description: Advanced configuration options for DEX cover agent proxy and connection settings, agent and application source conversion, sudo banner validation, device user mapping, and location determination. You can use these options to fine-tune system behavior for specific organizational requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/dex-advanced-configuration.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [dex advanced configuration, advanced configuration options, customize dex settings, fine-tune dex performance, optimize dex performance, dex performance tuning, organizational configuration requirements]
breadcrumb: [Configure, Digital End-User Experience, IT Operations Management]
---

# DEX advanced configuration

Advanced configuration options for DEX cover agent proxy and connection settings, agent and application source conversion, sudo banner validation, device user mapping, and location determination. You can use these options to fine-tune system behavior for specific organizational requirements.

-   **[Configure ACC to use a proxy for all traffic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/configure-acc-to-use-proxy.md)**  
Configure the Agent Client Collector \(ACC\) to use a proxy for all traffic by setting environment variables.
-   **[Switch ACC from one instance to another](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/convert-agent-instance.md)**  
Switch Agent Client Collector \(ACC\) to a different instance.
-   **[Configure MID-less Agent Client Collector using a single-line command]()**  
Use a single-line command to set up a MID-less Agent Client Collector. You can also use the single-line command to migrate agents configured with a MID Server to have a MID-less configuration.
-   **[Convert MID-based ACC to MID-less](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/convert-midbased-acc.md)**  
Convert MID-based Agent Client Collector \(ACC\) to MID-less ACC by adjusting the configuration in the acc.yml file so that ACC doesn't depend on a specific MID Server.
-   **[Convert an application source to DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/convert-app-source-to-dex.md)**  
Convert a Visibility Content application to DEX monitoring. After conversion, the application is managed in the Application and Device Health system.
-   **[Sudo banner validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/sudo-banner-validation.md)**  
Sudo banner validation flags missing sudo permissions on managed devices so you know when the DEX agent's capabilities are limited.
-   **[Map a device user to a ServiceNow DEX user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/map-a-device-user-to-a-servicenow-dex-user.md)**  
Map a device user to a DEX user so you can notify the user when device metrics breach a predetermined threshold.
-   **[Device location determination](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/location-determination.md)**  
Device location determination identifies the number of impacted devices at each location based on configurable logic.

**Parent Topic:**[Configuring Digital End-User Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/configure-dex-cf.md)

