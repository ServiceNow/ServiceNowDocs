---
title: Condition builder component setup
description: Condition builder enables users to create a condition statement of contextually generated fields that can be used to create filters, administer surveys, and control access to records.Configure the Condition builder properties to define what features are available to your end users.Select event handlers to configure the actions \(events\) provided with the Condition builder component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/condition-builder-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Condition builder component setup

Condition builder enables users to create a condition statement of contextually generated fields that can be used to create filters, administer surveys, and control access to records.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Condition builder that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "condition-builder-content-tree.png"\] Alt text: Shows the Condition builder component in the content tree

2.  Select the Condition builder component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Condition builder label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Condition builder component properties

Configure the Condition builder properties to define what features are available to your end users.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_cbh_mg4_htb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table name\[tableName\]

</td><td>

Name of the table the condition builder is using.

</td></tr><tr><td>

Encoded query\[encodedQuery\]

</td><td>

Filter string to use to populate the condition builder.

</td></tr></tbody>
</table><table id="table_dkq_fxg_ttb"><thead><tr><th>

Label \[property\]

</th><th>

Descrtiption

</th></tr></thead><tbody><tr><td>

Hide action bar\[hideActionBar\]

</td><td>

Hide all actions in the condition builder header, including "Use existing filter", "Save filter", "Record count", and "Undo/Redo."Default: **false**

</td></tr><tr><td>

Hide option to use existing filter\[hideLoadFilter\]

</td><td>

Prevent users from accessing saved filters in the condition builder.

</td></tr><tr><td>

Hide option to save filter\[hideSaveFilter\]

</td><td>

Hide the option to save a filter. Saved filters appear in the use existing filter list.Default: **false**

</td></tr><tr><td>

Hide results count\[hideRecordCount\]

</td><td>

Show or hide the record count for results that match the search criteria.Default: **false**

</td></tr></tbody>
</table><table id="table_bxx_gxg_ttb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide filter overview\[hideFilterOverview\]

</td><td>

Show or hide the filter overview that summarizes the condition builder.Default: **false**

</td></tr><tr><td>

Hide editor description\[hideEditorDescription\]

</td><td>

Shows or hides the editor description. Hiding the description provides more vertical space in the condition builder.Default: **false**

</td></tr><tr><td>

Hide dot walking\[hideDotWalking\]

</td><td>

Show or hide dot-walking capabilities to prevent users from being able to filter on related or extended tables.Default: **false**

</td></tr><tr><td>

Hide new condition set option\[hideSets\]

</td><td>

Show or hide the option to enable users to add comparative statements in the way of a new condition set.

</td></tr><tr><td>

Hide the related list conditions section\[hideRelatedListQueryCondition\]

</td><td>

Prevent users from including a relationship with another table in the filter.Default: **false**

</td></tr><tr><td>

Hide "Sort by" section\[hideSortBy\]

</td><td>

Show or hide the "Sort by" feature in condition builder.Default: **false**

</td></tr><tr><td>

Hide "Sort by" description\[hideSortByDescription\]

</td><td>

Show or hide the description that appears after the "Sort by" option.

</td></tr></tbody>
</table><table id="table_wjj_dch_ttb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field inclusion list\[fieldInclusionList\]

</td><td>

An array of fields that appear when using the condition builder.

</td></tr><tr><td>

Field exclusion list\[fieldExclusionList\]

</td><td>

An array of fields that will not be included when using the condition builder. The setting for this field takes precedence over the values contained in the "Field inclusion list."

</td></tr><tr><td>

Hide error information\[hideErrors\]

</td><td>

Shows or hides errors for invalid field, operator, or value inputs within the condition builder.Default: **false**

</td></tr></tbody>
</table>## Condition builder component events

Select event handlers to configure the actions \(events\) provided with the Condition builder component.

The Events tab shows the events used by the Condition builder component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Condition builder actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_agq_rn4_htb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Query updated

</td><td>

The user changes any of the condition blocks in the encoded query Payload:

-   **value**: Value of the encoded query
-   **partial**: Returns true if the query has any partial queries
-   **queryModel**: Specific query model

</td></tr></tbody>
</table>