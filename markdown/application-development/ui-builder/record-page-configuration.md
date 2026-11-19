---
title: Record page template configuration
description: Configure the reusable Record page template in your experience with different values and behaviors than those provided by default.These properties are available for configuration for the Record page template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/record-page-configuration.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Record page template configuration

Configure the reusable Record page template in your experience with different values and behaviors than those provided by default.

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

## Record page template properties

These properties are available for configuration for the Record page template.

### Properties

-   **actionConfigId**

    System ID of the *sys\_ux\_action\_config* record. Use this property to set the declarative actions that appear in the UI action bar component.

    Data type: string

-   **featureRoutes**

    Defines how and on which route a feature is being supported in an experience. JSON that maps the feature to the route the feature is supported on, and how the fields and parameters are mapped. If a current experience doesn't have **featureRoutes** defined in its page properties or the requested feature is not listed in the **featureRoutes** property, then **experiencePriorityList** defined under**\_default**, **conditionalExperienceMappings** for that feature in **globalNavigationConfig** is used to resolve the experience and route in the same order of the picked **experiencePriorityList**.

    Data type: string

-   **headerConfigId**

    System ID of the *sys\_ux\_header\_config* record. Use this property to set the UX Header Configurations record into the workspace.

    Data type: string

-   **highlightedValueConfigId**

    System ID of the *sys\_ux\_highlighted\_value\_config* record. Use this property to set the UX Highlighted Value Configurations record into the workspace.

    Data type: string

-   **record\_secondary\_values\_location**

    Uses a value of **header** or **sidebar**. Use this property to determine where the secondary form variables are displayed.

    Data type: string

-   **ribbonConfigId**

    System ID of the *sys\_ux\_ribbon\_config* record. Use this property to set the UX Ribbon Configurations record into the workspace.

    Data type: string

-   **ribbonLocation**

    Uses a value of **header** or **sidebar**. Use this property to determine where the form's ribbon is displayed.

    Data type: string

-   **routeConfigId**

    System ID of the *sys\_ux\_dynamic\_route\_config* record. Use this property to set the UX Dynamic Route Configurations record into the workspace.

    Data type: string

-   **routeParentTables**

    Comma separated list of parent tables, such as **task** or **kb\_knowledge**. The tables in this property are used to resolve the relationship between parent and child tables during form navigation.

    Data type: string

-   **View**

    Name of the view \(*sys\_ui\_view*\) in which to display forms, like workspace. Use this property to set the UI View record for the workspace.

    Data type: string

-   **viewRuleConfigId**

    Name of view rules \(*sys\_ux\_view\_rules\_configuration*\) used to display forms. Use this property to set the UX View Rules Configurations record into the workspace.

    Data type: string


