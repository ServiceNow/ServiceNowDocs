---
title: Activity timer component setup
description: The Activity timer component tracks the time a user spends on an activity, such as working on a record, and creates time log entries for reporting.Configure the properties for Activity timer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/activity-timer-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Activity timer component setup

The Activity timer component tracks the time a user spends on an activity, such as working on a record, and creates time log entries for reporting.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Activity timer that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). \[Omitted image "activity-timer-content-tree.png"\] Alt text: Activity timer in the UI Builder content tree.

2.  Select the Activity timer component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "activity-timer-config-panel.png"\] Alt text: Activity timer in the UI Builder configuration panel.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Activity timer component properties

Configure the properties for Activity timer.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table\[table\]

</td><td>

The table to track for logging time.

</td></tr><tr><td>

SysId\[sysId\]

</td><td>

Unique ID for the record to track in the selected table.

</td></tr><tr><td>

User\[user\]

</td><td>

Identifies the user whose activity the timer tracks.

</td></tr><tr><td>

Toggle Timer\[toggleTimer\]

</td><td>

Starts or stops the timer when the value changes.Default: **False**

</td></tr><tr><td>

Source\[source\]

</td><td>

An optional string that identifies the context in which the timer was triggered. Use this property to distinguish timer instances across different views in your experience.

</td></tr><tr><td>

Attributes\[attributes\]

</td><td>

Optional JSON object for passing custom metadata to the timer. The component stores these attributes with each timer record and returns them in the timer response.

</td></tr></tbody>
</table>