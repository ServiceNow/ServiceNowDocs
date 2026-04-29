---
title: Data Discovery jobs
description: Data Discovery reviews your targeted information using user-defined data patterns and target tables.
locale: en-US
release: australia
product: Data Discovery
classification: data-discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Data Discovery \(Classic\), Data Discovery, Platform Privacy]
---

# Data Discovery jobs

Data Discovery reviews your targeted information using user-defined data patterns and target tables.

Data Discovery works by first scheduling a job in the **Data Discovery Job** section. When a scheduled job runs, all active data patterns are searched for on the current target tables. For more information on creating and configuring a Data Discovery job, see [Configure a Data Discovery job](../task/configure-data-discovery-jobs.md).

**Note:** Sample Scan jobs scan up to 10,000 records are scanned per table per pattern.

**Warning:** If a job is executed twice in a small amount of time, the number of scanned rows may return 0 for second run.

## Data Discovery data patterns

The **Data Patterns** section shows all current data patterns, both active and inactive. A data pattern is a regular expression used to match sensitive data. For more information on how to access and configure data patterns, see [Configure Data Discovery patterns](../task/configure-data-discovery-patterns.md). The **Active Data Patterns** section shows only active patterns. Inactive patterns don’t appear.

## Target tables

The **Target Tables** section lists all tables that can be processed for a job. To access the target tables, select **Target Tables**.

The following tables aren’t supported:

-   sr
-   sysx
-   v
-   sh$
-   syslog
-   ua
-   usageanalytics
-   ecc
-   clone
-   jrobin
-   pa
-   sla\_repair\_log
-   scan
-   gcf
-   fm\_log
-   log
-   np$
-   sn\_data\_discovery
-   dp\_configuration
-   dp\_federated\_job
-   dp\_field\_technique
-   dp\_job
-   dp\_job\_summary
-   dp\_primary\_reference
-   dp\_technique
-   data\_classification
-   m2m\_dictionary\_dataclass

## Granular Configuration

The [Granular Configuration](../task/granular-configuration.md) tool enables more specific and fine tuned controls for discovering sensitive data in a table. However there are key differences in its operation compared to a traditional data discovery job. A granular configuration scans only specified columns of a table for discovery, reporting its findings by the record. Findings from the scan of Granular Configurations, called Granular Findings have their actions specified per record, and require the data\_privacy\_admin role to be anonymized.

