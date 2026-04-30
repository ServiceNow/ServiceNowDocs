---
title: Increase the allowed number of breadcrumb entries
description: You can add a property to allow for a larger number of breadcrumb entries in the filter.
locale: en-US
release: yokohama
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Restrict filters and breadcrumbs with fixed queries, Administering lists, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Increase the allowed number of breadcrumb entries

You can add a property to allow for a larger number of breadcrumb entries in the filter.

## Before you begin

Role required: admin

## Procedure

1.  Enter `sys_properties.list` in the Navigation filter.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Verify that the property does not exist by searching for **glide.ui.breadcrumb\_max\_entries**.

3.  Click **New**.

4.  Complete the form.

    |Field|Value|
    |-----|-----|
    |**Name**|glide.ui.breadcrumb\_max\_entries|
    |**Type**|integer|
    |**Value**|The number of breadcrumb entries you want to appear in the filter, for example, 15.The default number is 10.|

5.  To verify this property, go to any table and use the filter modifier **is one of** to search for any number of items.

    The number of entries you entered in the Value field displays before ending in a \[…\].

    ![Breadcrumb entries for incidents numbering from INC0010001 to INC0010015](../image/BreadcrumbEntries.png "Breadcrumb entries")


