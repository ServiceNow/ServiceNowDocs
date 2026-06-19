---
title: Configure Performance Analytics advanced features
description: Define key metrics and data structure to generate scores.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/performance-analytics/c\_PADataArchitecture.html
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Configure Performance Analytics advanced features

Define key metrics and data structure to generate scores.

The topics in this section are meant primarily for Performance Analytics administrators who deal directly with data structures.

-   **[Activating your Performance Analytics subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_PremiumPerformanceAnalytics.md)**  
Without a paid Performance Analytics subscription, your use is limited to 180 days of data collection \(five months for monthly indicators\) and to specific indicators provided by ServiceNow, and you cannot activate Data snapshots. For unlimited access to all features, purchase a subscription to Performance Analytics.
-   **[Performance Analytics Admin Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/pa-admin-console.md)**  
From a single console, administrators can manage Platform Analytics Solution content, manage Performance Analytics widgets and dashboards, diagnose and resolve errors, view usage analytics, modify configuration settings and access ServiceNow help.
-   **[Collecting indicator scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_ClctData.md)**  
Performance Analytics uses data collection jobs to collect and clean scores and snapshots. You can also set indicator scores manually.
-   **[Ranking records with Spotlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/spotlight/spotlight.md)**  
Use Spotlight to identify and rank records of interest based on multiple weighted criteria.
-   **[Data collection process and logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/data-collection-process-logging.md)**  
Performance Analytics data collection jobs collect indicator scores. To debug data collection, it is helpful to understand the data collection process and how it is reflected in the job logs.
-   **[Performance Analytics diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/self-diagnostics.md)**  
Identify and diagnose configuration issues using predefined scripts that examine the database for invalid records and provide suggestions to resolve issues.
-   **[\(Legacy\) Dependency Assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/impact-analysis.md)**  
Dependency Assessment enables you to view, analyze, and edit your performance analytics components including widgets, indicators, and breakdowns, from a single view. By viewing the hierarchy of components and the relationships between them, you can see immediately who is impacted by a change and what the effects of your changes are.
-   **[Domain separation and Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_PAWithDomainSeparation.md)**  
Domain separation is supported for Performance Analytics. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data. Performance Analytics supports collecting scores from multiple domains and can be configured to enable domain-specific administration. Extended domain configuration functionality is available for customers with complex domains.
-   **[Integrate Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_PAWebServiceIntegrations.md)**  
Integrate Performance Analytics with an external system to collect scores based on remote data or to expose Analytics Hub information.
-   **[Scripting in Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/pa-scripts.md)**  
Performance Analytics provides several script objects for use in scripts and APIs for querying Performance Analytics data. The scripts serve as breakdown mappings or to calculate a value from an indicator.
-   **[Using Performance Analytics with external data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/pa-external-data.md)**  
Performance Analytics on external data sources enables you to perform detailed analysis on data that is not in your ServiceNow instance.
-   **[Cleaning collected Performance Analytics data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_CollectionCleanup.md)**  
Performance Analytics scores and snapshots may grow over time and should be routinely cleaned to ensure optimal performance and accurate data.
-   **[Migrating indicator scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/pa-scores-migration.md)**  
The Performance Analytics Scores \[pa\_scores\] table was split into two tables. This structure helps with processing large numbers of scores. You can migrate your scores from the old table structure to the new, using the score migration tool.

**Parent Topic:**[Performance Analytics \(Indicator data sources\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown)

