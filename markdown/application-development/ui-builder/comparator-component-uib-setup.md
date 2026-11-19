---
title: Comparator component setup
description: The Comparator component enables users to compare content side-by-side by highlighting the differences between the original and changed content. Edit your content and see the highlighted differences between the original and changed content.Configure the compared content and the mode of comparison for the Comparator component.The Comparatorcomponent has no configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/comparator-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Comparator component setup

The Comparator component enables users to compare content side-by-side by highlighting the differences between the original and changed content. Edit your content and see the highlighted differences between the original and changed content.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Comparator that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "comparator-content-tree.png"\] Alt text: Comparator component in content tree with a custom label.

2.  Select the Comparator component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Comparator label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Comparator component properties

Configure the compared content and the mode of comparison for the Comparator component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_vyc_bh3_b4b"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mode

</td><td>

mode

</td><td>

The mode used to compare content. Possible values are the following:-   Diff: Compares the content by highlighting the differences side-by-side.
-   Normal: Displays the content side-by-side without highlighting any differences.
-   Editable: Displays the content side-by-side with the changed content made editable.

</td></tr><tr><td>

Comparison data

</td><td>

comparisonData

</td><td>

The data that is compared between the original and changed content. The compared data is represented as an array of objects. Each object in the array corresponds to one row in the comparison view. For each object, you must specify the following properties:-   Name \(name\): Name of the field that is being compared.
-   Content type \(contentType\): Type of content that is being compared, such as a string or HTML code.
-   Heading \(heading\): Title of the field that is being compared.
-   Original content \(originalContent\): The original content that is shown on the left-side of the comparison view.
-   Changed content \(changedContent\): The changed content that is shown on the right-side of the comparison view.

</td></tr></tbody>
</table>## Comparator component events

The Comparatorcomponent has no configurable events.

