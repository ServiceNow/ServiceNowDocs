---
title: Create an EVAM definition
description: Define the list of data sources to render. The Entity View Action Mapper \(EVAM\) definition is the main record for an EVAM configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/entity-view-action-mapper-evam/define-composite-dataset.html
release: zurich
product: Entity View Action Mapper \(EVAM\)
classification: entity-view-action-mapper-evam
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use EVAM, EVAM, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
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

<table id="choicetable_s23_h4l_wnb"><tbody><tr><td id="d171620e186">

**Create and Link**

</td><td>

[You can define a new data source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/entity-view-action-mapper-evam/define-evam-datasource.md) and then link this data source to your EVAM definition.

</td></tr><tr><td id="d171620e202">

**Link Existing**

</td><td>

You can add a pre-defined data source to your EVAM definition.

</td></tr><tr><td id="d171620e211">

**Unlink Selected**

</td><td>

You can remove the selected data source from your EVAM definition.

</td></tr></tbody>
</table>5.  Select **Submit**.

6.  In the EVAM View Config Bundle M2Ms related list, add a configuration bundle.

<table id="choicetable_lwc_h2h_xnb"><tbody><tr><td id="d171620e242">

**Create and Link**

</td><td>

[You can define a new configuration bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/entity-view-action-mapper-evam/define-view-configuration-bundle.md) and then link this bundle to your EVAM definition.

</td></tr><tr><td id="d171620e261">

**Link Existing**

</td><td>

You can add a pre-defined configuration bundle to your EVAM definition.

</td></tr><tr><td id="d171620e270">

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


**Parent Topic:**[Using Entity View Action Mapper](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/entity-view-action-mapper-evam/managing-entity-view-action-mapper.md)

