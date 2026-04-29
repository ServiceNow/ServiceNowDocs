---
title: Create an EVAM definition
description: Define the list of data sources to render. The Entity View Action Mapper \(EVAM\) definition is the main record for an EVAM configuration.
locale: en-US
release: australia
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing Entity View Action Mapper, Entity view action mapper, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create an EVAM definition

Define the list of data sources to render. The Entity View Action Mapper \(EVAM\) definition is the main record for an EVAM configuration.

## Before you begin

Role required: admin or evam\_admin

## Procedure

1.  Navigate to **All** &gt; **Entity View Action Mapper \(EVAM\)** &gt; **EVAM Definitions**, and then select **New**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the EVAM configuration.|
    |Active|Option to activate the EVAM definition.|
    |Sort Order|Order the data is ordered on the EVAM definition. You can select **Ascending** or **Descending**.|
    |Application|Application scope of the EVAM definition.|

3.  Select **Submit** and then select your EVAM definition.

4.  In the EVAM Data source M2Ms related list, add a data source.

<table id="choicetable_s23_h4l_wnb"><tbody><tr><td id="d353191e180">

**Create and Link**

</td><td>

[You can define a new data source](define-evam-datasource.md) and then link this data source to your EVAM definition.

</td></tr><tr><td id="d353191e196">

**Link Existing**

</td><td>

You can add a pre-defined data source to your EVAM definition.

</td></tr><tr><td id="d353191e205">

**Unlink Selected**

</td><td>

You can remove the selected data source from your EVAM definition.

</td></tr></tbody>
</table>5.  Select **Submit**.

6.  In the EVAM View Config Bundle M2Ms related list, add a configuration bundle.

<table id="choicetable_lwc_h2h_xnb"><tbody><tr><td id="d353191e236">

**Create and Link**

</td><td>

[You can define a new configuration bundle](define-view-configuration-bundle.md) and then link this bundle to your EVAM definition.

</td></tr><tr><td id="d353191e255">

**Link Existing**

</td><td>

You can add a pre-defined configuration bundle to your EVAM definition.

</td></tr><tr><td id="d353191e264">

**Unlink Selected**

</td><td>

You can remove the selected configuration bundle from your EVAM definition.

</td></tr></tbody>
</table>    After you link the configuration bundles, you can define an order to prioritize the bundles, with the lowest number receiving the higher precedence.

7.  In the EVAM Data Filters related list, select **New** and fill in the form to add data filters:

    |Field|Description|
    |-----|-----------|
    |Label|Label name of the EVAM data filter.|
    |Active|Option to activate the EVAM data filter.|
    |Order|Priority that the EVAM view configuration takes over other view configurations. To give higher priority to a view configuration, enter a lower number.|
    |Application|Application scope of the EVAM view configuration.|
    |EVAM Definition|Associate an EVAM definition with the data filter.|

8.  Select **Submit**.


