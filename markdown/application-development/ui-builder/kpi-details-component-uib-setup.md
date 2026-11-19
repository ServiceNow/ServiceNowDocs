---
title: KPI Details component setup
description: The KPI Details component allows click-through from a data visualization or a key performance indicator \(KPI\) on an experience. You can configure which indicators and the breakdowns, dates, and domains of those indicators to display. Users can then analyze indicator trends over time, drill down to relevant records, set and monitor targets, and improve their process​.Select event handlers to configure the actions \(events\) provided with the KPI Details component.Select event handlers to configure the actions \(events\) provided with the KPI Details component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/kpi-details-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# KPI Details component setup

The KPI Details component allows click-through from a data visualization or a key performance indicator \(KPI\) on an experience. You can configure which indicators and the breakdowns, dates, and domains of those indicators to display. Users can then analyze indicator trends over time, drill down to relevant records, set and monitor targets, and improve their process​.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your KPI Details component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "kpi-details-content-tree.png"\] Alt text: Content tree showing custom label for a KPI Details component

2.  Select the KPI Details component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the KPI Details label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## KPI Details component properties

Select event handlers to configure the actions \(events\) provided with the KPI Details component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_lkc_b1d_qnb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indicator\[indicatorSysid\]

</td><td>

Indicator to display on the runtime. You can select the indicator from a list or pass it as a scripted parameter. You can also pass the value from another component through data binding, with the property `@context.props.uuid`. In this case, the page with the KPI Details component must have `uuid` as a required field.

</td></tr><tr><td>

Breakdowns\[breakdowns\]

</td><td>

Breakdowns to be applied by default to the indicator on the runtime. Pass an array of JSON parameters. The first set of parameters contains the first-level breakdown sys\_id and one or more breakdown elements. You can optionally pass a second set of parameters with a second-level breakdown sys\_id and one breakdown element.Format:

```
{
     sysId: '<breakdownSysId>',
     elements: [
         '<elementSysId1>'
         '<elementSysId2>'
          ...
     ]
}
{
     sysId: '<2ndLevelBreakdownSysId>',
     elements: [
          '<elementSysId>'
     ]
}       
```

You can also pass the value from another component through data binding, with the property `@context.props.breakdown`. In this case, the page with the KPI Details component must have `breakdown` as an optional parameter.Default: If no values are passed, indicator scores are shown without breakdowns.

</td></tr><tr><td>

Aggregate\[aggregate\]

</td><td>

A default time aggregate, such as By month SUM, to apply to the indicator.

</td></tr><tr><td>

Domain\[domain\]

</td><td>

A specific domain to restrict the scores to. You can pass the domain from another component through data binding, with the property `@context.props.domain`. In this case, the page with the KPI Details component must have `domain` as an optional parameter.Default: Global

</td></tr></tbody>
</table><table id="table_vjb_bjc_pwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Score date\[scoreDate\]

</td><td>

Date \('YYYY-MM-DD'\) for which indicator scores are displayed. You can pass it from another component through data binding, with the property `@context.props.scoreDate`. In this case, the page with the KPI Details component must have `scoreDate` as an optional parameter.Default: The last date for which scores are available.

</td></tr><tr><td>

Date range: Start date\[startDateProp\]

</td><td>

The date in the format 'YYYY-MM-DD' to start the date range.Default: The first date for which scores are available.

</td></tr><tr><td>

Date range: End date\[endDateProp\]

</td><td>

The date in the format 'YYYY-MM-DD' to end the date range. Default: The last date for which scores are available.

</td></tr></tbody>
</table><table id="table_pyh_cjc_pwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show records view\[recordsListView\]

</td><td>

Enable this property if the Records view should be shown when KPI Details opens.

</td></tr><tr><td>

Show statistics horizontally\[showHorizontalStatisticOrientation\]

</td><td>

Shows statistics in a horizontal row instead of a vertical list.Default: **true**

</td></tr></tbody>
</table><table id="table_owg_djc_pwb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable record quick-view\[showRecordQuickEdit\]

</td><td>

When turned on and the records are shown in runtime, each listed record has an information icon that opens a quick edit pane. Default: **true**

</td></tr><tr><td>

Enable records comparison\[showCompareRecords\]

</td><td>

Set whether a user has access to the Compare Records function. This function compares indicator scores, targets, and records for two dates.Default: **true**

</td></tr><tr><td>

Enable real time update\[showRealTime\]

</td><td>

Sets whether KPI Details shows real-time scores by default. If set to true, the values for **Score date** and **Aggregate** can override this setting.The indicator record must have real-time scores enabled for KPI Details to display them, regardless of this property setting.

 Default: **false**

</td></tr><tr><td>

