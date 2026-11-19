---
title: Simple List page template configuration
description: Configure the reusable Simple List page template in your experience with different values and behaviors than those provided by default.These properties are available for configuration for the Simple List page template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/simple-list-page-config.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Simple List page template configuration

Configure the reusable Simple List page template in your experience with different values and behaviors than those provided by default.

## Before you begin

You can configure the properties for the this page in the UX Applications \[sys\_ux\_page\_registry\] table.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Navigate to **Next Experience Framework** &gt; **Experiences**.

2.  In the list of UX Applications, select the title of the experience that uses the page template.

3.  Select the UX Page Properties related list to view the properties included with the page template.

    You can select a property to edit or create a new property for your experience.

4.  To create a new page property:

    1.  Navigate to **sys\_ux\_page\_property.list**.
    2.  In the list of page properties, select **New**.
    3.  In the page property record, select an existing page \(UX application title\) for the property.
    4.  Create a unique name for the property and assign it a value.
    5.  Select **Submit**.

        Your new property appears in the UX Page Properties related list in the UX Application record for the page you selected.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Simple list page template properties

These properties are available for configuration for the Simple List page template.

### Properties

-   **actionConfigId**

    System ID of the *sys\_ux\_action\_config* record. Use this property to set the declarative actions that appear in the UI action bar component.

    Data type: string

-   **highlightedValueConfigId**

    System ID of the *sys\_ux\_highlighted\_value\_config* record. Use this property to set the UX Highlighted Value Configurations record into the workspace.

    Data type: string

-   **routeParentTables**

    Comma separated list of parent tables, such as **task** or **kb\_knowledge**. The tables in this property are used to resolve the relationship between parent and child tables during form navigation.

    Data type: string


