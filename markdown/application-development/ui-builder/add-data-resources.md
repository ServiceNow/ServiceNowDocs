---
title: Add and configure data resources to a page
description: Add data resources to dynamically expose data from tables, records, or other elements on your page in UI Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/add-data-resources.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add and configure data resources to a page

Add data resources to dynamically expose data from tables, records, or other elements on your page in UI Builder.

## Before you begin

Role required: ui\_builder\_admin

Choose the application containing your data resource. The Global application contains the most common data resources. The data resources relate to Server data, Operations, and Transform. You can add a data resource such as Look Up Records, Table route map, GlideRecord Query, and so on.

## About this task

In the data resource section of UI Builder, you can add and configure local data resource instances for your page. Local data resource instances dynamically expose data to components. If you have any inherited data resources, they are listed in the inherited data resource pane and are read-only. You don’t configure inherited data in UI Builder. Data resources from any application can be added to any page unless restricted by security permissions. You can add multiple local instances of the same data resource, if you need different configurations of the same data resource on your page.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create or open a page.

4.  Add a component to your page.

    You need a component on your page before you can bind a data resource to it.

5.  Select the **+** icon in the data resource drawer.

6.  Select **Data resource**.

7.  Select a data resource to add to your page.

    For example, you could select **Look up a single record**.

8.  Select **Add** to add the data resource to your page.

    The Data Resource configuration modal appears.

    \[Omitted image "data-resource-config-modal.png"\] Alt text: Look up a single record configuration modal.

9.  Fill in the required information for the data resource in the **Configure** tab to expose the data you want.

    The configuration fields vary depending on which Data Resource instance is selected. The **Configure** panel and preview window may display errors when a Data Resource is added to a page. UI Builder attempts to evaluate Data Resources when they’re added to a page. The errors remain until the required Data Resource fields have been filled.

    \[Omitted image "data-resource-config-modal-filled.png"\] Alt text: Look up a single record configuration modal with the Table field set to Task, displaying the corresponding JSON values.

10. Select the default label to provide a custom label and ID value.

    \[Omitted image "data-resource-label.png"\] Alt text: Field to customize the label and ID of a data resource.

    The data resource appears in the data and scripts drawer.

11. Select **Save** in the UI Builder header.


## What to do next

Now that you have a data resource connected to your page, you can bind the data to a component or bind an event to the data resource. For more information, see [Connect data to your components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/connect-data.md) and [Bind an event to a data resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/bind-event-data-resource.md).

**Parent Topic:**[Dynamically expose data in UI Builder pages \(advanced feature\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/data-resources.md)

