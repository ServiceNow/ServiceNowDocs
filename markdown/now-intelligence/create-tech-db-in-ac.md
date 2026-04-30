---
title: Create a technical dashboard in UI Builder
description: Follow the Technical Editor option to create a dashboard using UI Builder. In UI Builder, you can use a wider range of features than the inline editor, including scripting and data binding.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Create an advanced dashboard, Create a dashboard in UI Builder]
breadcrumb: [Technical dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Create a technical dashboard in UI Builder

Follow the Technical Editor option to create a dashboard using UI Builder. In UI Builder, you can use a wider range of features than the inline editor, including scripting and data binding.

## Before you begin

Creating dashboards in UI Builder is recommended for developers. For more information, see [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

It isn’t possible to edit the dashboard's details in the Analytics Center when you create a dashboard in the Technical Editor. However, you can share a technical dashboard from the Analytics Center.

**Note:** Data visualizations based on table data are automatically shared with users that you share a dashboard with.

Role required: ui\_builder\_admin

## About this task

The technical editor lets you add any UI Builder component to your dashboard. You can also use all other UI Builder features, such as data resources, client scripts, and data binding of configuration properties. The technical editor creates dashboards in a special workspace named Advanced Dashboards, which is available under My Experiences in the UI Builder.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Select **Create new dashboard**.

3.  Choose **Technical editor**.

    ![Create new technical dashboard modal](../image/tech-editor-create-modal.png)

    **Warning:** Do not try to create dashboards directly in the Advanced Dashboards experience on the UI Builder. Always begin in runtime from the Platform Analytics library. When you begin the technical dashboard in the library, it has an automatic connection to the par\_dashboards table and is listed in the Dashboard overview component.

4.  Provide a name and description of the dashboard you are going to create and select **Create new dashboard**.

    The Technical editor option opens an empty dashboard.

5.  Select **Edit in UI Builder**.

6.  In the Content tree view, add layouts or container components.

    Containers hold dashboard components including data visualizations, static text boxes, and images. If you’re creating a tabbed dashboard, you can create each tab as a container under the parent Tabs component. For more information, see the [Tabs component reference](https://developer.servicenow.com/dev.do#!/reference/next-experience/utah/now-components/now-uxf-tab-set/overview) on the Developer Site.

7.  On the right side of the UI Builder, in the **Styles** tab, choose a layout.

    Layouts organize container content in patterns.

    -   Choose **Grid** to specify the number of rows and columns in the selected container. For more information, see [Using CSS Grid layouts to build a page](https://www.servicenow.com/docs/access?context=css-grid-uib&version=zurich&pubname=zurich-application-development&ft:locale=en-US).
    -   Choose **Flexbox** for more flexibility in the layouts between containers. For more information, see [Using Flexbox layouts in UI Builder](https://www.servicenow.com/docs/access?context=flexbox-uib&version=zurich&pubname=zurich-application-development&ft:locale=en-US).
8.  Add a component to the container.

    Select it from the **Components** menu on the left or click the Add content \(**+**\) icon in the staging area.

    The **Configure** panel on the right enables you to configure the component you’ve chosen.

    ![Component menu in UI Builder.](../../par-for-workspace/image/dashboard-add-component.png)

9.  Add more containers, components, and configurations.

10. If you have added a data visualization component and you want viewers to drill down to a more detailed data view from that component, follow the instructions in [Add a drilldown event to a data visualization on a technical dashboard](add-custom-drilldown-event.md).

11. Click **Save** at any time to save the changes you've made to the dashboard.


**Parent Topic:**[Technical dashboards](../../performance-analytics/concept/technical-dashboards.md)

**Related topics**  


[Data visualizations in Platform Analytics](../../performance-analytics/concept/analytics-center-data-visualizations.md)

[Filters in Platform Analytics](../../par-for-workspace/concept/interactive-filters-workspace.md)

