---
title: Link Set component setup
description: The Link Set component provides web links to users so they can navigate to relevant resources.Configure the labels, links, and dimensions of your Link SetThe Link Set component has no configurable actions \(events\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/link-set-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Link Set component setup

The Link Set component provides web links to users so they can navigate to relevant resources.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Link Set that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "link-set-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Link Set component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Link Set label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Link Set component properties

Configure the labels, links, and dimensions of your Link Set

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_yxb_3xn_mnb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Heading

</td><td>

heading

</td><td>

Text to introduce the link set. You configure this text by updating the JSON. For more information on the JSON properties, see [Link Set API](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/shared-components/now-link-set/api).

</td></tr><tr><td>

Links

</td><td>

links

</td><td>

Links to display in the link set. You configure the links by updating the JSON. For more information on the JSON properties, see [Link Set API](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/shared-components/now-link-set/api).

</td></tr><tr><td>

Indent links

</td><td>

indentLinks

</td><td>

Option to indent the links.

</td></tr><tr><td>

Browse link

</td><td>

browseLink

</td><td>

Link to send users to when they click **Browse all**. You configure this link by updating the JSON. For more information on the JSON properties, see [Link Set API](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/shared-components/now-link-set/api).

</td></tr><tr><td>

Minimum width

</td><td>

minWidth

</td><td>

Minimum width, in pixels, of the link set component. If a user condenses the page in their system browser, the component can't condense any smaller than this width. By default, the minimum width is 150 pixels.

</td></tr><tr><td>

Width

</td><td>

width

</td><td>

Default width, in pixels, of the link set component on the page. By default, the width is 300 pixels.

</td></tr><tr><td>

Size

</td><td>

size

</td><td>

Size of the link set component. You can select **Medium** or **Large**.

</td></tr><tr><td>

Variant

</td><td>

variant

</td><td>

Color scheme to apply to the text of the link set.

</td></tr></tbody>
</table>## Link Set component events

The Link Set component has no configurable actions \(events\).

