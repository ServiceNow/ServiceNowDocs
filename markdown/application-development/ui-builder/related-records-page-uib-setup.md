---
title: Related records page template setup
description: Related records is a page template that displays records in the contextual side panel related to the content in the main workspace. These records can be searched and filtered dynamically.Configure the properties for the body of the Related records page, which includes data source information for the records to display.Configure the heading component used in the Related records shared page.Configure the various iconic button components used in the Related records shared page.Configure the input component used in the Related records shared page.Configure the filter dropdown component included in the Related records page.Configure the contents of the data set component used to show records in the Related records shared page.Select event handlers to configure the actions \(events\) provided in the Related records page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/related-records-page-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 16
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Related records page template setup

Related records is a page template that displays records in the contextual side panel related to the content in the main workspace. These records can be searched and filtered dynamically.

Pages are built in UI Builder using a template. For instructions on accessing UIB and selecting the Related records page template, see [Related records shared page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/related-records-shared-page.md).

## How to use the template

When you select the page you want to add, UI Builder asks how you want to use the template for that page.

-   **Use the original template**: References the template in your page. When the template is updated, your page gets the changes automatically. This selection permits limited customizations but is the safest choice.
-   **Copy template contents**: Enables you to change the property values for the components used in the page. If you copy a template, you don't get any of the changes when the template is automatically updated.

## Renaming components

You can rename components in the content tree to suit your use case. For details about editing the content tree, see [UI Builder quick start](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/ui-builder-quick-start.md).

## Page layout

For instructions on overriding the page layout using the Layout panel, see [Layouts in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-layouts.md).

**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## General page properties

Configure the properties for the body of the Related records page, which includes data source information for the records to display.

### Selecting the component in the page

You can open the Config panel for the page template by selecting **Body** from the content tree.

\[Omitted image "related-rec-body-tree.png"\] Alt text: Body of the Related records page selected in the content tree for configuration

### Property definitions

<table id="table_bdm_z14_rpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the table passed into the page and evaluated for related record's context.

</td></tr><tr><td>

sysid

</td><td>

System ID of the table passed into the page.

</td></tr><tr><td>

optionaltable

</td><td>

Optional table name to pass into the page.

</td></tr><tr><td>

optionalSysid

</td><td>

System ID of the optional table passed into the page.

</td></tr><tr><td>

pageSize

</td><td>

Not used in this version of the related record page template.

</td></tr><tr><td>

Label

</td><td>

The heading for the page.

</td></tr><tr><td>

Bare

</td><td>

Enables or disables additional padding around the page.

</td></tr><tr><td>

Scrollable

</td><td>

Enables scrolling of the page content. Choices are: -   Vertical
-   Horizontal
-   Both
-   None

</td></tr><tr><td>

Header Level

</td><td>

Heading level used to generate the header tag. Default: **1**

</td></tr><tr><td>

Intercept Notifications

</td><td>

Sets notifications to be handled by a custom componentDefault: **false**

</td></tr><tr><td>

Propagate Notifications

</td><td>

Determines if a parent page handles notifications. When set to **true**, all events are propagated through the parent page.Default: **false**

</td></tr></tbody>
</table>## Heading component properties

Configure the heading component used in the Related records shared page.

### Selecting the component in the page

Open the Config panel for the heading component using either of these methods:

-   Select **Heading 1** in the content tree.\[Omitted image "related-rec-heading-tree.png"\] Alt text: The heading component selected for configuration in the content tree
-   Select the heading component in the page.\[Omitted image "related-rec-heading.png"\] Alt text: The heading component selected for configuration on the page

### Property definitions

For more information about this component, see [Heading](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/now-components/now-heading/overview).

<table id="table_mm3_stk_qpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Header title.

</td></tr><tr><td>

Level

</td><td>

Defines the HTML heading element used to render the label. Possible choices are H1-H6. Default: **1**

</td></tr><tr><td>

Style

</td><td>

Defines the font and size used to render the heading.Default: **Header-secondary**

</td></tr><tr><td>

Disable text wrap

</td><td>

Prevents the label from wrapping when set to **true**. Label text is truncated if it doesn't fit in the available space. Default: **false**

</td></tr><tr><td>

Hide bottom margin

</td><td>

Removes the bottom margin of the heading when set to **true**.Default: **false**

</td></tr></tbody>
</table>## Iconic button properties

Configure the various iconic button components used in the Related records shared page.

### Selecting the iconic button to configure

