---
title: Knowledge Management Platform Analytics Solutions
description: Platform Analytics Solutions contain preconfigured dashboards. These dashboards contain actionable data visualizations that help you improve your business processes and practices.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Analytics and Reporting Solutions for Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge Management Platform Analytics Solutions

Platform Analytics Solutions contain preconfigured dashboards. These dashboards contain actionable data visualizations that help you improve your business processes and practices.

## Platform Analytics Solutions

Platform Analytics data visualizations use Performance Analytics [indicator](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=xanadu&pubname=xanadu-glossary&section=gloss-indicator&ft:locale=en-US) data to show you data over time, helping you analyze your business processes and identify areas of improvement. With Platform Analytics Solutions, you can get value from Performance Analytics for your application with minimal setup. You can always create your own objects as well.

**Important:** Set up and test Platform Analytics Solutions on a non-production instance before enabling them in production.

To enable the solution for Knowledge Management, an admin can navigate to **Performance Analytics** &gt; **Guided Setup**. Click **Get Started** then scroll to the section for Knowledge Management. The guided setup takes you through the entire setup and configuration process.

**Note:** You must [Activate the Knowledge Management Advanced plugin](../../../product/knowledge-management/task/activate-knowledge-advanced-plugin.md).

## Domain separation and 'Run As' user

In some solutions, System Administrator is the **Run As** user for data collection jobs in the Platform Analytics Solutions. In other solutions, the **Run As** user for data collection jobs is left blank. Verify that the **Run As** user exists on the instance, and that this user has the appropriate level of access. An inappropriate **Run As** user can cause errors or limit the data that is collected. This setting only has an effect if domain separation is enabled.

## New and deprecated versions of this solution

In London , this Solution was replaced with a new version, `com.snc.pa.knowledge_v2`. If you activated an earlier version of the Solution and then upgraded your instance, you still have and can still use the earlier Solution. You can also activate the newer version without losing data from existing indicators and breakdowns. If you activate the newer version, run a historical data collection job to populate any new indicators and breakdowns.

## Add Self-Service Analytics to Knowledge Management dashboards

If you have Self-Service Analytics activated on an instance, you can add Self-Service analytics widgets to your Performance Analytics dashboards or a Service Portal. To obtain a ready-made set of indicators and breakdowns, activate the Self-Service Analytics PA \(**com.snc.pa.self\_service\_analytics**\) plugin. Find the Self-Service indicators through the Performance Analytics Admin Console, then create widgets and add them to your dashboard or portal. Also activate the \[SSA\] Self-Service Analytics data collection job.

-   **[Knowledge Management dashboard](knowledge-management-dashboard.md)**  
The Knowledge Management dashboard helps knowledge content owners and managers to determine the usage and quality of their knowledge content. It helps confirm that the proper processes and procedures are being followed for content creation.

**Parent Topic:**[Analytics and Reporting Solutions for Knowledge Management](../../../product/knowledge-management/concept/analytics-and-reporting-solutions-for-knowlege-management.md)

**Related topics**  


[Platform Analytics Solutions](https://www.servicenow.com/docs/access?context=content-packs-in-form-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

[Activate your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)