Enable target status badge\[showTargetBadge\]

</td><td>

Displays a badge in the score summary to indicate whether the score is on track to meet the target by the review date. Applies only if a target is set on the indicator and that target has a review date.Default: **true**

</td></tr></tbody>
</table>## KPI Details component events

Select event handlers to configure the actions \(events\) provided with the KPI Details component.

The Events tab shows the events used by the KPI Details component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the KPI Details actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_t5m_pt4_pnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record list row clicked

</td><td>

Dispatched when the user has **Show records** turned on and selects the link to a record.Payload contains:

-   row: Row \(object\) containing the ID and display value
-   table: Table name of the selected row
-   listTable: Table name being viewed when clicking a row
-   nativeEvent: Event object
-   sys\_id: Sys ID of the record selected

</td></tr><tr><td>

Formula component clicked

</td><td>

Enables links from the information pane for a formula indicator to the KPI Details for each of the contributing indicators.\[Omitted image "kpi-details-contributing-indicator-links.png"\] Alt text: Links to KPI Details for contributing indicators in info pane of formula indicator.

 Payload contains:

-   indicatorSysid: SysID of the indicator selected
-   scoreDate: Date format \('YYYY-MM-DD'\) in which the formula indicator's scores are displayed
-   breakdowns: Breakdown to apply to the formula indicator
-   domain: Domain of the formula indicator

</td></tr></tbody>
</table>### Linking Record list row event to page showing records

Set the following properties to link the Record list row event in a KPI Details component to open a record. You do not link to one specific component for displaying a record. Instead, link to a page that is set up with scripts and visual subcomponents to display records. Some properties are also passed to some components, such as Record tabs.

**Tip:** If you have the Base Agent Workspace UX application, which is included in the base system, you have a Record page template. You can create a page in your application using this template. Only copy the contents of the page. The component configuration properties are populated. You have to add the required and optional page parameters. Also configure the relevant event handler on the KPI Details component to link to this page.

|Parameters on Record page|Config properties on Record Tab and other components, such as Header|Link to Destination event handler properties|
|-------------------------|--------------------------------------------------------------------|--------------------------------------------|
|table \(required\)|@context.props.table|@payload.table|
|sysid \(required\)|@context.props.sysId|@payload.sys\_id|
|query \(optional\)|None|@payload.breakdown|
|extraParams \(optional\)|None|@payload.domain|
|views \(optional\)|None|None|
|selectedTabIndex \(optional\)|@context.props.selectedTabIndex \(Record tab only\)|None|

In the following image, the Link to Destination event handler for a Record list row clicked event is configured to link to a page with the route /record.

\[Omitted image "kpi-details-record-list-row-clicked-handler.png"\] Alt text: The configuration of the Link to destination event handler for a Record list row clicked event.

### Linking Formula component event to KPI Details component

To link the Formula Component Clicked event in a KPI Details component to a KPI Details component, follow these steps:

1.  Create the page that will hold the KPI Details component. You can instead use the originating KPI Details component.
2.  Add the required and optional parameters to that page.
3.  Add the KPI Details component to the page, unless you are using the originating component.
4.  Configure the KPI Details component with the properties.
5.  In the originating KPI Details component, add a **Link to destination** event handler to the Formula Component Clicked event.
6.  In the destination of the event handler, select an app route to the page that holds the KPI Details component. Again, this can be the originating page.
7.  Configure the event handler properties.

**Tip:** If you have the Base Agent Workspace UX application, which is included in the base system, you have a KPI Details page template. You can create a page in your application using this template. Only copy the contents of the page. The component config properties are populated. You have to add the required and optional page parameters. Also configure the relevant event handler on the KPI Details component to link to this page.

|Parameters on page containing KPI Details|Value of corresponding Config fields on KPI Details|Link to Destination event handler properties|
|-----------------------------------------|---------------------------------------------------|--------------------------------------------|
|uuid \(required\)|@context.props.uuid|@payload.indicatorSysid|
|scoreDate \(optional\)|@context.props.scoreDate|@payload.scoreDate|
|breakdown \(optional\)|@context.props.breakdown|@payload.breakdowns|
|domain \(optional\)|@context.props.domain|@payload.domain|

In the following image, the Link to Destination event handler for a Formula Component Clicked event is configured to link to a page with the route ac\_kpi\_details. If this route is the originating page, the Link to Destination event reloads that KPI Details tab and shows that contributing indicator. If this route is another page with KPI Details, the Link to Destination event opens a new KPI Details tab that shows that contributing indicator.

\[Omitted image "indicator-scorecard-event-handler-config.png"\] Alt text: Configuration of Link to destination event handler for an Indicator Overview component.

