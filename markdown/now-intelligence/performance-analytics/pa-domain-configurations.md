---
title: Approaches to Performance Analytics with domain separation
description: When using Performance Analytics with domain separation, you can collect domain-specific scores. You can use global or domain-specific Performance Analytics table records or even a combination of both.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Domain separation, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Approaches to Performance Analytics with domain separation

When using Performance Analytics with domain separation, you can collect domain-specific scores. You can use global or domain-specific Performance Analytics table records or even a combination of both.

## Global approach and collecting domain-specific scores

You can keep all Performance Analytics records, such as indicators, breakdowns, and widgets, in the Global domain. In this case, you apply domain separation through domain-specific [data collection jobs](performance-analytics-glossary.md#).

To configure a data collection job to be domain-specific, add a **Run as** user to the job. The **Run as** user determines the domain context of where the data collection job runs. For more information, see [Create or schedule a data collection job](../task/t_CreatASchedDataCollJob.md).

You can also specify a domain configuration. Domain configurations are part of the Performance Analytics plugin for domain support, intended to help with complex domain management. For more information, see [Associate a domain configuration with a data collection job](../task/associate-domain-config-dc-job.md).

The data collection job collects scores against facts table records in the Global domain. The job also collects scores against records in the domains of the **Run as** user. The job stores the scores in the domain it collected them from. In data visualizations, a user sees only scores from domains they have visibility into.

If you specify only a **Run as** user, scores from all child domains are rolled up to the parent. If you also specify a domain configuration, more options are available. For more information about options for collecting and rolling up child domain scores, see [Grouping domains in Performance Analytics domain configurations](pa-domain-separation-msp.md).

Only users with the pa\_admin role who are members of one of the domains that the job collects scores for can modify domain-separated data collection jobs. Global users with pa\_admin can modify any job.

By default, Platform Analytics Solutions use the global approach.

**Note:** Domain configurations require a global approach to domain separation. For more information, see [Grouping domains in Performance Analytics domain configurations](pa-domain-separation-msp.md).

## Domain-specific approach

By using domain-specific Performance Analytics records, you can grant the pa\_admin role to domain users to create their own domain-specific components. Users, including administrators, can create and edit Performance Analytics records only within their domain. Users in child domains can read but not edit Performance Analytics records in a parent domain.

You must create a domain-specific copy of a Performance Analytics record to use it in that domain. For example, to add a domain-specific condition to an indicator source, you must create a copy of the indicator and indicator source in that domain.

You can quickly copy an indicator or breakdown and related data from a different domain. Use the **Insert and Stay with Relations** UI action on the Indicator or Breakdown forms. Any breakdowns, breakdown exclusions, or time series exclusion relationships are also copied. Any associated scheduled jobs are copied only if the **Run as** user for that job is the current user.

To collect scores, create a new data collector job associated with the domain-specific indicators.

**Note:** Domain users cannot set Performance Analytics properties that begin with `com.snc.pa`. Only users with the admin or pa\_admin roles in the global domain can see or set these properties.

## Hybrid approach

A hybrid approach keeps reusable, foundational Performance Analytics records such as indicator sources within the global domain or a parent domain. At the same time, administrators in other domains create domain-specific higher-level Performance Analytics records such as indicators and widgets.

**Note:** The hybrid approach is an advanced option. Implement either the global or domain-specific approaches successfully before attempting to use a hybrid approach.

When using a hybrid approach, foundational records should be managed only within the global domain or a parent domain. All other Performance Analytics records, such as widgets and indicators, should be managed separately within each child domain. The following record types are considered foundational records:

-   Bucket groups
-   Buckets
-   Scripts
-   Breakdown sources
-   Indicator sources
-   Filters
-   Breakdowns
-   Managed sources
-   Manual breakdowns
-   Breakdown mappings
-   Breakdown relations

## Copying Performance Analytics records between domains

You can reuse Performance Analytics records in multiple domains. The PADomainUtils API provides functionality that enables administrators to move or copy Performance Analytics records between domains.

**Parent Topic:**[Domain separation and Performance Analytics](c_PAWithDomainSeparation.md)

