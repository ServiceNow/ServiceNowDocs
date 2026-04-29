---
title: Create an identification inclusion rule for a non-CMDB table
description: Narrow the scope of records that are included in the identification process of non-CMDB records by creating an identification inclusion rule.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [IRE support for non-CMDB tables, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create an identification inclusion rule for a non-CMDB table

Narrow the scope of records that are included in the identification process of non-CMDB records by creating an identification inclusion rule.

## Before you begin

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

## About this task

During duplication detection of independent CIs, the Identification and Reconciliation Engine \(IRE\) processes only the records that satisfy the identification inclusion rules. For example, you can set a filter to include only records whose state is operational. When no identification inclusion rules exist, all records are included in the identification process.

In the base system, there are no predefined identification inclusion rules. Identification inclusion rules are defined at the class level.

**Note:** Identification inclusion rules impact any script that calls IRE, therefore create them carefully. Identification inclusion rules can prevent the identification of certain types of records, affecting some features of Discovery and Service Mapping.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **Identification Inclusion Rules**.

2.  In the Identification Inclusion Rules list view, click **New**.

3.  Fill out the Identification Inclusion Rules form.

    |Field|Description|
    |-----|-----------|
    |Applies to|Non-CMDB table that this rule applies to.|
    |Inclusion condition|Criteria that non-CMDB records must meet to be included in the identification process.|

4.  Click **Save**.


**Parent Topic:**[IRE support for non-CMDB tables](../concept/ire-support-non-cmdb-tables.md)