You can open the Config panel for an iconic button by selecting the component in the page or in the content tree. You can add additional components in the empty slots where indicated. For more information about this component, see [Button iconic](https://developer.servicenow.com/dev.do#!/reference/now-experience/utah/now-components/now-button-iconic/usage).

The Related records page uses iconic buttons to perform these actions:

|Action|Icon|Content tree selection|
|------|----|----------------------|
|Open a record list|\[Omitted image "related-rec-open-icon.png"\] Alt text: Shows button iconic component in the related records page that creates a new record|\[Omitted image "related-rec-button-iconic-tree.png"\] Alt text: Highlighted name of the iconic button in the content tree that opens a record list|
|Execute a search|\[Omitted image "related-rec-search-icon.png"\] Alt text: Shows button iconic component in the related records page that executes a search|\[Omitted image "related-rec-search-icon-tree.png"\] Alt text: Highlighted name of the iconic button in the content tree that executes a search|
|Open the filter dropdown|\[Omitted image "related-rec-filter-icon.png"\] Alt text: Shows the icon used to trigger the filter dropdownThe default trigger is the sliders icon. To replace this icon select the **Add component** link to choose a different icon. Your choice replaces the default icon and the placeholder. The click behavior and other functionality is automatically maintained for your custom trigger.|\[Omitted image "related-rec-filter-add-trigger.png"\] Alt text: Shows the link for adding a filter trigger in the content tree|
|Create a new record|\[Omitted image "related-rec-add-record-icon.png"\] Alt text: Shows button iconic component in the related records page that adds a record|\[Omitted image "related-rec-add-icon-tree.png"\] Alt text: Highlighted name of the iconic button in the content tree that creates a new record|

### Property definitions

<table id="table_qvw_tll_qpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Icon

</td><td>

Defines the icon displayed in the button.

</td></tr><tr><td>

Variant

</td><td>

Sets the iconic button styles. The selections are **Primary**, **Secondary**, and **Tertiary**.Default: **secondary**

</td></tr><tr><td>

Size

</td><td>

Sets the button size. The choices are **Small**, **Medium**, and **Large**.Default: **Medium**

</td></tr><tr><td>

Bare

</td><td>

Removes the iconic button border and sets the default background to be transparent.Default: **false**

</td></tr><tr><td>

Disabled

</td><td>

Mutes the button color and disables user click interactions when set to **true**.Default: **false**

</td></tr><tr><td>

Padding

</td><td>

Shows or hides the padding around the iconic button. By default, an iconic button's height is based on the **Size** property. Setting the **Padding** property to **Show** reduces the iconic button height. This ensures that the iconic button only takes up the height required by its icon. Buttons with padding included do not align vertically with other button types. This setting is not recommended for iconic buttons that have the `bare` property set to **true**.

</td></tr><tr><td>

High contrast

</td><td>

Sets whether variant colors have higher contrast for visually impaired users. To use high contrast colors, set the **Bare** property to **true**.Default: **false**

</td></tr><tr><td>

Tooltip text

</td><td>

Text content shown inside the tooltip for this iconic button.

</td></tr><tr><td>

ARIA properties

</td><td>

An object whose keys reference a specific HTML element within the iconic button. The value of each key is an object that contains one or more ARIA properties and corresponding values. These ARIA properties are set on specified elements. An example would be: `<divid="saveChanges"tabindex="0"role="button"aria-pressed="false">Save</div>`

For details about ARIA attributes, see [https://www.w3.org/TR/wai-aria-1.1/\#button](https://www.w3.org/TR/wai-aria-1.1/#button).

</td></tr></tbody>
</table>## Input component properties

Configure the input component used in the Related records shared page.

### Selecting the component to configure

You can open the Config panel for the input component using either of these methods:

-   Select **Input 1** in the content tree.\[Omitted image "related-rec-search-input-tree.png"\] Alt text: Shows the input component selected for configuration in the content tree
-   Select the button iconic component in the page.\[Omitted image "related-rec-search-input.png"\] Alt text: Shows the input component selected for configuration on the page

### Property definitions

For more information about this component, see [Input](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/now-components/now-input/overview).

<table id="table_tn1_23m_qpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Type of input for this field. The choices are **Email**, **Ip**, **Number**, or **Text**.Default: **Text**

</td></tr><tr><td>

Label

</td><td>

User visible label for the input field.

</td></tr><tr><td>

Placeholder text

</td><td>

Hint text displayed in the input when the user has not yet entered a value. Placeholder text disappears when the user starts typing.

</td></tr><tr><td>

Identifier

</td><td>

Name of the input field. This name is dispatched with the field value when a user interacts with the field.

</td></tr><tr><td>

Value

</td><td>

The value of the input field. Leave this property empty unless the input field has pre-populated data.

</td></tr><tr><td>

Read only

</td><td>

Controls whether the user can modify the value in this field. Setting this value to **true** prevents user from modifying the value. Default: **false**

</td></tr><tr><td>

Required

</td><td>

Sets the field as a required field. Setting this value to **true**, requires the user to enter a value before submitting the form.

</td></tr><tr><td>

Hide required indicator

</td><td>

Show or hide the required field indicator. Set this property to **true** for forms where most fields are required, together with the **Optional** flag for any fields that are not required.Default: **false**

</td></tr><tr><td>

Optional

</td><td>

Marks the field as an optional field that isn't required to submit the form. Default: **false**

</td></tr><tr><td>

Min. value

</td><td>

Minimum value that a user can enter in the field.

</td></tr><tr><td>

Max. value

</td><td>

Maximum value that a user can enter in the field.

</td></tr><tr><td>

Min. characters

</td><td>

Minimum number of characters that a user can enter in the field.

</td></tr><tr><td>

Max. characters

</td><td>

Maximum number of characters that a user can enter in the field.

</td></tr><tr><td>

Multiple addresses allowed

</td><td>

Enables users to enter multiple addresses of type **Email** in a comma-separated list. Default: **false**

</td></tr><tr><td>

Validation pattern

</td><td>

Regular expression to use to validate user input.

</td></tr><tr><td>

Auto focus

</td><td>

When enabled, puts focus in the input field when the page loads.Default: **false**

</td></tr><tr><td>

Disabled

</td><td>

Disables the input field. The field is dimmed and not accessible to the user.

</td></tr><tr><td>

Invalid

</td><td>

When enabled, indicates that an invalid value was entered in the input field.Default: **false**

</td></tr><tr><td>

Helper content

</td><td>

Defines hint text that is displayed to users in a popover to help them create a query. When helper text is defined, an iconic button appears next to the field label to trigger the popover. Use helper content to display password requirements or other instructions for completing the field.

</td></tr><tr><td>

Alert messages

</td><td>

This property is not intended for use in the related records page, and the value should not be changed. This empty state message is the only message used in the input component: "No content to display. Try modifying your search text or filter to find what you're looking for."

</td></tr></tbody>
</table>## Dropdown filter component properties

Configure the filter dropdown component included in the Related records page.

### Selecting the component in the page

You can open the Config panel for the dropdown component that contains filtering options by selecting **Filters** from the content tree. \[Omitted image "related-rec-filter-tree.png"\] Alt text: Filter component selected in the content tree

### Property definitions

For more information about this component, see [Dropdown](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/now-components/now-dropdown/overview).

<table id="table_sx5_ls1_rpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Variant

</td><td>

Sets the button styles of the dropdown trigger. The choices are: -   **primary**
-   **secondary**
-   **tertiary**

</td></tr><tr><td>

Selection

</td><td>

Determines what happens when the user selects an item from the dropdown. Options include:-   **Single**: \(default\) The panel closes, the trigger label is updated with the label of the selected list item, and the list item is marked as selected.
-   **Multi**: The panel stays open, the trigger label is updated with the selected list item count, and the list item's selected state is toggled on or off.
-   **None**: The panel closes, the trigger label is not updated, and the list item is not marked as selected.

</td></tr><tr><td>

Size

</td><td>

Sets the button size of the dropdown trigger. The choices are: -   **Small**
-   **Medium** \(default\)
-   **Large**

</td></tr><tr><td>

Placeholder text

</td><td>

Placeholder text that displays when no items are selected. If you do not specify a value, especially in the case of iconic dropdowns, provide `tooltipContent` and/or an `aria-label` through the `configAria` property.

</td></tr><tr><td>

Hide selected item

</td><td>

Hides the selected item in the dropdown trigger. Default: **true**

</td></tr><tr><td>

Placerholder icon

</td><td>

Placeholder icon to include in the dropdown trigger. This icon will be replaced by the icon of a selected dropdown item if the item has an icon configured.

</td></tr><tr><td>

Hide container

</td><td>

When set to **true**, makes the dropdown trigger border and background transparent but retains its variant style setting when using an iconic button. If the button is text or text with an icon, only set this property to **true** when the variant is set to **secondary**, **tertiary**, or **inherit**.Default: **false**

</td></tr><tr><td>

Show padding

</td><td>

Includes side padding on bare buttons. By default, bare buttons with labels don't have side padding.Default: **true**

</td></tr><tr><td>

Hide caret

</td><td>

Hides the triangular caret icon used as the default dropdown trigger. Default: **true**

</td></tr><tr><td>

Disabled

</td><td>

When set to **true**, disables the dropdown and prevents the dropdown from opening when the user interacts with it.Default: **false**

</td></tr><tr><td>

Show presence pattern

</td><td>

When set to **true**, displays the dropdown item's presence status icon with a pattern to make it distinguishable by a means other than color.Default: **false**

</td></tr><tr><td>

Items

</td><td>

An array of `DropdownItem` or `DropdownSection` items.

</td></tr><tr><td>

Opened

</td><td>

Automatically updates when the user opens or closes the dropdown. Default: **false**

</td></tr><tr><td>

Panel position

</td><td>

Properties to configure the dropdown panel.Valid keys are:

-   **position**: Array of possible positions in which to place the panel, relative to its target.

Default: `["bottom-start top-start","top-start bottom-start","bottom-end top-end","top-end bottom-end"]`

-   **constrain**: Object specifying size constraints relative to the panel's target.

Default: `{"minHeight":32,"minWidth":"target","maxWidth":400,"maxHeight":300}`

-   **offset**: Number of pixels to offset the panel from the trigger.

</td></tr><tr><td>

Selected items

</td><td>

An array of IDs representing selected dropdown panel items. -   **Multi-select mode NOT enabled**: Each time the user selects a list item, the previously selected ID is replaced with the new ID.
-   **Multi-select mode enabled**: IDs are added to or removed from the list.

</td></tr><tr><td>

ARIA properties

</td><td>

An object whose keys reference a specific HTML element within the dropdown component. The value of each key is an object that contains an ARIA property \(or properties\) and corresponding value. These ARIA properties are set on the specified element. The 'trigger' key corresponds to the inner html `<button>` that acts as the dropdown trigger. See [https://www.w3.org/TR/wai-aria-1.1/\#button](https://www.w3.org/TR/wai-aria-1.1/#button) for properties and accepted values. The 'panel' key corresponds to the inner html `<div>` that acts as the 'listbox'. See [https://www.w3.org/TR/wai-aria-1.1/\#listbox](https://www.w3.org/TR/wai-aria-1.1/#listbox) for properties and accepted values.

</td></tr><tr><td>

Tooltip text

</td><td>

Text shown inside the tooltip.

</td></tr><tr><td>

Active Route

</td><td>

Property inherited from the component that isn't used in this page template.

</td></tr></tbody>
</table>## Data set component properties

Configure the contents of the data set component used to show records in the Related records shared page.

### Selecting the component in the page

You can open the Config panel for the data set component using either of these methods:

-   Select **Data set 1** in the content tree.\[Omitted image "related-rec-data-set-tree.png"\] Alt text: Highlights the name of the component in the content tree that contains the record cards in the Related records page
-   Select the data set container in the page.\[Omitted image "related-rec-data-set.png"\] Alt text: Outlines the data set container for the record cards in the Related records page

### Property definitions

For more information about this component, see [Data set](https://developer.servicenow.com/dev.do#!/reference/now-experience/sandiego/shared-components/now-data-set/overview).

<table id="table_hll_kvs_qpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Sets an optional second title for the data set component.

</td></tr><tr><td>

Data

</td><td>

Data input from the data broker.

</td></tr><tr><td>

Show grid/list toggle

</td><td>

This property is part of the data set component and has no application for the dynamic related records page template. Enabling this property may cause unexpected results.

</td></tr><tr><td>

Default view

</td><td>

Choice of which default view to use: **list** or **grid**.Default: **list**

</td></tr><tr><td>

Card height \(grid view\)

</td><td>

The size of the cards displayed in the grid view. Possible sizes are:-   **Small**
-   **Medium**
-   **Large**

 Default: **sm**

</td></tr><tr><td>

Max. cards per row \(grid view\)

</td><td>

Maximum number of cards to display in a row in the grid view. Possible values are from 1-6. Default: **4**

</td></tr><tr><td>

Min. card width \(grid view\)

</td><td>

Minimum card width of 150 or greater pixels for the grid view.Default: **150**

</td></tr><tr><td>

Databroker State

</td><td>

Tracks the state of the data broker.Default: **false**

</td></tr><tr><td>

Empty state message

</td><td>

Message when there is no card data to display.Default: **No content to display**

</td></tr><tr><td>

Hide filter

</td><td>

This property is not intended for use in the dynamic related records page template, and the value should not be changed. A different filter method is in use.

</td></tr><tr><td>

Hide pagination

</td><td>

This property is not intended for use in the dynamic related records page template, and the value should not be changed. Users find records by scrolling and with the search input component.

</td></tr><tr><td>

Title heading level

</td><td>

The HTML heading level used to render the optional data set title. Possible values are from 1-6.Default: **1**

</td></tr><tr><td>

Title style variant

</td><td>

The style used to render the optional data set title.Default: **header-tertiary**

</td></tr><tr><td>

Declarative action contract

</td><td>

Contains the data needed for dynamic declarative action event mapping.

</td></tr></tbody>
</table>## Events used in the related records page

Select event handlers to configure the actions \(events\) provided in the Related records page.

### Event handlers

Event handlers work with data resources to link the page template actions to the data you want to display to your users. Expand an event in the list and add one or more event handlers. For information about handlers, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Body events

These events are triggered at the top level of the page.\[Omitted image "related-rec-body-events.png"\] Alt text: Events for the body of the Related records page template

|Event|Description|
|-----|-----------|
|Data Set Navigation|User selects a card in the data set component to navigate to that record.|
|Page ready|Event inherited from the page. It's not necessary to listen to or propagate this event.|
|Page property changed|Event inherited from the page. It's not necessary to listen to or propagate this event.|
|Page viewport load completed|Event inherited from the page. It's not necessary to listen to or propagate this event.|

### Heading events

The heading component doesn't have configurable events.

### Button iconic events

\[Omitted image "related-rec-button-iconic-events.png"\] Alt text: Shows events list for iconic buttons in the Related records page

|Event|Description|
|-----|-----------|
|Button iconic clicked|User selects the iconic button.|

### Input events

\[Omitted image "related-rec-search-input-events.png"\] Alt text: Displays the events for the search input component in the Related recordspage template

<table id="table_vxy_t2g_rpb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input invalid set

</td><td>

The user moves focus away from the input field. The event contains these properties:-   Value of the **name** property.
-   Value of the **invalid** property, which is based on the values of the **required** and **pattern** properties.
-   Value entered in the field.
-   Value of the **type** property

</td></tr><tr><td>

Input value set

</td><td>

The user moves focus away from the field, and the value is valid. The event contains these properties:-   Value of the **name** property.
-   Value entered in the field.

</td></tr><tr><td>

Input input

</td><td>

The user enters data in the field by typing or pasting text. The system does not validate the value or update the **value** property. The event contains these properties:-   Value of the **name** property.
-   Value entered in the field that caused the event to occur.
-   Current value of the field when the event occurred.

</td></tr></tbody>
</table>### Filter events

\[Omitted image "related-rec-filter-events.png"\] Alt text: Shows events list for the filter dropdown in the Related records page

<table id="table_jtt_yqb_rpb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dropdown opened set

</td><td>

The user opens or closes the dropdown list.

</td></tr><tr><td>

Dropdown selected items set

</td><td>

The user changes the selection of items in the dropdown list. The event contains these keys:-   **value**: An array containing either a single ID or multiple IDs of the selected items.
-   **items**: An array of objects of the item or items selected from the dropdown list.

</td></tr><tr><td>

Dropdown item clicked

</td><td>

The user selects a dropdown item. The event contains a reference to the clicked item.

</td></tr></tbody>
</table>### Data set events

\[Omitted image "related-rec-data-set-events.png"\] Alt text: Shows events list for the data set component in the Related records page

<table id="table_ptl_2bg_rpb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NOW\_DATA\_SET\_PAGINATION\_BUTTON\_CLICKED

</td><td>

The user selects the pagination button. The event contains this information:-   Context information to send to the data broker.
-   Page number of the data displayed.
-   Size of the content displayed \(items per page\).
-   Type of pagination button selected \(previous or next\).

</td></tr><tr><td>

NOW\_DATA\_SET\_FILTER\_ITEM\_CLICKED

</td><td>

The user selects an item in the filter dropdown. The event contains this information:-   Sys ID of the item selected.
-   Name of the option selected from the filter dropdown.

</td></tr><tr><td>

NOW\_DATA\_SET\_ACTION\_SUCCEEDED

</td><td>

Dispatched with information about a component level action when that action is successful. The event contains this information: -   Details of the action that invoked the server-side update.
-   Details of the model on which the server-side update was invoked.
-   Metadata from the declarative action success script.
-   Payload information from the declarative action success script.

</td></tr><tr><td>

NOW\_DATA\_SET\_ACTION\_FAILED

</td><td>

Dispatched with information about a component level action when that action fails. The event contains this information:-   Details of the action that invoked the server-side update.
-   Details of the model on which the server-side update was invoked.
-   Metadata from the declarative action failed script.
-   Payload information from the declarative action success script.

</td></tr></tbody>
</table>