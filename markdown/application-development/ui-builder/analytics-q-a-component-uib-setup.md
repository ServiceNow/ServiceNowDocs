---
title: Analytics Q&amp;A component setup
description: Through Natural Language Query, the Analytics Q&amp;A component enables any user, regardless of technical background, to discover and ask information about the data they have access to.The Analytics Q&amp;A component doesn't have any user-configurable properties.Select event handlers to configure the actions \(events\) provided with the Analytics Q&amp;A component.Set up Analytics Q&amp;A so that when your users ask a question, they see only the results and not the other components on the page. They see the other components again when they navigate back.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/analytics-q-a-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Analytics Q&amp;A component setup

Through Natural Language Query, the Analytics Q&amp;A component enables any user, regardless of technical background, to discover and ask information about the data they have access to.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

If you have the Base Agent Workspace UX application, which is included in the base system, you have an Analytics Center page template. If you create a page using that template, it contains an Analytics Q&amp;A component. The events on this component have Link to destination Relay event handlers, which you use as a basis for Link to destination event handlers.

**Note:** This component has no configurable properties. You can determine where to redirect query results by configuring the event handlers.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Analytics Q&amp;A component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "analytics-qa-content-tree.png"\] Alt text: Content tree showing custom labeled Analytics Q&amp;A component

2.  Select the Analytics Q&amp;A component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Analytics Q&amp;A label you created for your component in the content tree.

**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Analytics Q&amp;A component properties

The Analytics Q&amp;A component doesn't have any user-configurable properties.

## Analytics Q&amp;A component events

Select event handlers to configure the actions \(events\) provided with the Analytics Q&amp;A component.

The Events tab shows the events used by the Analytics Q&amp;A component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the component actions to the data you want to display to your users. Expand the event in the list and select **Add an event handler**. For information about event handlers, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_t5m_pt4_pnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Report visualization clicked

</td><td>

User selects a visualization based on table data from the results of "Ask a question about your data."Event handler: Link to Destination

 Suggested target component: List

</td></tr><tr><td>

Indicator visualization clicked

</td><td>

User selects an indicator visualization from the results of "Ask a question about your data."Event handler: Link to Destination

 Suggested target component: KPI Details

</td></tr><tr><td>

List item clicked

</td><td>

User selects column data from the results of "Ask a question about your data."Event handler: Link to Destination

 Suggested app route: A page configured to show records

</td></tr><tr><td>

Ask button clicked

</td><td>

Hides other components on page when user asks for query results. Event handler: A script you write to hide the components on the page. To restore the components, configure the "Back button clicked from NLQ Results page" event.

</td></tr><tr><td>

Back button clicked from NLQ Results page

</td><td>

Restores components hidden by "Ask button clicked" when user selects to go back from the query results.Event handler: A script you write to restore the components on the page, reversing the results of the script you wrote for "Ask button clicked." For an example of script for both events, see Show Analytics Q&amp;A results in full page.

</td></tr></tbody>
</table>### Linking Report Visualization Clicked event to List component

Set the following properties to link the Report Visualization Clicked event in an Analytics Q&amp;A component to the suggested List component. You can link to a different component if that component takes a subset or none of the properties listed here. To link one component to another, follow these broad steps:

1.  Create the page that will hold the target component.
2.  Add the required and optional parameters to that page.
3.  Add the List component to the page.
4.  Configure the List component with the properties.
5.  In the linking component, add a **Link to destination** event handler to the linking event.
6.  In the destination of the event handler, select an app route to the page that holds the target component.
7.  Configure the event handler properties.

**Tip:** If you have the Platform Analytics Workspace, which is included in the base system, you have a Simple List page template. You can create a page in your application using this template. Only copy the contents of the page. The component config properties are populated. You have to add the required and optional page parameters. Also configure the relevant event handler on the Analytics Q&amp;A component to link to this page.

|Parameters on page containing List|Value of corresponding Config fields on List|Link to Destination event handler properties|
|----------------------------------|--------------------------------------------|--------------------------------------------|
|table \(required\)|@context.props.table|@payload.table|
|listTitle \(optional\)|@context.props.listTitle|@payload.listTitle|
|query \(optional\)|@context.props.query|@payload.query|
|disableInlineEditing \(optional\)|@context.props.disableInlineEditing|None|

In the following example, the Link to Destination event handler for a Report Visualization Clicked event is configured to link to a page with the route /simplelist. That page contains a List component.

\[Omitted image "analytics-qa-report-viz-link-dest.png"\] Alt text: Shows the suggested Link to destination event handler configuration, with /simplelist for the route

### Linking Indicator Visualization Clicked event to KPI Details component

Set the following properties to link the Indicator Visualization Clicked event in an Analytics Q&amp;A component to the suggested KPI Details component. You can link to a different component provided that component takes a subset or none of the properties listed here. To link one component to another, follow the broad steps in the "Linking Report Visualization Clicked event to List component" section of this topic.

**Tip:** If you have the Base Agent Workspace UX application, which is included in the base system, you have a KPI Details page template. You can create a page in your application using this template. Only copy the contents of the page. The component config properties are populated. You have to add the required and optional page parameters. Also configure the relevant event handler on the Analytics Q&amp;A component to link to this page.

|Parameters on page containing KPI Details|Value of corresponding Config fields on KPI Details|Link to Destination event handler properties|
|-----------------------------------------|---------------------------------------------------|--------------------------------------------|
|uuid \(required\)|@context.props.uuid|@payload.indicatorSysid|
|scoreDate \(optional\)|@context.props.scoreDate|@payload.scoreDate|
|breakdown \(optional\)|@context.props.breakdown|@payload.breakdowns|
|domain \(optional\)|@context.props.domain|@payload.domain|

