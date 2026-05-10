---
title: Create a composite geography
description: Create a composite geography by combining different geographies into a single, powerful view for efficient planning. You can streamline tasks and optimize resources using a composite geography.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create geographies, Territory Planning, Set up workforce, Configure, Field Service Management]
---

# Create a composite geography

Create a composite geography by combining different geographies into a single, powerful view for efficient planning. You can streamline tasks and optimize resources using a composite geography.

## Before you begin

Role required: sn\_fsm\_tp.fsm\_territory\_planner, sn\_fsm\_tp.fsm\_territory\_manager

## About this task

Composite Geography combines smaller geographies into a bigger, more impactful one. For example, you can use composite geography if you've created three or more smaller geographies and now want to unite them into a larger geography.

## Procedure

1.  Open either Territory Planning platform or Territory Planning console based on your role.

    -   Navigate to **All** &gt; **Field Service** &gt; **Territory Planning**.
    -   Navigate to **All** &gt; **Field Service** &gt; **Territory Planning** &gt; **Territory Planning Console**.
2.  Do either of the following.

<table id="choicetable_jbt_4fz_szb"><thead><tr><th align="left" id="d148160e102">

To create composite geography

</th><th align="left" id="d148160e105">

Do this

</th></tr></thead><tbody><tr><td id="d148160e111">

**From Platform**

</td><td>

In the Territory Geographies page, select **New**.

</td></tr><tr><td id="d148160e123">

**From Territory Planning console**

</td><td>

1.  Select **Create Territory**.
2.  In the Geography field, select the New Geography for Territory icon \(![New Geography for Territory icon.](../image/EditWidgetButton.png)\).


</td></tr></tbody>
</table>3.  On the form, fill in the fields.

<table id="table_nfl_kt1_5tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the geography.

</td></tr><tr><td>

Geography Type

</td><td>

Select **Composite Geography**.

</td></tr><tr><td>

Composite geography

</td><td>

Select the geographies which you want to comprise into a composite geography. **Note:** You can choose up to 10 GeoJSON geographies. Avoid selecting a composite geography or a geography with matching attributes within another composite geography.

</td></tr></tbody>
</table>4.  Select **Submit**.

    The composite geography is created.


## Result

The composite geography encompasses all the latitude, longitude, and geo points contained within the selected geographies. Associate the composite geography to a territory to manage work order tasks in the Territory Planning console. The geography appears visually on the map when its territory is selected in the Territory Planning console.

## What to do next

Link the geography to a territory. For more information, see [Create a Field Service territory](create-territories-territory-planning-console.md).

