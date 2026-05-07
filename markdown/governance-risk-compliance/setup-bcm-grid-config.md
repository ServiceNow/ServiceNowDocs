---
title: Set up grid configuration for BIA dependency assessment
description: Set up the grid configuration to render the BIA dependency assessment grid with configured columns.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Grid configuration, BCM in the Classic Workspace, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Set up grid configuration for BIA dependency assessment

Set up the grid configuration to render the BIA dependency assessment grid with configured columns.

## Before you begin

Role required: sn\_bcm.admin

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **General Administration** &gt; **Grid Configurations**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the grid configuration.|
    |Grid category|Grid category for which the configuration is applicable. For example, DEP\_ASSMNT.|
    |Element definition|Configuration item to be assessed in the BIA. In grid category, if enable element context is true then grid configuration should be based on element.|
    |Active|Option to set the record active. If the option is disabled then the grid is rendered based on the configured view. Only one active configuration for a category and element should be present.|
    |Grid column configuration|
    |Field source|Source from which the fields must be selected. For example, dependency, element, and element variable tables.|
    |Source table|Table that has the field.|
    |Field|Name of the field.|
    |Order|Order of column appearance in the grid.|
    |Enable filter|Option to set filter on columns.|
    |Enable grouping|Option to enable grouping of columns.|
    |Enable sort|Option to enable sorting of the columns.|

4.  Click **Submit**.