In the following image, the Link to Destination event handler for an Indicator Visualization Clicked event is configured to link to a page with the route ac\_kpi\_details, which contains a KPI Details component.

\[Omitted image "analytics-qna-indicator-event-handler.png"\] Alt text: The event handler configured for an Indicator Visualization Clicked event on an Analytics Q&amp;A component

### Linking List Item Clicked event to page showing records

Set the following properties to link the List Item Clicked event in an Analytics Q&amp;A component to open a record. You do not link to one specific component for displaying a record. Instead, link to a page that is set up with scripts and visual subcomponents to display records. Some properties are also passed to some components, such as Record tabs.

**Tip:** If you have the Base Agent Workspace UX application, which is included in the base system, you have a Record page template. You can create a page in your application using this template. Only copy the contents of the page. The component config properties are populated. You have to add the required and optional page parameters. Also configure the relevant event handler on the Analytics Q&amp;A component to link to this page.

|Parameters on Record page|Config properties on Record Tab and other components, such as Header|Link to Destination event handler properties|
|-------------------------|--------------------------------------------------------------------|--------------------------------------------|
|table \(required\)|@context.props.table|@payload.table|
|sysid \(required\)|@context.props.sysId|@payload.row.sys\_id.value|
|query \(optional\)|None|@payload.breakdowns|
|extraParams \(optional\)|None|@payload.domain|
|views \(optional\)|None|None|
|selectedTabIndex \(optional\)|@context.props.selectedTabIndex \(Record tab only\)|None|
|None|None|@payload.row.name.value|

In the following image, the Link to Destination event handler for a List Item Clicked event is configured to link to a page with the route /record. The title for the records page is passed in `@payload.row.name.value`.

\[Omitted image "list-item-clicked-event-handler.png"\] Alt text: The configuration of the Link to destination event handler for a List Item Clicked event

**Related topics**  


[Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/create-page.md)

## Show Analytics Q&amp;A results in full page

Set up Analytics Q&amp;A so that when your users ask a question, they see only the results and not the other components on the page. They see the other components again when they navigate back.

### Before you begin

This procedure assumes you have a page with an Analytics Q&amp;A component and other components.

Role required: None

### About this task

For Analytics Q&amp;A results to appear in a full page, create the following items:

-   A client state parameter for whether full page is enabled
-   A client script to make the results appear in a full page
-   A client script to reset the page to show all components

Then you configure the Analytics Q&amp;A component to use these scripts. Lastly, configure the other components on the page to be hidden or not according to the state parameter.

**Tip:** If you have the Base Agent Workspace UX application, which is included in the base system, you have an Analytics Center page template. If you create a page using that template, it contains an Analytics Q&amp;A component that is set up to show the results in full-page format.

### Procedure

1.  Navigate to your experience and open it in UI Builder.

2.  Open the relevant page that has an Analytics Q&amp;A component.

3.  Open the **Client state** menu from the icon in the bottom-left margin.

    \[Omitted image "client-state-icon.png"\] Alt text: Client state icon with tooltip

4.  Create a Boolean parameter with a meaningful name and no initial value.

    In this example, you have named the parameter **nlq\_results\_full\_page**. You use the default code:

    ```
    {
      "nlq_results_full_page": false
    }
    ```

5.  Open the **Client scripts** menu from the icon in the bottom-left margin.

    \[Omitted image "client-scripts-icon.png"\] Alt text: Client scripts icon with tooltip.

6.  Create a script with a meaningful name that sets the value of the state parameter you created to `true`.

    In this example, you have named the script Set NLQ Results Full Page. The script sets the **nlq\_results\_full\_page** parameter to `true`:

    ```
    /**
     * @param {params} params
     * @param {api} params.api
     * @param {any} params.event
     * @param {any} params.imports
     */
    function handler({api, event, helpers, imports}) {
    	api.setState('nlq_results_full_page', true);
    }
    ```

7.  Create a script with a meaningful name that resets the value of the state parameter to `false`.

    In this example, you have named the script Reset NLQ Results Full Page View. The script sets the **nlq\_results\_full\_page** parameter to `false`:

    ```
    /**
     * @param {params} params
     * @param {api} params.api
     * @param {any} params.event
     * @param {any} params.imports
     */
    function handler({api, event, helpers, imports}) {
    	api.setState('nlq_results_full_page', false);
    }
    ```

8.  Select the Analytics Q&amp;A component and open the **Events** tab.

9.  Expand the **Ask button clicked** event and select **+ Add a new event handler**.

10. Select the script you created that sets the state parameter to `true` and select **Apply**.

    In this example, you have selected the Set NLQ Results Full Page script.

    \[Omitted image "analytics-qa-select-script.png"\] Alt text: The Event Handler preview dialog for the Ask button clicked event, showing Set NLQ Results Full Page selected.

11. Expand the **Back button clicked from NLQ Results page** event and select **+ Add a new event handler**.

12. Select the script you created that sets the state parameter to `false` and select **Apply**.

    In the example, this script is Reset NLQ Results Full Page View.

13. For each of the remaining components, follow these steps:

    1.  Select the component.

    2.  Click the **Edit component visibility** icon above the config panel.

        \[Omitted image "edit-component-visibility.png"\] Alt text: Edit component visibility button at the top of the config panel.

    3.  At the **Hide component** field, select the **Data** icon.

    4.  Browse for the client state parameter that you created.

        This parameter has the `@state` prefix.

        In the example, the client state parameter is named **nlq\_results\_full\_page**, so the field value is `@state.nlq_results_full_page`.

        \[Omitted image "hide-component-state-parm.png"\] Alt text: Hide component field on Component visibility panel showing state parameter selected


### What to do next

You can look at a fully configured Analytics Q&amp;A component in the Base Agent Workspace experience, included in the base system.

