---
title: Set a CI field to be recommended
description: Define a list of CI fields as recommended, noting that it is desirable that they are populated by a data source such as Discovery. You can then configure the CMDB completeness KPI to include recommended fields in its aggregated health reports.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set a CI field to be recommended

Define a list of CI fields as recommended, noting that it is desirable that they are populated by a data source such as Discovery.You can then configure the CMDB completeness KPI to include recommended fields in its aggregated health reports.

## Before you begin

Role required:

-   sn\_cmdb\_admin or Itil\_admin, and personalize\_dictionary: For editing the dictionary table
-   sn\_cmdb\_editor and itil have read access

## About this task

Use this procedure for fields which should not be mandatory, but that might have useful information that the CI should have. For example, a field with information that might at some point help with diagnosis. Initially, a derived class is set with the recommended fields that are defined at the parent level. You can add or remove recommended fields for a derived class, setting it with its own recommended fields, without affecting the recommended fields at the parent or sibling levels. If all recommended fields for a derived class are removed, then the derived class automatically derives the recommended fields from its parent class.

The CI Class Manager doesn't support dot-walking for selecting fields from referenced tables, as recommended. See the steps at the end of this procedure to directly update tables with recommended fields, using one level dot-walking.

For more information about child and parent classes, see Table extension and classes.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to show the CI Classes list, and then select the class that contains the fields that need to be set as recommended.

3.  In the class navigation bar, expand **Health**, select **Completeness**, and then select the Recommended Fields tab.

4.  In the Recommended Fields tab, use the list collector to move the fields that you want to designate as recommended, from the **Available** list to the **Selected** list.

5.  Click **Save**.


## What to do next

To directly update the CMDB Recommended Fields \[cmdb\_recommended\_fields\] table, \(outside the CI Class Manager\), using dot-walking to designate a field from a referenced table, as recommended:

1.  Select **All**.
2.  In the Filter navigator, enter `cmdb_recommended_fields.list` to access the CMDB Recommended Fields table.
3.  On the CMDB Recommended Field form, set **Table** to the table that you want to set with recommended fields.
4.  Select **Recommended fields** and use the list collector to select recommended fields for the table. You can expand a reference field up to one level, and use dot-walking to select a field from a referenced table.
5.  Select **Submit**.

