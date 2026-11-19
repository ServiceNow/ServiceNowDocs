---
title: Connect data to your components
description: Bind data exposed by local data resources to components on your UI Builder page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/connect-data.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Connect data components, Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Connect data to your components

Bind data exposed by local data resources to components on your UI Builder page.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Data binding is the process of associating data with a UI element that displays the information. Before binding data to components you must add a data resource to your UI Builder page, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-data-resources.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create or open a page.

4.  Add a data resource to your page.

    For more information, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-data-resources.md).

5.  Add a component to your page.

    You need a component on your page before you can bind a data resource to it. For more information, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-components.md).

6.  Select the **Configure** tab from the configuration panel in UI Builder.

7.  Point to a field that you want to bind data to and select the dynamic data binding icon \(\[Omitted image "uib-dynamic-data-binding-button.png"\] Alt text: Dynamic data binding icon.\).

    \[Omitted image "data-bind-icon-hover.png"\] Alt text: Hovering over the bind data icon.

    The data binding modal appears.

    \[Omitted image "data-bind-modal.png"\] Alt text: Data binding modal showing available data.

8.  Select **Data resource** in the **Data types** tab.

9.  Select the data resource that you want to bind to the component.

    \[Omitted image "data-bind-select-resource.png"\] Alt text: Select a data resource from the list.

10. Select and drag the data you want to bind to the component into the field above.

    You may have to select several pills to get to a specific property value or display value.

    \[Omitted image "data-bind-select-data.png"\] Alt text: Arrow pointing to data bound to a component.

11. Select **Apply**.

    The component displays the property value or display value that you've selected.

    \[Omitted image "data-bind-dot-walk-example.png"\] Alt text: Component text field displays the data bound from the data resource.

12. Select **Save** in the UI Builder header.


**Parent Topic:**[Connect data components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/connect-data-components.md)

