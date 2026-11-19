---
title: Container component setup
description: The Container component is an empty box into which you can put other components. You can apply an optional layout to a container to split it into multiple parts.The Container component doesn't have any properties that can be configured.The Containercomponent doesn't have any events that can be configured.The Container component has inner and outer layers that work together to keep the components it contains proportioned correctly. The inner layer wraps the contents of the container and isolates their behavior and appearance from the page. The outer layer anchors the component to the rest of the framework and to the page. The CSS properties listed here are used by default with the inner layer to control the children within the container. The remaining CSS properties are used with the outer layer only. This configuration provides the best outcome for most use cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/container-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Container component setup

The Container component is an empty box into which you can put other components. You can apply an optional layout to a container to split it into multiple parts.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Container that differentiates it from other components in the [content tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-tutorial.md).

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Work with pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "container-config-content-tree.png"\] Alt text: Shows the container component in the content tree

2.  Select the Containercomponent, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Container label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Container component properties

The Container component doesn't have any properties that can be configured.

## Container component events

The Containercomponent doesn't have any events that can be configured.

## Container component styles

The Container component has inner and outer layers that work together to keep the components it contains proportioned correctly. The inner layer wraps the contents of the container and isolates their behavior and appearance from the page. The outer layer anchors the component to the rest of the framework and to the page. The CSS properties listed here are used by default with the inner layer to control the children within the container. The remaining CSS properties are used with the outer layer only. This configuration provides the best outcome for most use cases.

**Important:** If you configure the inner layer with CSS properties not on this inclusion list, issues with the proportions of the container contents can occur. If you apply CSS properties to the inner layer that don't appear in the inclusion list and experience a problem, use the advanced editing capabilities in UI Builder to adjust the CSS properties.

1.  Select the Styles tab in the configuration pane of UI Builder.
2.  At the bottom of the tab, select the **View and edit CSS** toggle to enable CSS editing.

    The controls for editing the internal and external layers of Container appear.

    \[Omitted image "container-css-editing.png"\] Alt text: Shows the Styles tab of the container component with controls for editing the CSS of the internal and external layers of the component

3.  Select the layer whose CSS styles you want to edit.

    The CSS editor for that layer appears.

    \[Omitted image "container-css-editor.png"\] Alt text: Shows the CSS editor for the internal container

4.  Make any changes to the CSS you need for your use case and then select **Apply**.

    These CSS properties are intended for use with the inner layer only. It is recommended that you avoid using properties on that layer that are not in this list, unless the appearance of the components in the container is not as expected.

<table id="table_uxm_4lq_btb"><tbody><tr><td>

-   align-content
-   align-items
-   column-gap
-   display
-   flex-direction
-   flex-flow
-   flex-wrap
-   gap
-   grid-auto-columns
-   grid-auto-flow
-   grid-auto-rows
-   grid-column-gap


</td><td>

-   grid-gap
-   grid-row-gap
-   grid-template-areas
-   grid-template-columns
-   grid-template-rows
-   grid-template
-   grid
-   justify-content
-   justify-items
-   margin-bottom
-   margin-left


</td><td>

-   margin-right
-   margin-top
-   margin
-   padding-bottom
-   padding-left
-   padding-right
-   padding-top
-   padding
-   place-content
-   place-items
-   row-gap


</td></tr></tbody>
</table>
