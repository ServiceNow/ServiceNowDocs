---
title: Omit record count in a list
description: Speed up how fast lists load by removing the calculation of the total number of records in a list.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [List configuration, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Omit record count in a list

Speed up how fast lists load by removing the calculation of the total number of records in a list.

## Before you begin

Role required: workspace\_admin

## About this task

Calculating the total number of records included in a list that's filtered from large tables can take a long time. Platform displays the total number of records in the list.

![Record calculation](../image/pagination-calculation.jpg)

To load lists faster, you can remove the page calculation for all or only specified filtered lists. When you remove the calculation, the total record count is not displayed and the double arrow icon \(![Forward arrows](../image/double-arrow-forward.jpg)\) is grayed out.

![No pagination](../image/no-pagination.jpg)

## Procedure

1.  Open a list, for example navigate to **Incident** &gt; **All**.

2.  Right-click a header in the list and navigate to **Configure** &gt; **List Control**.

3.  Select **Remove pagination count**.

4.  To omit the record count only in specific view:

    1.  Select **Remove pagination count for specific views**.

    2.  Beside Specific list of views prevented from getting full record count, click the lock icon \(![Lock icon](../../../common/image/icon-lock.png)\).

    3.  Select the search icon \(![Search icon](../image/magnifying-glass.png)\) and select the view where platform omits the page count.

    4.  Repeat the previous step for as many views as necessary.

5.  Select **Update**.


**Parent Topic:**[List configuration](../concept/c_ListConfiguration.md)

