---
title: Exclude classes from CMDB 360
description: Prevent CMDB 360 from collecting, storing, and analyzing data for classes for which it isn't needed. CMDB 360 processes large amounts of data. Therefore, excluding classes can help improve the performance of the Multisource Dashboard Analytics Population scheduled job and of CMDB 360 queries.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CMDB 360/Multisource CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exclude classes from CMDB 360

Prevent CMDB 360 from collecting, storing, and analyzing data for classes for which it isn't needed. CMDB 360 processes large amounts of data. Therefore, excluding classes can help improve the performance of the Multisource Dashboard Analytics Population scheduled job and of CMDB 360 queries.

## Before you begin

Role required: cmdb\_ms\_admin \(automatically included in the CMDB Admin role\)

## About this task

To exclude classes from CMDB 360, you must directly manage records in the CMDB 360 denied classes \[cmdb\_multisource\_deny\_class\] table. For each class that you want to exclude, add an active record for that class. Excluding a class from CMDB 360 also automatically excludes any of its descending classes. In the base system, the CMDB 360 denied classes table is populated by default with some classes, such as dscy\_net\_base and discovery\_net\_base.

## Procedure

1.  Select **All** and then, in the Filter navigator, enter `cmdb_multisource_deny_class.list` to open the CMDB 360 denied classes table.

2.  Select **New** and then fill out the form.

    -   Select the class to exclude \(with its descendents\) in the field labeled **Deny this class and all extended classes from this class to store CMDB 360 data**.
    -   Ensure that **Active** is selected. If **Active** isn't selected, then the specified class isn't excluded from CMDB 360.
    -   Select **Submit**.

## Result

Existing data for the specified class and its descending classes will be gradually removed from the CMDB 360 Data \[cmdb\_multisource\_data\] table using record cleaners, without any impact to the system.

## What to do next

You can deselect **Active** or completely delete a record for a class that you want to include in CMDB 360 data collection.

