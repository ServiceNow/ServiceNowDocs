---
title: ITSM Success Dashboard Admin console
description: The ITSM Success Dashboard offers valuable insights to both the leadership team and process owners, enabling them to assess the performance of their product implementation.
locale: en-US
release: xanadu
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring ITSM Success Dashboard indicators, ITSM Success Dashboard indicators, IT Service Management]
---

# ITSM Success Dashboard Admin console

The ITSM Success Dashboard offers valuable insights to both the leadership team and process owners, enabling them to assess the performance of their product implementation.

The performance is assessed by utilizing the established key performance indicators \(KPIs\). This process categorizes configuration activities and provides information in each category such as planning guidance, pre-setup steps, and links to useful help content.

ITSM Success Dashboard Admin Console Overview 

## Prerequisites

-   User Roles: You can assign different roles based on specific access requirements. For more information on the ITSM Success Dashboard roles, see [Success Dashboard indicators user roles and responsibilities](success-roles.md)
-   Review and configure self-service KPIs: You can review and configure the self-service KPIs for Knowledge deflection, Virtual Agent deflection, and Catalog Item fulfillment level.
-   Performance Analytics jobs: Activate Performance Analytics jobs to collect daily and historical data for the ITSM Success Dashboard indicators.
-   Process Mining projects: Review and Configure the process mining KPIs.

## Advanced Options

Configure the ITSM Success Dashboard KPIs and its related attributes from the advanced options.

-   System properties: Configure and manage the behavior of the features for the ITSM Success Dashboard.
-   Attribute cost savings to contributing indicators: Review the time savings and the persona group association to contributing indicators based on your organization.
-   Key performance indicators \(KPIs\): Enable the ITSM Success Dashboard and configure settings to understand and use the KPIs and formulas.
-   Contributing indicators: Modify the base system contributing indicators associated with the primary indicators, or add additional contributing indicators based on your implementation.
-   Contextual Help content: Add or modify the contextual help content to be displayed for the primary or contributing indicators.

-   **[Set the refresh interval for Success Dashboard indicators](../task/configure-knowledge-deflection.md)**  
Set the refresh interval to calculate the number of incidents deflected within the defined time range when a user reads the KB article recommended by the Virtual Agent.
-   **[Configure Virtual Agent topics for ITSM Success Dashboard](configure-va.md)**  
Configure the Virtual Agent \(VA\) topics for ITSM Success Dashboard indicators so that data is displayed correctly if you have topics other than the base system topics.
-   **[Update the live agent script include](../task/update-live-agent-script-include.md)**  
Live agent configuration is used in the self-solved deflections \(Deflection using KB articles, Deflection using QnA AIS, Deflection using QnA LLM, and Deflection using ITSM VA\). While we configure these deflections, we need to update the live agent script include. Update the SSADeflectionHelper script to override the *checkInteraction* function.
-   **[Set fulfillment automation level of catalog item for the Success Dashboard indicators](../task/set-fulfillment-automation-level-sdb.md)**  
Set the fulfillment automation level of catalog items from any Service group that are fulfilled without any manual intervention to Fully-automated tracking of the requested items with an end-to-end automated fulfilment.
-   **[Activate Performance Analytics jobs for ITSM Success Dashboard indicators](../task/activae-pa-indicator-jobs-sdb.md)**  
Activate the Performance Analytics \(PA\) jobs to collect daily and historical data for the ITSM Success Dashboard indicators.
-   **[Configure Success Dashboard indicators KPIs](../task/config-kpis-sdb.md)**  
Success Dashboard indicators has a prescriptive methodology for measuring performance. But you can reconfigure the source of the Key Performance Indicators \(KPIs\) by replacing the available indicators in the base system or by adding more indicators.

**Parent Topic:**[Configuring ITSM Success Dashboard indicators](configure-success-dashboards.md)

