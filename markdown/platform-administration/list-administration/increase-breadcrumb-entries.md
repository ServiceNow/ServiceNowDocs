---
title: Increase the allowed number of breadcrumb entries
description: Add a system property to increase the number of breadcrumb entries that appear in a list filter.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/list-administration/increase-breadcrumb-entries.html
release: australia
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2026-11-09"
reading_time_minutes: 1
breadcrumb: [Restrict filters and breadcrumbs, Administer, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Increase the allowed number of breadcrumb entries

Add a system property to increase the number of breadcrumb entries that appear in a list filter.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_properties.list` in the filter.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Verify that the property does not exist by searching for **glide.ui.breadcrumb\_max\_entries**.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |**Name**|glide.ui.breadcrumb\_max\_entries|
    |**Type**|integer|
    |**Value**|Number of breadcrumb entries to display in the filter, for example, 15. The default is 10.|

5.  To verify this property, go to any table and use the filter modifier **is one of** to search for any number of items.

    The breadcrumb shows the number of entries specified in the **Value** field, followed by \[…\].

    \[Omitted image "BreadcrumbEntries.png"\] Alt text: Breadcrumb entries for incidents numbering from INC0010001 to INC0010015


