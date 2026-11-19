---
title: Filter component setup
description: The Filter component provides a unified filter experience for all other components in a workspace, including data visualization components that show data from either tables or indicators.Select the source tables and fields that you want to use for this Filter component. The Config tab then populates automatically with different configuration options depending on the type of field you selected.The following configuration options are available for filters that filter on one or multiple values from a set of choices. This filter type includes cascading filters.The following configuration options are available when you select a true/false type for the filter.The following configuration options are available when you select a Date type field for the filter. Date filters apply to Time Series visualizations for indicators and to Bar, Pie, Donut, and Single Score visualizations for tables.Select event handlers to configure the actions \(events\) provided with the Filter component.On UI Builder pages, create a custom event handler for Filter components to apply to any List or Data Visualization components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/filter-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 14
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Filter component setup

The Filter component provides a unified filter experience for all other components in a workspace, including data visualization components that show data from either tables or indicators.

## Before you begin

The dashboard in-line editor lets you add filters to dashboard tabs. You do not need to configure an event for filters added in this way. These instructions still apply if you work on a dashboard in the technical editor. For more information, see [Dashboards in configurable workspaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/analytics-center-dashboards.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Filter component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    This component label is visible only on the UI Builder. Do not confuse it with the Filter label, which is visible to the runtime user.

    \[Omitted image "filter-content-tree.png"\] Alt text: Content tree showing three Filter components with custom labels indicating the filter type

2.  Select the Filter component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Filter label you created for your component in the content tree.
    The **Filter type** and **FIlter label** fields appear in the Config tab.

3.  In the **Filter label** field, type a meaningful name for the filter.

    This label should help the runtime user.

4.  Select the filter type.

    -   Single select: A single value from a set of choices
    -   Multiple select: More than one value from a set of choices, such as both High and Critical Priority
    -   Date: A calendar date. You have the option to set a time. Automatically applies to all indicator data on page or tab.
    -   True/False: Whether a field value is true or false
5.  Specify the remaining configuration options for the filter.

    The available configuration options depend on the type of the field you selected to filter on: Single or Multiple Select, Date, or True/False.


## What to do next

**Tip:** If you have multiple filters on a page, dashboard, or tab, consider adding a Button component to clear all those filters at once. Add the following page script and use it for the button event handler:

```
function resetFilter ({ api }) {
  api.setState('parFilters', []);
}
```

**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Filter component properties

Select the source tables and fields that you want to use for this Filter component. The Config tab then populates automatically with different configuration options depending on the type of field you selected.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

**Note:** Select the filter type and label. All other properties are specific to the filter type.

<table id="table_mvp_yzg_d4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Filter type \[filterComponentType\]

</td><td>

The type of data that will be filtered. Other configuration options vary based on this value.-   Single select: A single value from a set of choices. This is the default filter type.
-   Multiple select: More than one value from a set of choices, such as both High and Critical Priority
-   Date: A calendar date. You have the option to set a time.

To apply a date filter to table data, specify the table and a date field. Date filters automatically apply to all indicator data on the page or tab.

You can also apply a date filter to table fields.

-   True/False: Whether a field value is true or false

</td></tr><tr><td>

Filter label \[filterLabel\]

</td><td>

A meaningful name for the filter that is visible to the user.

</td></tr></tbody>
</table>### Single or multiple select filter configuration options

The following configuration options are available for filters that filter on one or multiple values from a set of choices. This filter type includes cascading filters.

<table id="table_xzs_xkm_f4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Filter options

</td></tr><tr><td>

Filter element \[filterElementType\]

</td><td>

The visual element that will be used to select the filter value. The options are:-   Pill \(default\)
-   Radio buttons \(Single select\)
-   Checkbox \(Multi-select\)
-   Typeahead \(Multi-select\)

**Note:** Only the Pill element allows this filter to follow other filters. Also, only the Pill element allows this filter to be followed.

</td></tr><tr><td>

Show values in pill \[isShowSelectedValueInPill\]

</td><td>

\(Pill only\) Toggle on to show the selected filter elements inside the pill.

</td></tr><tr><td>

Filter label \[filterName\]

</td><td>

A meaningful name for the filter. This name is visible to users.

</td></tr><tr><td>

Max number of buttons \[fallbackLimit\]

</td><td>

\(Radio buttons only\) The maximum number of radio buttons. If the number of possible selections exceeds this limit, the filter element falls back to Pill.

</td></tr><tr><td>

Layout \[filterElementLayout\]

</td><td>

\(Radio buttons and checkboxes\) How the filter elements to choose from are displayed. For example, radio buttons can be laid out horizontally or vertically.

</td></tr><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td rowspan="2">

Filter source \[datasource\]

</td><td>

The data source for the filter, which determines the values available to filter by. Select only one filter source. After you select the filter source, select which of the available values to use. This property contains the following information:-   Filter source type: Table, Usage Insights, or indicator breakdown
-   Table: If the source type is Table, this value is the name of the table.
-   Field: If the source type is Table, this value is the specific field of the table.

If you select no field, you can only target that table or reference fields that point to that table. For example, if you select the Company table as your filter source, you can only select a field that references the Company table as the data to filter, such as Incident.Caller.Company or Incident.Location.Company.

If you select a field that is a reference field to another table, the filter source resets to refer to that table with no field selected. The filter target is set automatically to the reference field that you originally selected. The only additional targets you can set must be the table in the filter source or other reference fields pointing to that table. For example, if you try to select Incident.Assignment Group as the filter source, the filter source is set to the Group table, no field, and the data to filter is set as Incident.Assignment Group.

-   Indicator breakdown: If the source type is indicator breakdown, this value is the name of the indicator breakdown. You can select only breakdowns that at least one indicator is using.

**Important:** Only two levels of breakdown can be applied to an indicator at the same time. On a page, this could be two filters or one filter and a breakdown specified in the data visulization.

-   Usage Insights: Select a Usage Insights property and optionally a default value.

</td></tr><tr><td>

Configure values \(number\): Select which possible field values or breakdown elements the runtime user can choose to filter by. The button label shows how many values are selected.

</td></tr><tr><td>

Data to filter \[targets\]

</td><td>

The location of the data that will be filtered. Some filtering targets are set automatically, depending on the filter source. You can add any number of additional targets. Similarly to selecting a filter source, select either a table and field, a Usage Insights property, or all indicators with a particular breakdown. If you select a table, you can also select to apply the filter to the hierarchy of related tables: parents, children, siblings, and any database views that contain the table.

 **Note:**

-   If a table and a field is specified as the filter source, that table and field are selected automatically as a target. Only reference fields that point to that table and field can work as additional targets. The filter does not apply to any other targets you set.
-   If a table but no field is specified as the filter source, that table or a reference field pointing to that table is selected automatically as a target. Only that table or reference fields that point to that table can work as additional targets. The filter does not apply to any other targets you set.

</td></tr><tr><td>

Default values \[defaultSelectedItems\]

</td><td>

Select the default value or values for the filter. The dashboard applies these values when a user opens it.

</td></tr><tr><td class="sub-head" colspan="2">

Other filters to follow

</td></tr><tr><td>

Directly connected filters \[filtersFollowing\]

</td><td>

A list of filters on the same UI Builder page that this filter can follow. Select filters to populate the **filtersFollowing** array.

 Limitations:

-   You can only follow filters if Pill is the filter UI element for this filter.
-   Only filters with the Pill UI element can be followed.
-   Many-to-many relationships are not supported.

 For an example of a cascading filter, see [https://www.servicenow.com/docs/r/now-intelligence/create-select-filter-workspace.html](https://www.servicenow.com/docs/r/now-intelligence/create-select-filter-workspace.html).

</td></tr><tr><td>

Filters with table connection

</td><td>

If you want to filter by a many-to-many relationship between tables, you need to use a connecting table, which has a unique record for each match. For more information, see [https://www.servicenow.com/docs/r/now-intelligence/set-filter-to-follow-filter.html](https://www.servicenow.com/docs/r/now-intelligence/set-filter-to-follow-filter.html).

</td></tr><tr><td class="sub-head" colspan="2">

Advanced options

</td></tr><tr><td>

Sort direction \[sort\]

</td><td>

If you select Ascending, the lowest filtered values are shown first. If you select Descending, the highest values are shown first. The user can change this value.

</td></tr><tr><td>

Allow filter clearance \[enableClearFilter\]

</td><td>

Option to give users a control to clear the filter values.

</td></tr><tr><td>

Elements loaded at page refresh \[maxElements\]

</td><td>

The maximum number of elements loaded initially and at each page refresh. Default: 500

</td></tr></tbody>
</table>### True/false filter configuration options

The following configuration options are available when you select a true/false type for the filter.

<table id="table_bp1_knm_f4b"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Label for the filter element 'true' \[booleanLabelTrue\]

</td><td>

A string to display instead of 'true' to represent the value 'true.' For example, display 'Yes' for 'true.'

</td></tr><tr><td>

Label for the filter element 'false' \[booleanLabelFalse\]

</td><td>

A string to display instead of 'false' to represent the value 'false.' For example, display 'No' for 'false.'

</td></tr><tr><td>

Data to filter \[targets\]

</td><td>

The location of the data that will be filtered. You can add any number of additional targets. Select either a table and field, all indicators with a particular breakdown, or a Usage Insights property. If you select a table, you can also select to apply the filter to the hierarchy of related tables: parents, children, siblings, and any database views that contain the table.

 **Note:**

-   To help you select only true/false indicator breakdowns, the system restricts your choice to breakdowns based on a bucket \[pa\_buckets\] with only two values. However, the system does not check further whether the indicator breakdown is really true/false. You have to determine this yourself.
-   An empty value is possible for a field or breakdown. Therefore, the total number of true and false values can be less than the total number of records or the Count indicator score.

</td></tr><tr><td>

Default value \[defaultBoolean\]

</td><td>

Select 'true', 'false', or an empty value \(usually NULL in the database\). This value is applied when the user opens the page.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced options

</td></tr><tr><td>

Sort direction \[sort\]

</td><td>

If you select Ascending, the lowest filtered values are shown first. If you select Descending, the highest values are shown first. The user can change this value.

</td></tr><tr><td>

Allow filter clearance \[enableClearFilter\]

</td><td>

Option to give users a control to clear the filter values.

</td></tr></tbody>
</table>### Date filter configuration options

The following configuration options are available when you select a Date type field for the filter. Date filters apply to Time Series visualizations for indicators and to Bar, Pie, Donut, and Single Score visualizations for tables.

<table id="table_itz_mrm_f4b"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Data to filter \[targets\]

</td><td>

The location of the data that will be filtered. The filter is applied automatically to all Performance Analytics indicators and MetricBase KPIs on the page or tab based on the score date. You can add any number of date fields on tables or Usage Insights properties to apply the filter to as well. If you add a table, you can also select to apply the filter to the hierarchy of related tables: parents, children, siblings, and any database views that contain the table.

</td></tr><tr><td>

Date filter view \[dateFilterView\]

</td><td>

How the date filter is displayed.-   Both calendar and relative ranges, such as 7 days or Year To Date \(YTD\)
-   Calendar only
-   Relative ranges only

 In UI Builder, open **Select predefined ranges** to select the relative ranges that the user can choose from.

</td></tr><tr><td>

Allow time selection \[allowTimeSelection\]

</td><td>

When enabled, users can specify the time in hours and minutes instead of only the date.

</td></tr><tr><td>

Default values

</td><td>

Select a predefined relative range to be applied when a user opens a page that contains the filter.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced options

</td></tr><tr><td>

Allow filter clearance \[enableClearFilter\]

</td><td>

Option to give users a control to clear the filter values.

</td></tr></tbody>
</table>## Filter component events

Select event handlers to configure the actions \(events\) provided with the Filter component.

The Events tab shows the events used by the Filter component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Filter actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

When you click **Add a new event handler**, the event handler preview opens. The event requires you to create a custom event handling script. The scripts differ depending on whether you are filtering a List or a Data visualization component. Browse the event handler preview for the client script that you created. Instructions for creating the script follow.

|Event|Description|
|-----|-----------|
|Filter applied|The filter is applied. The action contains an array that includes the table, the field, and other information depending on the configuration.|

### Connect the filter to List and Data Visualization components

On UI Builder pages, create a custom event handler for Filter components to apply to any List or Data Visualization components.

#### Before you begin

This procedure assumes that the following tasks are complete:

1.  You have added the Filter component to the UI Builder page, as well as at least one Data Visualization or List component. The Filter can apply to multiple Data Visualizations or Lists.
2.  You have configured the filter to source and the data to filter, if applicable, for the Filter component. If the Filter component is supposed to filter a List, you have specified the table that the List component shows as data to filter.
3.  You have configured data sources for any Data Visualization components.
4.  You have specified a table for any List components.

Role required: ui\_builder\_admin, admin

#### Procedure

1.  Open the relevant UI Builder page.

    This page may be a technical dashboard.

2.  Navigate to the UI Builder State section and add a state variable named *parFilters* of type JSON with a simple array initial value `[]`.

    For more information, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

    \[Omitted image "add-parFilters.png"\] Alt text: Adding the parFilters client state parameter to a UIB page.

3.  Add a second JSON state variable named *encodedQueries* of type Object with initial value `{}`.

4.  Navigate to the Client Scripts section and create a custom script with a name such as "Apply PAR Filters" and the following content or a functional equivalent thereof:

    ```javascript
    function handler({ api, event, helpers, imports }) {
    	const mergePARFiltersV2 = imports["global.mergePARFilters"]().v2;
    	const { appliedFilters } = event.payload;
    	api.setState("parFilters", ({ currentValue, api }) => {
    		const { parFilters, encodedQueries } = mergePARFiltersV2(
    			currentValue,
    			appliedFilters
    		);
    		api.setState("encodedQueries", encodedQueries);
    		return parFilters;
    	});
    }
    ```

5.  In the Client Scripts section, open the **Client Script Includes** tab.

    \[Omitted image "client-script-includes.png"\] Alt text: The Client Script Includes tab of the Client Scripts pane on a UIB page.

6.  In the **Add a script include** field, select `mergePARFilters` and click **Add**.

    \[Omitted image "add-mergePARFilters.png"\] Alt text: Adding the mergePARFilters script include.

7.  Close the window for configuring data, client state, and client scripts.

8.  In the UI Builder, select the Filter component.

9.  Select the **Events** tab in the configuration panel and add the page script you have created, which in this example is Apply PAR Filters, as an event handler.

    \[Omitted image "add-apply-par-filters.png"\] Alt text: Adding the Apply PAR Filters script as the Filter applied event handler.

10. Save the page.


