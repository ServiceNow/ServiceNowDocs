---
title: Header app shell configuration
description: Configure the Header app shell with different values and behaviors than those provided by default.These properties are available for configuration for the Header app shell.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/header-app-shell-configuration.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Header app shell configuration

Configure the Header app shell with different values and behaviors than those provided by default.

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

## Header app shell properties

These properties are available for configuration for the Header app shell.

### Properties

-   **globalSearchDataConfigId**

    System ID of the **sys\_search\_context\_config** record. This property sets the Search Application Configuration record into the workspace. For more information, see [Search input UIB setup](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/shared-components/sn-search-combobox/uib-setup).

    Data type: string

-   **global\_search\_configurations**

    This property is used to set search configurations in the workspace.

    |Value|Description|
    |-----|-----------|
    |globalSearchViewConfigId|Defines the view, using the system ID of the **sys\_aw\_global\_search\_config** record.|
    |globalSearchRoute|Defines the route \(search\).|

-   **chrome\_header**

    Defines the header configuration.

    Data type: JSON

-   **chrome\_main**

    Main configuration.

    Data type: JSON

-   **chrome\_notification\_uiRoute**

    This property . . .

    Data type: string

-   **chrome\_preferences**

    User preferences for the app shell.

    Data type: JSON

-   **chrome\_tab**

    Tab configuration

    Data type: JSON

-   **chrome\_toolbar**

    Level 1 toolbar configuration.

    Data type: JSON

-   **chrome\_toolbar**

    Level 1 configuration for Analytics Center.

    Data type: JSON


