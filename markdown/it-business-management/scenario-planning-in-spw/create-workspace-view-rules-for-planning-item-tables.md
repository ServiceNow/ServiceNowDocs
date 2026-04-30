---
title: Create workspace view rules for new planning item forms in Strategic Planning
description: Define workspace view rules for the form views of new planning item types in Strategic Planning.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Define a new planning item type in Strategic Planning, Planning item configuration for lenses and portfolio plans, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create workspace view rules for new planning item forms in Strategic Planning

Define workspace view rules for the form views of new planning item types in Strategic Planning.

## Before you begin

-   [Create form views for new planning item tables in Strategic Planning](create-form-views-for-planning-item-tables-in-apw.md)
-   Ensure the application scope in your instance is set to Portfolio Planning

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Forms** &gt; **Workspace View Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For field information, see [View rule form](../reference/new-view-rule-form.md).

4.  In the Conditions section, select **Add Filter Condition** and add the following condition:

    -   For APW Default view: **Created** **is not empty**
    -   For Default view: **Created** **is empty**
5.  Select **Submit**.

6.  Repeat this process until you have completed creating both workspace view rules.


## What to do next

[Enable custom item types in Strategic Planning](enable-custom-item-types-strategic-planning-workspace.md).

