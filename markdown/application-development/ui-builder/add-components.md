---
title: Add and configure components
description: Learn how to add components to your page in UI Builder. A page is built by adding components.Learn about the various functions supported in the UI Builder component formula editor.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Configure components and repeaters \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add and configure components

Learn how to add components to your page in UI Builder. A page is built by adding components.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Components are the building blocks used to create custom pages in UI Builder. Learn how to add a component to a page. After you add a component to a page, you must configure the component. For more information about configuring components, see [Component documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades) on the ServiceNow Developer Site.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Open or create a page.

    If you open an existing page, make sure you are in the same scope as the original page. If not, change the scope before you start editing the page. Application scoping protects applications by identifying and restricting access to application files and data. Administrators set the scope to specify what parts of an application are accessible to other applications. Application scope protects data and application files. See [Learn about security and roles](security-roles.md) for more information about application scope.

4.  Select an existing container or create a column layout.

    See [Organize components in UI Builder pages](../concept/work-layouts.md) for more information.

5.  Add components to your page.

    UI Builder comes with a library of components to choose from. You add components as the building blocks of your page. For example, you can add a heading, data visualizations, and so on. The following table shows you the different ways you can add a component to a page.

<table id="choicetable_dzv_llh_wnb"><thead><tr><th align="left" id="d274853e196">

To add a component

</th><th align="left" id="d274853e199">

Do the following

</th></tr></thead><tbody><tr><td id="d274853e205">

**Directly from your page**

</td><td>

From your page, select **+** and choose a component from the toolbox. You can search for a component or scroll through the list.![Add content icon selected on the stage showing the toolbox window with Components tab selected.](../image/component-add-from-stage.png)

</td></tr><tr><td id="d274853e225">

**Floating menu above page**

</td><td>

Select the floating menu above your component. -   Select **Add before** or **Add after**.
-   Choose a component from the toolbox.


</td></tr><tr><td id="d274853e251">

**Content tree**

</td><td>

You can add a component from the content tree in the following two ways.-   Select **+Add content** beneath a container in the content tree. Then choose a component from the toolbox.
-   Move your mouse device over a container in the content tree, select the **Menu** icon, and select **Add component**. Then choose a component from the toolbox.
 ![Black arrow pointing to + add content option in content tree next to the toolbox window with Components tab selected.](../image/component-add-from-content-tree.png)

