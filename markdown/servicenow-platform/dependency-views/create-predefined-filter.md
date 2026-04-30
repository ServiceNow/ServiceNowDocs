---
title: Create a predefined filter
description: Create filters to narrow down the CIs that are displayed on a Dependency Views map. You can create filters that are based on CIs' class, CIs' attributes, or CIs' relationships.
locale: en-US
release: zurich
product: Dependency Views
classification: dependency-views
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Administer, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a predefined filter

Create filters to narrow down the CIs that are displayed on a Dependency Views map. You can create filters that are based on CIs' class, CIs' attributes, or CIs' relationships.

## Before you begin

Role required: ecmdb\_admin

## About this task

Create a predefined filter that you can then select to determine the scope of the CIs that are displayed in a Dependency Views map. **Configuration type** filters filter by CI class, **CI filters** filter by CI attributes, and **relationship filters** filter by relationships. Only CIs that match at least one of the configuration type filters \(if any exists\), and at least one of the CI filters \(if any exists\), and at least one of the relationship type filters \(if any exists\) - are displayed on the map. If no filters are defined, then no filtering is applied.

**Note:** Predefined filters do not apply to virtual groups. Therefore a virtual group displays even if it contains CIs that a predefined filter would have not included. Upon the expansion of a virtual group, predefined filters are applied, and any or all of the CIs that were previously virtually grouped, might no longer display on the map.

## Procedure

1.  Navigate to **All** &gt; **Dependency Views** &gt; **Predefined Filters**.

2.  On the **Predefined Filters** page, click **New**.

3.  Type in a **Name** for the filter.

4.  Click **Roles**, and in the **Roles** dialog box, select the roles that this filter will be available for.

5.  Right-click on the page header, and click **Save**.

6.  Create a configuration type filter:

    1.  Click **Configuration Types**, and then click **Edit**.

    2.  In the **Collection** list collector, select the classes that CIs must belong to in order to be displayed on the map, and move them to the **Configuration Types List**.

    3.  Click **Save**.

7.  Create a CI filter:

    1.  Click **CI Filters**, and then click **New**.

    2.  In the **CI Filters** page enter conditions to filter CIs by specific attribute values.

    3.  Click **Submit**.

8.  Create a relationship type filter:

    1.  Click **Relationship Type**, and then click **New**.

    2.  In the **Collection** list collector, select the relationships that CIs must have in order to be displayed on the map, and move them to the **Relationship Types List**.

    3.  Click **Save**.


## What to do next

After creating a predefined filter, you can apply it to a map:

1.  Click the Map settings icon ![Map settings.](../image/dv-map-settings.png) to open **Map Settings**.
2.  Select a filter from the **Predefined Filters** list.
3.  Click **Apply**.

**Parent Topic:**[Administer Dependency Views](../topic/p_AdministerNGBSM.md)

**Related topics**  


[Create or modify map indicators](t_CreateModifyNGBSMMapIndicators.md)

[Create or modify map icons](t_CreateModifyNGBSMMapIcons.md)

[Set a predefined filter as default](set-predefined-filter-default.md)

[Create or modify Map Related Items](t_CreateModifyNGBSMMapRelatedItems.md)

[Create or modify Dependency Views menu actions](t_CreateModifyNGBSMMenuActions.md)

[Condition and script parameters for menu actions](../reference/condition-script-parameters.md)

[Create or edit a dependency type](t_CreateMapScript.md)

[Filter the view of a Dependency Views map](t_FilterViewNGBSMMap.md)

