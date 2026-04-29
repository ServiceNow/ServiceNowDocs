---
title: Exclude classes from Dynamic IRE
description: Exclude specific classes, for which Dynamic IRE isn't beneficial, from Dynamic IRE. When a hierarchy branch \(such as the Hardware class branch\) is configured to use Dynamic IRE, you can configure specific classes within that branch, to be excluded from Dynamic IRE.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exclude classes from Dynamic IRE

Exclude specific classes, for which Dynamic IRE isn't beneficial, from Dynamic IRE. When a hierarchy branch \(such as the Hardware class branch\) is configured to use Dynamic IRE, you can configure specific classes within that branch, to be excluded from Dynamic IRE.

## Before you begin

There might be reasons for configuring child classes descending from the Hardware class, to be excluded from Dynamic IRE. For example, you might want to exclude a custom class with custom attributes, for which there are IRE rules that are based on those custom attributes. In this situation, it might not be beneficial to apply Dynamic IRE for that class and its descendants. When Dynamic IRE is enabled for the instance, Static IRE will still be used for those excluded classes.

Classes excluded from Dynamic IRE are stored in the Dynamic IRE skipped classes \[cmdb\_dynamic\_ire\_skip\_class\] table. Add a record for each Hardware-descending class, for which you don't want to apply Dynamic IRE to \(including the class descending classes\).

Role required:

-   To create, delete, and write: itil\_admin or sn\_cmdb\_admin
-   To read: itil, itil\_admin, or sn\_cmdb\_editor

## Procedure

1.  In the navigation filter, enter `cmdb_dynamic_ire_skip_class.list` to access the Dynamic IRE skipped classes table.

2.  In the list view select **New** and fill out the form.

    In the **Class to be skipped for Dynamic IRE** field, select a class that descends from the Hardware class, to which you don't want to apply Dynamic IRE. This exclusion applies to the specified class and to its descending classes.

3.  Select **Submit**.


**Parent Topic:**[Configuring CMDB Identification and Reconciliation](../concept/configuring-ire.md)

