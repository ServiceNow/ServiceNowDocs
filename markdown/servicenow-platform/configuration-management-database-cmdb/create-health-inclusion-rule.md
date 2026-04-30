---
title: Create health inclusion rule
description: Filter the CIs that are included in health calculations and that appear in the CMDB Health Dashboard by defining health inclusion rules. Use health inclusion rules to temporarily filter out classes that generate a large number of failures, until the problems are fixed.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create health inclusion rule

Filter the CIs that are included in health calculations and that appear in the CMDB Health Dashboard by defining health inclusion rules. Use health inclusion rules to temporarily filter out classes that generate a large number of failures, until the problems are fixed.

## Before you begin

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

## About this task

Evaluation for the required, orphan, recommended, duplicate and staleness health metrics, will apply only to CIs that satisfy health inclusion rules. For example, health inclusion rules can limit CMDB Health scores of the duplicate metric only for server and network CIs.

**Note:**

-   You can specify health inclusion rules per domain.
-   Creating health inclusion rules at the level of the base cmdb\_ci table can potentially filter out health results of all classes in CMDB Health dashboards.
-   Applying a health inclusion rule to the duplicate metric, is supported only in the global domain.
-   Due to performance issues, dot-walking in health inclusion rules for the duplicate metric is not supported.

In addition to any health inclusion rules, [identification inclusion rules](create-id-inclusion-rule.md) also indirectly impact what appears in the CMDB Health Dashboard for duplicate CIs. The dashboard itself uses the identification engine \(IRE\) to identify duplicate CIs and therefore identification inclusion rules are applied.

Inheritance of health inclusion rules:

-   If there are no health inclusion rules specified for a child class, then rules specified on a parent class are applied to the child class.
-   If health inclusion rules are specified for a child class, then those rules take precedence over rules specified on a parent class.

In the base system, there are no predefined health inclusion rules, in which case all CIs are included in the CMDB Health calculations.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to show the CI Classes list and then select the class for which to create a health inclusion rule.

3.  In the class navigation bar, expand **Health** and then select **Health Inclusion Rules**.

4.  Select an existing rule to edit or select **New** and then fill out the Health Inclusion Rules form.

    |Field|Description|
    |-----|-----------|
    |Applies to|Class this rules applies to.|
    |Active record condition|Criteria that CIs must meet to be included in the evaluation for the specified health metrics.|
    |Applies to metric|Metrics that the rule applies to.|

5.  Select **Save** or **Update**.


## What to do next

You can delete a health inclusion rules that is no longer needed by selecting that rule, and then on the CMDB Health Configuration form, selecting **Delete**.

