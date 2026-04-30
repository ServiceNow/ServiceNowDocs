---
title: Grouping domains in Performance Analytics domain configurations
description: Instead of configuring Performance Analytics for the domains of a specific user, create a reusable domain configuration. Select domains that are visible to a group of users, or filter domains directly. Domain configurations let you define hierarchical relationships and aggregate scores across multiple domains.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Domain separation and Performance Analytics, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Grouping domains in Performance Analytics domain configurations

Instead of configuring Performance Analytics for the domains of a specific user, create a reusable domain configuration. Select domains that are visible to a group of users, or filter domains directly. Domain configurations let you define hierarchical relationships and aggregate scores across multiple domains.

**Note:** Performance Analytics domain configurations are enabled with the Performance Analytics – Domain Separation Support plugin. For more information about plugins, see [Activate a Plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Associate these domain configurations with specific data collection jobs and dashboards to provide relevant scores to users. At the same time, maintain your Performance Analytics records, such as indicators, breakdowns, and their sources, in the global domain.

**Important:** Regardless of whether a domain configuration is used, the **Run as** user always determines the domain context of where the data collection Job runs.

Only Performance Analytics administrators with access to all the domains in a configuration can edit a data collection job that has a domain configuration applied to it.

## Required approach

Only the Global approach to Performance Analytics with domain separation supports domain configurations. For more information, see [Approaches to Performance Analytics with domain separation](pa-domain-configurations.md).

## Data tables, process tables, and Run as user

The **Run as** user always determines the domain context of where the data collection Job runs. If you are collecting scores only on data tables such as Incident \[incident\], set an administrator from the global domain as the **Run as** user. This user, and the data collector running under them, has full visibility of all data table records.

A different approach is needed if you are collecting scores on a process domain. It is common practice to define process records such as business rules and SLAs on a process domain. In this case, a **Run as** user who is a global administrator has visibility only to global domain records of these tables. This limitation also impacts scores collected through [database views](performance-analytics-glossary.md#), for example if a join is made to an SLA table like contract\_sla. In such cases, set a user with explicit visibility into the relevant process domains as the **Run as** user.

## Collection, roll-up, and aggregation options

The Domain Configuration record provides flexibility in the way domain records contribute to scores. Prior to the availability of the Domain Support plugin, records in child domains would “roll up” and contribute to the score of a parent domain. The Domain Support plugin provides additional options for how records in child domains should be handled:

-   Select whether to collect scores from individual child domains.
-   Select whether to roll up scores from child domains into the parent domain score. You can roll up child domain scores with or without also collecting the individual scores.
-   If you roll scores from child domains up to the parent domain, select whether to roll up all child domains or only the ones that the domain configuration explicitly includes.
-   Select whether to sum all collected individual domain scores into an aggregate score. This score is stored in a separate domain.

The following table shows the scores that are collected for different configurations with a parent domain and three child customer domains. The table also shows aggregate values.

|Configuration|Parent Domain: MSP| |
|Child domains: Customers|MSP contains customers| |
|A|B|C|MSP|Customers|Aggregate|
|-------------|------------------|---|
|------------------------|----------------------|---|
|---|---|---|---|---------|---------|
|Data|
|New incident records|30|100|50|20|0|-|
|Results|
|No aggregate options|-|-|-|20|-|-|
|No aggregate options + Aggregate|-|-|-|20|-|20|
|Collect Children|30|100|50|20|0|-|
|Collect children + Aggregate|30|100|50|20|0|200|
|Collect Children + Roll up only selected domains \(A and C\)|30|100|50|100|80|-|
|Collect children + Roll up only selected domains \(A and C\) + Aggregate|30|100|50|100|80|200|
|Collect Children + Roll up all child domains|30|100|50|200|180|-|
|Collect Children + Roll up all child domains + Aggregate|30|100|50|200|180|380|
|Roll up only selected domains \(A and C\)|-|-|-|100|-|-|
|Roll up only selected domains \(A and C\) + Aggregate|-|-|-|100|-|100|
|Roll up all child domains|-|-|-|200|-|-|
|Roll up all child domains + Aggregate|-|-|-|200|-|200|

## Domain configuration records

The Performance Analytics – Domain Separation Support plugin adds the Domain Configurations \[pa\_domain\_configurations\] table to your instance. The details of each domain configuration are stored in one of these records.

## Transferring records between instances

Use update sets to transfer domain configurations between instances. If the domain configuration has **Collect aggregate** enabled, also transfer the aggregation domain separately. For more information, see [Transfer domain configuration with score aggregation](../task/transfer-aggregation-domains.md).

-   **[Create a domain configuration](../task/create-domain-configuration.md)**  
Create a domain configuration to define which domains to collect scores from and how to store scores within the domain hierarchy.
-   **[Associate a domain configuration with a data collection job](../task/associate-domain-config-dc-job.md)**  
To collect Performance Analytics indicator scores from the domains specified in a domain configuration, associate that domain configuration with a collection job.
-   **[Associate a domain configuration with a dashboard](../task/associate-domain-config-dashboard.md)**  
Display a domain picker on a dashboard to enable users of that dashboard to view scores from specific domains.
-   **[Transfer domain configuration with score aggregation](../task/transfer-aggregation-domains.md)**  
To transfer between instances a Performance Analytics domain configuration that is set to aggregate scores, transfer both the configuration and the aggregation domain.

**Parent Topic:**[Domain separation and Performance Analytics](c_PAWithDomainSeparation.md)

