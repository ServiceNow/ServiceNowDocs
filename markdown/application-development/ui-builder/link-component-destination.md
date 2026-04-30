---
title: Link an event to another page
description: Add a link to the destination event handler within UI Builder so that an event action can open another page. You can also configure the event handler to follow the App Route to the desired page.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Bind an event to a data resource, Bind events to add actions, Manage actions in UI Builder pages, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Link an event to another page

Add a link to the destination event handler within UI Builder so that an event action can open another page. You can also configure the event handler to follow the App Route to the desired page.

## Before you begin

You must have a workspace page that contains a component that is intended to open another page when a user clicks it. The dashboard overview is an example of such a component. Components such as **Link to Destination** do not support the link to destination event handle. The component link property takes priority over the link to destination event handler.

Role required: ui\_builder\_admin

## About this task

To configure an event action to open another page, you must know what page you want to open, what the required and optional parameters are for that page, and what payload values to set on the event handler to pass the required parameters to the destination page.

**Tip:** You may be able to find examples of both the components that you want to link from and the destination pages that you want to link to in the Base Agent Workspace Experience. This Next Experience is provided in the base system. If you create a page from a page template, you should only copy the contents of the template. Do not reference it. For more information about the difference between copying and referencing a page template, see [Create a page from a template](reuse-page-definitions.md).

## Procedure

1.  Open your experience in UI Builder.

2.  If the destination page doesn't exist in your experience, create one.

    For information about creating pages, see [Create a page in UI Builder](create-page.md). Make sure that you set the required and optional parameters for the page so that you can use it as a destination. If a particular component in the page is a destination, you must include that component. You also must configure the properties on the component to consume the page parameters with `@context.props.<parameter-name>` values.

    You might consider creating the page from a page template. The Base Agent Workspace Experience has several page templates that are already configured to be destinations for other components. If you create a destination page from a template, the components are already configured with the correct properties. Any necessary state parameters or client scripts are also copied over. You have to add the page parameters. You can copy these parameters from the UX App Routes related list on the Agent app config \[sys\_ux\_app\_config\] record of the experience that contains the page templates.

    To make sure that the pages that you are creating work reliably as destinations in your experience, your experience must have the same app shell UI as the experience with the page templates.

3.  Switch to the page that you want to link to the destination page.

4.  Navigate to the relevant component and select it.

5.  Select the **Events** tab.

6.  Select **+ Add event mapping**.

7.  Select the event you want to use.

8.  Select **+ Add event handler**.

    ![Arrow pointing to the + add event handler option.](../image/link-dest-add-handler.png)

9.  In the Inherited event handlers section, select **Link to destination**.

    ![Arrow pointing to the link to destination inherited event handler.](../image/link-destination-select-handler.png)

10. Click **Select destination**.

    ![Arrow pointing to the select destination button.](../image/event-handler-select-dest.png)

11. Expand **Pages** and select the page in the experience that you want to link to.

    Fields appear for each of the parameters on the destination page that the route leads to. Required parameters are marked with an asterisk \(\*\).

12. Complete each required parameter field and the applicable parameter fields with an appropriate `@payload.*` value.

    If the developers of your component included default payload values in your event, you can select one through autocompletion. As shown in the following example, the payload value may not match the parameter name.

    ![Using autocomplete to select the @payload.indicator_sysId property for the uuid parameter field.](../image/event-handler-destination-props.png)

    **Note:** You have the option to link to an External URL instead of specifying an **App route**.

    If no default values are provided, or you can't determine which values are correct for some fields, refer to the configuration and API documentation for the component in the [ServiceNow® Developer Site](https://developer.servicenow.com/). If you still can't find the necessary `@payload.*` values, contact Customer Service and Support.

    **Tip:** If you create your linking component by creating a page from a Base Agent Workspace page template, the component contains Link to destination Relay event handlers. These event handlers do not work. However, they contain the applicable `@payload.*` values for the parameters.


## Configuring the event handlers for an Analytics Q&amp;A component

Let's say that you want to take a new Next Experience and add a page with an Analytics Q&amp;A component. First, you create the page from the Analytics Center page template that is provided in the Base Agent Workspace experience. Next, you create a target page for the first of the three events in Analytics Q&amp;A and then you configure an event handler for that event.

By navigating to **Now Experiences Framework** &gt; **Experiences**, you see the Test experience UX application. Because it uses the same Agent Workspace App Shell UI as the Base Agent Workspace, you can use the page templates from the Base Agent Workspace.

![List of UX Applications.](../image/event-handlers-ux-app-list.png)

You next select the Test workspace admin panel, find an UX App Configuration record with no UX app routes or pages, and then click **Open**.

As the example shows, in the UI Builder, you have created a page named Analytics Center that is based on the Analytics Center page template from the Base Agent Workspace. Next, you select the option to copy only the contents of the page template.

![Create a page dialog.](../image/event-handler-create-page.png)

You select the Analytics Q&amp;A 1 component and open the **Events** tab. From here, you can open the**Link to destination Relay** event handler for the **Report Visualization Clicked** event. When a question in Analytics Q&amp;A returns a report, you can trigger this event by clicking a value in the report. When you click a value, you also see a list of the records that contribute to this value. In the **Route** field, you see that the destination is expected to be a page that is based on the Simple List page template. You also see the parameters of the page that the `@payload.*` values correspond to, and that the **Title** field can be populated with `@payload.listTitle`.

|Parameter|@payload.\* value|
|---------|-----------------|
|table \(required\)|@payload.table|
|listTitle|@payload.listTitle|
|query|@payload.query|
|disableInlineEditing|none|

![Destination Relay event handler.](../image/event-handler-link-destination-relay.png)

Next, you navigate to **Menu** &gt; **Create page** and create a page that is based on the Simple List template. Let's say that you name the page as Record list. You then follow a similar process as when you created the Analytics Center page. This time, in the last steps of the process, you would add `table` as a required parameter and `listTitle`, `query`, and `disableInlineEditing` as optional parameters.

![Last page of the create a page wizard.](../image/event-handler-page-parameters.png)

Because this page already contains a List component, when you open the **Config** tab for this component, you see that the parameters are already passed in the `@context.props.*` values.

![Configure tab of the list component.](../image/event-handler-list-config.png)

Now, you return to the Analytics Center page. In the **Report Visualization Clicked** event, you add a new event handler. Next, you select the Record list page that you created and add the `@payload.*` values in the **table**, **listTitle**, and **query** fields, following the information that you got from the **Link to destination Relay** event handler. Predictive typing helps you to fill in these fields.

![Configuring the navigation for a link to the destination event handler.](../image/event-handler-destination.png)

After you click **OK** and add `@payload.listTitle` as the **Title**, the event handler is done. You can now delete the**Link to destination Relay** event handler for this event.

The following example shows an Analytics Center page. On this page, you can enter a query for Incidents by Priority and get a report as a result. Also, by clicking a column, you trigger a **Report Visualization Clicked** event. The event handler enables you to see a simple list of the incidents in the report.

![Analytics Q&A component.](../image/event-handler-complete-example.gif "Triggering the configured Report Visualization Clicked event")

**Parent Topic:**[Bind an event to a data resource](bind-event-data-resource.md)

