---
title: General administration setup for BCM
description: If you are the BCM administrator, you can set up the Business Continuity Management application by performing certain administrative tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/set-up-bcm-bcmadmin-tasks.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# General administration setup for BCM

If you are the BCM administrator, you can set up the Business Continuity Management application by performing certain administrative tasks.

## General Administration module

The administrative tasks that are associated with the BCM application are listed in the **General Administration** module in the application UI as shown in the example.\[Omitted image "gen-admin-module.png"\] Alt text: General Administration module.

The Business Continuity Management administrator with the sn\_bcm.admin role is responsible to perform the administrative tasks that are associated with the Business Continuity Management application.

Business Continuity Management administrators perform these administrative tasks:

-   Configure the impact categories and documentation sections. For more information, see [Configure impact category for BIA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-impact-category-uib-ws.md) and [Configure documentation section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-doc-section-for-bcp.md).
-   Configure the element definitions, element variables, loss scenarios, and impact ratings. For more information, see [Configure element definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-element-definition-bia-uib-ws.md), [Configure element variables for element definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-element-variable-uib-ws.md), [Configure loss scenarios in the plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-plan-loss-scenario-uib-ws.md), and [Configure impact ratings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-impact-rating-uib-ws.md).
-   Configure the recovery tiers and recovery timeframes. For more information, see [Configure recovery tiers for BIA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-recovery-tier-bia-uib-ws.md) and [Set up recovery timeframes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-recovery-timeframe-bia-uib-ws.md).
-   View the My tasks page configurations module, approval configurations, and properties. For more information, see [My tasks page configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/my-tasks-page-config-module.md), [Approval configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-approval-configuration.md), and [BCM properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-properties-module.md).
-   For more information on the grid configurations and categories, see [Configure grid for BIA assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-grid-configuration-uib-ws.md) and [Configure grid categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-grid-category.md).

## Custom queue for the Update dependencies process

Previously, Update dependencies events were added to the platform default queue, which is shared across all ServiceNow applications. During periods of high activity, this could result in delays in processing BCM dependency updates — either because other applications saturated the queue, or because a long-running BCM process affected other items in it.

With the Australia release and later, the Update dependencies process uses a dedicated custom queue \(bcm\_dependencies\) instead of the platform default queue. This is a backend change with no visible indicator in the UI.

The dedicated queue ensures that Update dependencies events have their own processor and do not compete with or block other platform activity.

If you previously configured a custom queue for BCM dependency processing on your instance, remove it — BCM now provides this configuration natively.

For more information about custom queues and the event registry, see [System Events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/system-events/events.md) and [Event registry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/r_EventRegistry.md).

This change applies to the Australia release and later.

## BIA Configuration module

The BCM administrator configures the BIA templates in the BIA Configuration module. Configuring the BIA templates is a pre-requisite for performing the business impact analysis.

The **BIA templates** menu option in the BIA Configuration module is shown in the example.\[Omitted image "bia-config-module.png"\] Alt text: BIA Configuration module.

For more information on configuring a BIA template, see [Configure BIA templates with legacy assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-bia-template-uib-ws.md).

## Plan Templates module

The Business Continuity Management administrator uses the **Plan Templates** module to configure a business continuity plan template. The **Plan Templates** module is shown in the example.\[Omitted image "plan-templates-module.png"\] Alt text: Plan Templates module.

For more information on configuring a business continuity plan template, see [Configuring plan template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-admin-plan-templates.md).

-   **[Dependency Configuration records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/dependency-config-modules.md)**  
The BCM administrators configure the Dependency Configuration records.
-   **[Configure impact category for BIA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-impact-category-uib-ws.md)**  
Configure an impact category for your business, when you are performing the business impact analysis. Use the **Impact Categories** module in the Business Continuity Management application navigator to define the name, criteria that the impact category contributes to, applicable timeframes, maximum RTO value, and so on.
-   **[Configuring the documentation section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-admin-documentation-sections.md)**  
You can configure the documentation section of a business continuity plan in a structured format. You can describe high level details of the plan such as its purpose, scope, coverage areas, goals, and success criteria.
-   **[Configure element definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-element-definition-bia-uib-ws.md)**  
Configure element definitions to identify the configuration item that has to be assessed in a business impact analysis and recovered in a business continuity plan. Use the **Element Definitions** module in the Business Continuity Management application navigator to configure an element definition.
-   **[Configure element variables for element definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-element-variable-uib-ws.md)**  
Configure an element variable for a specific dependency of an element. To do this, use the **Element variables** module in the Business Continuity Management application navigator.
-   **[Configure loss scenarios in the plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-plan-loss-scenario-uib-ws.md)**  
Configure a plan for an identified loss scenario by using the loss scenario template in the Business Continuity Management application. Use the documented plan that has the needs and requirements listed for a potential disaster.
-   **[Configure impact ratings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-impact-rating-uib-ws.md)**  
Configure an impact rating to assess an impact category as low, moderate, high, or critical. Use the **Impact Ratings** module in the Business Continuity Management application navigator to help you measure the intensity of the loss when a business downtime occurs.
-   **[Configure recovery tiers for BIA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-recovery-tier-bia-uib-ws.md)**  
Configure a recovery tier with a set of business applications that follow a similar range of recovery time objective \(RTO\) values. Use the **Recovery Tiers** module in the Business Continuity Management application navigator to configure a recovery tier.
-   **[Set up recovery timeframes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-recovery-timeframe-bia-uib-ws.md)**  
Set up a recovery timeframe for a recovery tier. The recovery timeframe starts from when a disruptive event happens to the time when your business can resume usual operations. You can use the **Recovery Timeframes** module in the Business Continuity Management application to set up the timeline for the recovery timeframe.
-   **[Configure grid categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-grid-category.md)**  
Configure a grid category such as Dependency Assessment for the grid configuration. Use the **Grid Categories** module in the Business Continuity Management application navigator to configure the grid categories.
-   **[Configure grid for BIA assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configure-grid-configuration-uib-ws.md)**  
Configure the grid to render the BIA dependency assessment grid with configured columns. Use the **Grid Configurations** module in the Business Continuity Management application navigator to configure the grid.
-   **[My tasks page configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/my-tasks-page-config-module.md)**  
If you are the Business Continuity Management application user, you can use **My tasks page configurations** in the **General Administration** module to view your assigned tasks.
-   **[Approval configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-approval-configuration.md)**  
Approver configurator provides you with capabilities to define multiple levels of approvals based on business rule definitions.
-   **[BCM properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-properties-module.md)**  
You can configure the BCM properties in the **Properties** module.
-   **[Properties installed with BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/properties-bcm.md)**  
Properties are added with the activation of Business Continuity Management.

**Parent Topic:**[Configuring Business Continuity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configuring-business-continuity-management.md)

