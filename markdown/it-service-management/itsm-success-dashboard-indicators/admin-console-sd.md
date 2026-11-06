---
title: ITSM Success Dashboard Admin console
description: The ITSM Success Dashboard offers valuable insights to both the leadership team and process owners, enabling them to assess the performance of their product implementation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-success-dashboard-indicators/admin-console-sd.html
release: australia
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure, ITSM Success Dashboard indicators, IT Service Management]
---

# ITSM Success Dashboard Admin console

The ITSM Success Dashboard offers valuable insights to both the leadership team and process owners, enabling them to assess the performance of their product implementation.

The performance is assessed by using the established key performance indicators \(KPIs\). This process categorizes configuration activities and provides information in each category such as planning guidance, pre-setup steps, and links to useful help content.

## Prerequisites

-   User roles: You can assign different roles based on specific access requirements. For more information on the ITSM Success Dashboard roles, see [Success Dashboard indicators user roles and responsibilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-success-dashboard-indicators/success-roles.md)
-   Review and configure self-service KPIs: You can review and configure the self-service KPIs for Knowledge deflection, Virtual Agent deflection, and Catalog Item fulfillment level.
-   Performance Analytics jobs: Activate Performance Analytics jobs to collect daily and historical data for the ITSM Success Dashboard indicators.
-   Process Mining projects: Review and Configure the process mining KPIs.

## Advanced options

Configure the ITSM Success Dashboard KPIs and its related attributes from the advanced options.

-   System properties: Configure and manage the behavior of the features for the ITSM Success Dashboard.
-   Attribute cost savings to contributing indicators: Review the time savings and the persona group association to contributing indicators based on your organization.
-   Key performance indicators \(KPIs\): Enable the ITSM Success Dashboard and configure settings to understand and use the KPIs and formulas.
-   Contributing indicators: Modify the base system contributing indicators associated with the primary indicators, or add additional contributing indicators based on your implementation.
-   Contextual help content: Add or modify the contextual help content to be displayed for the primary or contributing indicators.

-   **[Set the refresh interval for Success Dashboard indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-success-dashboard-indicators/configure-knowledge-deflection.md)**  
Set the refresh interval for calculating incidents deflected when users read knowledge articles recommended by Virtual Agent.
-   **[Configure Virtual Agent topics for ITSM Success Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-success-dashboard-indicators/configure-va.md)**  
Measure Virtual Agent usage in ITSM Success Dashboard indicators with deflection nodes or self-service analytics, including for topics other than base system topics.
-   **[Update the live agent script include](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-success-dashboard-indicators/update-live-agent-script-include.md)**  
Live agent configuration is used in the self-solved deflections \(Deflection using KB articles, Deflection using QnA AIS, Deflection using QnA LLM, and Deflection using ITSM VA\). When you configure these deflections, update the live agent script include. Update the SSADeflectionHelper script to override the *checkInteraction* function.
-   **[Set fulfillment automation level of catalog item for the Success Dashboard indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-success-dashboard-indicators/set-fulfillment-automation-level-sdb.md)**  
Set the fulfillment automation level of catalog items from manual to fully automated to reduce manual effort and accelerate the turnaround time.
-   **[Activate Performance Analytics jobs for ITSM Success Dashboard indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-success-dashboard-indicators/activae-pa-indicator-jobs-sdb.md)**  
Activate the Performance Analytics \(PA\) jobs to collect daily and historical data for the ITSM Success Dashboard indicators.
-   **[KPI configuration for Success Dashboard indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-success-dashboard-indicators/config-kpis-sdb.md)**  
Reconfigure the source of KPIs in Success Dashboard indicators by replacing or adding indicators in the base system.

**Parent Topic:**[Configuring ITSM Success Dashboard indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-success-dashboard-indicators/configure-success-dashboards.md)

