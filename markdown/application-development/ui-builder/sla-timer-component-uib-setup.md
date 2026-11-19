---
title: SLA timer component setup
description: The SLA timer component counts down the time remaining on a task Service Level Agreement \(SLA\) and uses a highlighted value to indicate the status of the SLA.Identify the task and configuration records for which your SLA timer is configured with these properties.The SLA timer component doesn't have configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/sla-timer-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# SLA timer component setup

The SLA timer component counts down the time remaining on a task Service Level Agreement \(SLA\) and uses a highlighted value to indicate the status of the SLA.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your SLA timer that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "sla-timer-content-tree.png"\] Alt text: Shows the label of the SLA timer that identifies the it in the content tree

2.  Select the SLA timer component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the SLA timer label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## SLA timer configuration properties

Identify the task and configuration records for which your SLA timer is configured with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_jxh_5qc_ppb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task sys\_id

</td><td>

task

</td><td>

System identifier \(sys\_id\) of the task for which this SLA timer is displayed.

</td></tr><tr><td>

Configuration sys\_id

</td><td>

configuration

</td><td>

System identifier \(sys\_id\) of the configuration record specifying which SLA is shown.

</td></tr><tr><td>

Show Icon

</td><td>

show-icon

</td><td>

Controls whether the clock icon is shown in the timer. Default: **false**

</td></tr></tbody>
</table>## SLA timer component events

The SLA timer component doesn't have configurable events.

