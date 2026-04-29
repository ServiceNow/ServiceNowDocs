---
title: Edit a geography
description: Edit the boundaries or shapes of an existing territory geography in a map.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create geographies, Territory Planning, Set up workforce, Configure, Field Service Management]
---

# Edit a geography

Edit the boundaries or shapes of an existing territory geography in a map.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console**.

2.  Locate the territory card for which you want to edit geography and select the More Options \(![More Options icon.](../image/more_actions.png)\) icon.

3.  Select **Edit Geography**.

4.  Modify the geography based on the geography type.

    -   To edit a GeoJSON geography in the Territory Planning console, select the geography on the map and modify the boundaries. For more information, see [Create a GeoJSON geography in Territory Planning console](../concept/creating-a-gojson-geography.md#).
    -   To edit a geography that is created using matching attributes, select the **Matching Attributes** tab, and then select **Add**. For more information, see [Create a matching attributes geography](create-territory-matching-attributes.md).
    -   To edit a composite geography, see [Create a composite geography](create-a-composite-geography.md).
5.  After editing geography, you can see either the **Save** or **Save As New** option, depending on the number of related territories and your managerial permissions.

    If you only manage one related territory, it’s best to save the changes to the existing record since it only affects that specific territory. However, if you manage multiple territories or you don't have management permission for all related territories, it’s recommended to create a record to avoid impacting other territories.

    -   Select **Save** to modify the existing geography.
    -   Select **Save As New** to create a geography for the territory while preserving the previous one.
    **Note:** If both buttons are available, you can choose between saving the modifications to the existing geography or creating one.

    Once you have made your selection, the changes are saved, and the territory geography is updated accordingly.


