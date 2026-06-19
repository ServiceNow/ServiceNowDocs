---
title: Connect data to your components with formulas
description: Bind data exposed by local data resources to components with formulas on your UI Builder page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/connect-data-formulas.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Connect data components, Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Connect data to your components with formulas

Bind data exposed by local data resources to components with formulas on your UI Builder page.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Data binding is the process of associating data with a UI element that displays the information. Before binding data to components you must add a data resource to your UI Builder page, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/add-data-resources.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create or open a page.

4.  Add a data resource to your page.

    For more information, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/add-data-resources.md).

5.  Add a component to your page.

    You need a component on your page before you can bind a data resource to it. For more information, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-components.md).

6.  Select the **Configure** tab from the configuration panel in UI Builder.

7.  Point to a field that you want to bind data to and select the dynamic data binding icon \(\[Omitted image "uib-dynamic-data-binding-button.png"\] Alt text: Dynamic data binding icon.\).

    \[Omitted image "data-bind-icon-hover.png"\] Alt text: Hovering over the bind data icon.

    The data binding modal appears.

    \[Omitted image "data-bind-modal.png"\] Alt text: Data binding modal showing available data.

8.  Select the **Formulas** tab.

9.  Select and drag the formula you want to bind to the component into the field above.

    \[Omitted image "data-bind-select-formula.png"\] Alt text: Select a formula from the list.

    For more information about formulas, see [Supported functions in the UI Builder component formula editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/add-components.md).

10. Fill in the fields of the formula.

    \[Omitted image "data-bind-complete-formula.png"\] Alt text: Data bind formula filled out with data from the local data resource.

11. Select **Apply**.

    The component displays the property value or display value that you've selected.

12. Select **Save** in the UI Builder header.


**Parent Topic:**[Connect data components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/connect-data-components.md)

