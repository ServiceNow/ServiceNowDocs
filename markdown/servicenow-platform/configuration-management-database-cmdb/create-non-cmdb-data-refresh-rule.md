---
title: Create a data refresh rule for a non-CMDB table
description: To apply Identification and Reconciliation Engine \(IRE\) features to supported non-CMDB tables, create data refresh rules for those tables. Data refresh rules are used to determine if a record is stale for a specific data source. Such records can then be updated by a lower-priority authorized data source.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [IRE support for non-CMDB tables, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a data refresh rule for a non-CMDB table

To apply Identification and Reconciliation Engine \(IRE\) features to supported non-CMDB tables, create data refresh rules for those tables. Data refresh rules are used to determine if a record is stale for a specific data source. Such records can then be updated by a lower-priority authorized data source.

## Before you begin

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

## About this task

Data refresh rules have no impact when dynamic reconciliation rules are in effect.

Data refresh rules are used in conjunction with static reconciliation rules to determine reconciliation steps for a record. These rules determine if, when, and by which data source a record can be updated.

## Procedure

1.  Click **All**.

2.  In the Filter navigator, enter `cmdb_datasource_staleness.list` to open the Data Source Staleness Definitions table.

3.  In the Data Source Staleness Definitions list view, click **New**.

4.  Fill out the Data Source Staleness Definitions form.

<table id="table_ypd_12f_z1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applies to

</td><td>

Non-CMDB class that this rule applies to.

</td></tr><tr><td>

Data source

</td><td>

Data source for which record staleness is evaluated.

</td></tr><tr><td>

Effective Duration

</td><td>

The time period that is used for the staleness evaluation.If the fields specified in the static reconciliation rule for the record's class were not updated by the specified data source within the specified time period — the record is determined to be stale for that data source.

 If you enter a value with a prefix that is valid and a suffix that is not, such as `15 x` — the valid portion of the value is used \('15'\). If the entire value is invalid — the default value of 0 is used.

</td></tr><tr><td>

Active

</td><td>

Activates the rule.

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[IRE support for non-CMDB tables](../concept/ire-support-non-cmdb-tables.md)

