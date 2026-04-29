---
title: Create or edit a relationship filter
description: Create a custom relationship filter to display CI relationships from selected tables in the CI relations formatter.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CI relations formatter, CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or edit a relationship filter

Create a custom relationship filter to display CI relationships from selected tables in the CI relations formatter.

## Before you begin

Role required: ecmdb\_admin

## About this task

The CI relations formatter displays related CIs for the base CI, and the relationships between the CIs. You can use relationship filters on the CI relations formatter to customize CI relationship views.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Relationships** &gt; **Relationship Filters**.

2.  Click **New** or select a filter to edit.

3.  Enter or edit the relationship filter name.

4.  Right-click the form header and click **Save**.

5.  In the **Configuration Types** section, click **Edit**.

6.  On the **Edit Members** form, select the tables of the CIs that you want to show with the filter and then move the tables to the **Configuration Types list**.

7.  Click **Save**.


## Result

On a CI form, in the relations formatter settings, you can select the newly defined relationship filter from the **Filter Relations by CMDB View** list.

In the legacy CI relations formatter, you can click **View** and select the newly defined relationship filter.

After you select a filter, the relations formatter displays only CIs from the tables specified in the filter or from descending tables.

**Parent Topic:**[CI relations formatter](../concept/c_CIRelationsFormatterNG.md)

