---
title: Run the Item Diagnostic Results report
description: Identify the catalog items that are not designed per ServiceNow recommended practices to run your catalog efficiently.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Item diagnostic report, Debugging Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Run the Item Diagnostic Results report

Identify the catalog items that are not designed per ServiceNow recommended practices to run your catalog efficiently.

## Before you begin

Role required: admin or catalog\_admin

## About this task

This report runs every weekend on all catalog items of all types.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Request Reports**.

2.  Select the \[Catalog\] Item Diagnostics Results report.

    A report is displayed with all active catalog items with a non-zero score. These catalog items are grouped by score and each score has a different color.

3.  Click the score to diagnose the associated catalog items.

    **Note:**

    -   Any item with a score greater than zero indicates a recommended practice rule violation.
    -   The higher the score, the more is the catalog item deviating from ServiceNow recommended practices.
4.  Click the score of the required catalog item.

    Diagnostic results are displayed for the catalog item with violated rules. For information on default diagnostic rules per ServiceNow recommended practices, see [Item diagnostic report](../concept/c_ItemDiagnostic.md).

5.  To understand details of each violated rule, click the **Count** value for that rule.


**Parent Topic:**[Item diagnostic report](../concept/c_ItemDiagnostic.md)