</td></tr></tbody>
</table>6.  Now configure the properties of the components that you just added.

    Configuring components means to customize them to your needs. For more information about configuring components, see [Next Experience Components](https://developer.servicenow.com/dev.do#!/reference/now-experience/rome/components).

    1.  Select the component that you want to configure.

    2.  Select the **Configure** tab from the configuration panel in UI Builder.

    3.  Customize the [component properties](../concept/ui-builder-glossary.md#) for the component.

        For example, you could add a name for a button component. Some components, like data visualizations, require a data source before you can configure the properties. Each component has different configuration properties based on the requirements and options for each component. For example, the **Button** component configuration is simple, while a **List** component requires more configuration.

    4.  For components with configurable JSON properties, you can use UI Builder's low-code JSON editor to edit component properties without needing to edit JSON code.

        The JSON editor UI displays all available properties, even properties not defined in the dummy data or defined values. You can update properties or add your own custom properties within the JSON editor. For more information about configuring components, see [Edit code with the Now Code Editor \(advanced feature\)](../../now-code-editor/concept/now-code-editor.md).

        **Note:** The low-code JSON editor is only available to properties that have a schema and whose JSON input matches said schema.

        The low-code JSON editor supports simple objects, simple array properties, complex arrays, arrays of objects, and partially supports complex objects. For complex arrays, you can add, delete, or move the position of array items. You can also select **Hide unset items** to hide objects with empty or null values for a simplified editing experience.

        ![UI Builder low-code JSON editor.](../image/json-editor.png)

    5.  When working with a container component, you can edit some styles by using the floating panels.

        Select the **Menu** icon to view a menu.

        ![Arrow pointing to the menu icon with the floating menu expanded.](../image/container-more-button.png)

        Select the **Layout**, **Sizing**, or **Spacing** option to open a floating panel with the most common options displayed. Drag the floating panel to another location as needed. Only one floating panel can be open at a time.

        ![Layout options displayed in a floating panel.](../image/container-style-floating-panel.png)

    For more information about configuring components, see [Next Experience Components](https://developer.servicenow.com/dev.do#!/reference/now-experience/rome/components).

7.  Select the **Events** tab to add an event handler to your component.

    Add an event handler to add actions to the components on your page. For example, a button component is static and doesn’t do anything until you bind an event action to it, such as saving a record. Some components don’t have an event action applied to them, such as a heading component. But many components require you to map an event to your component to actually make it perform an action. See [Bind an event to a component](bind-event-component.md) for more information on how to add event handlers to your component.

8.  You can override any styles for a component by adding CSS styling under the **Styles** tab.

    For more information, see [Change the default appearance of components](add-styling-to-component.md#).

    **Note:** Style changes only affect a single component at a time. To change the visual style of all the components in your experience, you must apply a theme to your experience. For more information, see [Manage the visual style of UI Builder experiences](../concept/manage-the-visual-style-of-ui-builder-experiences.md).

9.  Add additional containers to your page to display your components in an organized way.

    For example, one container could have a heading component. Another container below it could include a list component, a button component, and so on.

    1.  Select the **+** at the top of your container to add a container component before the existing component and select the **+** at the bottom of a component to insert a container component after it.

    2.  Drag a container component from the Components list to your existing container on the page; Hold over the top line of the container to insert the new container before the existing container or over the bottom line of the existing container to add it after.

10. Add more components to your page by selecting the **+** on the top or bottom of the components on the page \(the **+** changes to **+ Add**\).

    ![Plus signs at the top and bottom of a component to add additional components.](../image/add-another-component.png)

    1.  Select the **+** at the top of your component to add a component before the existing component or select the **+** at the bottom of a component to insert a component after it.

    2.  Drag a component from the component list to insert the component before or after an existing component.

11. To make a modal appear when you select a component such as a button, you must add the modal to the component first.

    A modal is a confirmation pop-up that appears when you select the component. For example, if you add a button component that deletes a record, you add a modal to ask the user to confirm they want to delete the record. See [Create modals in UI Builder](../concept/Modals-overview.md) for more information.

12. Select **Save** often on your page as you work.

13. View and test your page by selecting the **Preview** button.


## What to do next

You have added and configured components on your page. See [Dynamically expose data in UI Builder pages \(advanced feature\)](../concept/data-resources.md) for more information. A data resource in UI Builder is the data that a page fetches to display content in components. Components use data resources as a way to reuse data and configurations across different experiences, and make the components dynamic on a page.

**Parent Topic:**[Configure components and repeaters \(advanced feature\)](../concept/configure-comp-and-repeaters.md)

## Supported functions in the UI Builder component formula editor

Learn about the various functions supported in the UI Builder component formula editor.

The following table lists the functions you can use in the UI Builder component formula editor. For more information about the component formula editor, see [Customize UI Builder pages using components](../concept/work-components.md).

<table id="table_jb1_r21_ft"><thead><tr><th>

Operator label

</th><th>

Example condition

</th><th>

Equivalent query operator

</th><th>

Example query

</th><th>

Example output

</th></tr></thead><tbody><tr><td>

All empty

</td><td>

\[Short description\]\[ALL\_EMPTY\]

</td><td>

ALL\_EMPTY

</td><td>

short\_descriptionALL\_EMPTY

</td><td>

All records in which there is no value in the **Short description** field.

</td></tr><tr><td>

All equal

</td><td>

\[Short description\]\[ALL\_EQ\]\[Network storage unavailable\]

</td><td>

ALL\_EQ

</td><td>

short\_description=network storage unavailable

</td><td>

All records in which the value for the **Short description** field is equal to "Network storage is unavailable."

</td></tr><tr><td>

All greater than

</td><td>

\[Impact\]\[ALL\_GT\]\[2 - Medium\]

</td><td>

&gt;

</td><td>

impact&gt;2

</td><td>

All records in which the **Impact** field has a value of **3 - Low**

</td></tr><tr><td>

All greater than or equal

</td><td>

\[Impact\]\[ALL\_GTE\]\[2 - Medium\]

</td><td>

&gt;=

</td><td>

impact&gt;=2

</td><td>

All records in which the **Impact** field has a value of **2 - Medium** or **3 - Low**.

</td></tr><tr><td>

All less than

</td><td>

\[Reassignment count\]\[ALL\_LT\]\[2\]

</td><td>

&lt;

</td><td>

reassignment\_count&lt;2

</td><td>

All records in which the value in the **Reassignment count** field is any number less than \(but not equal to\) **2**.

</td></tr><tr><td>

All less than or equal

</td><td>

\[Reassignment count\]\[ALL\_LTE\]\[2\]

</td><td>

&lt;=

</td><td>

reassignment\_count&lt;=2

</td><td>

All records in which the value in the **Reassignment count** field is one of the following:-   a number less than 2
-   2

</td></tr><tr><td>

All not equal to

</td><td>

\[Impact\]\[ALL\_NEQ\]\[1 - High\]

</td><td>

!=

</td><td>

impact!=1

</td><td>

All records in which the value in the **Impact** field is anything but **1 - High**.

</td></tr><tr><td>

All not empty

</td><td>

\[Impact\]\[ALL\_NOTEMPTY\]

</td><td>

ALL\_NOTEMPTY

</td><td>

impactALL\_NOTEMPTY

</td><td>

All records in which the **Impact** field has any value.

</td></tr><tr><td>

All not one of

</td><td>

\[Impact\]\[ALL\_NOTONEOF\]\[1 - High, 2 - Medium\]

</td><td>

ALL\_NOTONEOF

</td><td>

impactALL\_NOTONEOF1,2

</td><td>

All records in which the **Impact** field is populated by anything except the following values:-   **1 - High**
-   **2 - Medium**

</td></tr><tr><td>

All one of

</td><td>

\[Impact\]\[ALL\_ONEOF\]\[1 - High, 2 - Medium\]

</td><td>

ALL\_ONEOF

</td><td>

impactALL\_ONEOF1,2

</td><td>

All records in which the **Impact** field is populated by one of the following values:-   **1 - High**
-   **2 - Medium**

</td></tr><tr><td>

Any empty

</td><td>

\[Short description\]\[ANY\_EMPTY\]

</td><td>

ANY\_EMPTY

</td><td>

short\_descriptionANY\_EMPTY

</td><td>

Any record in which there is no value in the **Short description** field.

</td></tr><tr><td>

Any equal

</td><td>

\[Short description\]\[ANY\_EQ\]\[Network storage unavailable\]

</td><td>

ANY\_EQ

</td><td>

short\_description=network storage unavailable

</td><td>

Any record in which the value for the **Short description** field is equal to "Network storage is unavailable."

</td></tr><tr><td>

Any greater than

</td><td>

\[Impact\]\[ANY\_GT\]\[2 - Medium\]

</td><td>

ANY\_GT

</td><td>

impactANY\_GT2

</td><td>

Any records in which the **Impact** field has a value of **3 - Low**

</td></tr><tr><td>

Any greater than or equal

</td><td>

\[Impact\]\[ANY\_GTE\]\[2 - Medium\]

</td><td>

ANY\_GTE

</td><td>

impactANY\_GTE2

</td><td>

Any record in which the **Impact** field has a value of **2 - Medium** or **3 - Low**.

</td></tr><tr><td>

Any less than

</td><td>

\[Reassignment count\]\[ANY\_LT\]\[2\]

</td><td>

ANY\_LT

</td><td>

reassignment\_countANY\_LT2

</td><td>

Any record in which the value in the **Reassignment count** field is any number less than \(but not equal to\) **2**.

</td></tr><tr><td>

Any less than or equal

</td><td>

\[Reassignment count\]\[ANY\_LTE\]\[2\]

</td><td>

ANY\_LTE

</td><td>

reassignment\_countANY\_LTE2

</td><td>

Any record in which the value in the **Reassignment count** field is one of the following:-   a number less than 2
-   2

</td></tr><tr><td>

Any not equal

</td><td>

\[Impact\]\[ANY\_NEQ\]\[1 - High\]

</td><td>

ANY\_NEQ

</td><td>

impactANY\_NEQ1

</td><td>

Any record in which the value in the **Impact** field is anything but **1 - High**.

</td></tr><tr><td>

Any not empty

</td><td>

\[Impact\]\[ANY\_NOTEMPTY\]

</td><td>

ANY\_NOTEMPTY

</td><td>

impactANY\_NOTEMPTY

</td><td>

Any record in which the **Impact** field has any value.

</td></tr><tr><td>

Any not one of

</td><td>

\[Impact\]\[ANY\_NOTONEOF\]\[1 - High, 2 - Medium\]

</td><td>

ANY\_NOTONEOF

</td><td>

impactANY\_NOTONEOF1,2

</td><td>

Any record in which the **Impact** field is populated by anything except the following values:-   **1 - High**
-   **2 - Medium**

</td></tr><tr><td>

Any one of

</td><td>

\[Impact\]\[ANY\_ONEOF\]\[1 - High, 2 - Medium\]

</td><td>

ANY\_ONEOF

</td><td>

impactANY\_ONEOF1,2

</td><td>

Any record in which the **Impact** field is populated by one of the following values:-   **1 - High**
-   **2 - Medium**

</td></tr><tr><td>

CONCAT

</td><td>

CONCAT\(value\)

</td><td>

CONCAT

</td><td>

CONCAT\("Welcome, ",@context.session.user.firstName\)

</td><td>

Create a new string that combines all supplied strings into one

</td></tr><tr><td>

EMPTY

</td><td>

EMPTY\(value\)

</td><td>

EMPTY

</td><td>

EMPTY\(@context.session.user.roles\)

</td><td>

Returns true if value is null or undefined

</td></tr><tr><td>

IF

</td><td>

IF\(if, then, else\)

</td><td>

IF

</td><td>

IF\(@context.props.bare,"bare page","not bare page"\)

</td><td>

If condition is true, return the value then. If condition is false, return the value else.

</td></tr><tr><td>

LEN

</td><td>

LEN\(list\)

</td><td>

LEN

</td><td>

LEN\(\[1,2,3\]\)

</td><td>

Returns the number of items in the array

</td></tr><tr><td>

Pick

</td><td>

PICK\(array, field\)

</td><td>

Pick

</td><td>

PICK\(@context.session.user.preferences,"name"\)

</td><td>

Creates a new array where each item is picked from field in each item in the array. If the field does not exist, the item in the new array will be EMPTY

</td></tr><tr><td>

Range

</td><td>

RANGE\(from, to\)

</td><td>

Range

</td><td>

RANGE\(1,10\)

</td><td>

Creates an array of numbers, starting with from, up to, incrementing by step

</td></tr><tr><td>

Sum

</td><td>

SUM\(array\)

</td><td>

Sum

</td><td>

SUM\(\[1,2,3\]\)

</td><td>

Starting at 0, add the number value of each item in the array and return the resulting summation

</td></tr><tr><td>

Translate

</td><td>

TRANSLATE\(text\)

</td><td>

Translate

</td><td>

TRANSLATE\("Welcome back"\)

</td><td>

Returns the string from the first argument after the characters specified in the second argument are translated into the characters specified in the third argument.

</td></tr><tr><td>

Where empty

</td><td>

\[Short description\]\[WHERE\_EMPTY\]

</td><td>

WHERE\_EMPTY

</td><td>

short\_descriptionWHERE\_EMPTY

</td><td>

Extract records where there is no value in the **Short description** field.

</td></tr><tr><td>

Where equal

</td><td>

\[Short description\]\[WHERE\_EQ\]\[Network storage unavailable\]

</td><td>

WHERE\_EQ

</td><td>

short\_descriptionWHERE\_EQnetwork storage unavailable

</td><td>

Extract records where the **Short description** field is equal to "Network storage is unavailable."

</td></tr><tr><td>

Where greater than

</td><td>

\[Impact\]\[WHERE\_GT\]\[2 - Medium\]

</td><td>

WHERE\_GT

</td><td>

impactWHERE\_GT2

</td><td>

Extract records where the **Impact** field has a value of **3 - Low**

</td></tr><tr><td>

Where greater than or equal

</td><td>

\[Impact\]\[WHERE\_GTE\]\[2 - Medium\]

</td><td>

WHERE\_GTE

</td><td>

impactWHERE\_GTE2

</td><td>

Extract records where the **Impact** field has a value of **2 - Medium** or **3 - Low**.

</td></tr><tr><td>

Where less than

</td><td>

\[Reassignment count\]\[WHERE\_LT\]\[2\]

</td><td>

WHERE\_LT

</td><td>

reassignment\_countWHERE\_LT2

</td><td>

Extract records where the value in the **Reassignment count** field is any number less than \(but not equal to\) **2**.

</td></tr><tr><td>

Where less than or equal

</td><td>

\[Reassignment count\]\[WHERE\_LTE\]\[2\]

</td><td>

WHERE\_LTE

</td><td>

reassignment\_countWHERE\_LTE2

</td><td>

Extract records where the value in the **Reassignment count** field is one of the following:-   a number less than 2
-   2

</td></tr><tr><td>

Where not equal

</td><td>

\[Impact\]\[WHERE\_NEQ\]\[1 - High\]

</td><td>

WHERE\_NEQ

</td><td>

impactWHERE\_NEQ1

</td><td>

Extract records where the value in the **Impact** field is anything but **1 - High**.

</td></tr><tr><td>

Where not empty

</td><td>

\[Impact\]\[WHERE\_NOTEMPTY\]

</td><td>

WHERE\_NOTEMPTY

</td><td>

impactWHERE\_NOTEMPTY

</td><td>

Extract records where the **Impact** field has any value.

</td></tr><tr><td>

Where not one of

</td><td>

\[Impact\]\[WHERE\_NOTONEOF\]\[1 - High, 2 - Medium\]

</td><td>

WHERE\_NOTONEOF

</td><td>

impactWHERE\_NOTONEOF1,2

</td><td>

Extract records where the **Impact** field is populated by anything except the following values:-   **1 - High**
-   **2 - Medium**

</td></tr><tr><td>

Where one of

</td><td>

\[Impact\]\[WHERE\_ONEOF\]\[1 - High, 2 - Medium\]

</td><td>

WHERE\_ONEOF

</td><td>

impactWHERE\_ONEOF1,2

</td><td>

Extract records where the **Impact** field is populated by one of the following values:-   **1 - High**
-   **2 - Medium**

</td></tr></tbody>
</table>