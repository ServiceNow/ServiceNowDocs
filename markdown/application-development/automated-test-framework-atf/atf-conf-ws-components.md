---
title: Testable Configurable Workspace components
description: Learn about the components and its associated actions in the configurable workspace.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 22
breadcrumb: [Reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Testable Configurable Workspace components

Learn about the components and its associated actions in the configurable workspace.

For more information, see [Testable configurable workspace components](https://horizon.servicenow.com/workspace/components).

## Accordion item

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Check if accordion collapsed|Determines if the accordion is currently collapsed|Boolean|
|Toggle accordion content|Toggles the accordion item's content| |
|Get header text|Expected return value: Returns the header text value in the accordion's item trigger|String|
|Get caption text|Expected return value: Returns the caption text value in the accordion's item trigger|String|

## Action bar

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click action|Clicks an action|N/A|
|Has action|Checks if an action exists|Boolean|

## Activity Stream

<table id="table_cyp_x4x_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Select Option In Filter Set Modal Field

</td><td>

Selects the given option in the given field in the filter set modal

</td><td>

N/A

</td></tr><tr><td>

Apply Filter Set With Name

</td><td>

Applies the filter set with the given name

</td><td>

N/A

</td></tr><tr><td>

Get Journal Tile Content

</td><td>

Returns the content of a journal tile at the given index**Note:** It can contain either HTML or text.

</td><td>

String

</td></tr><tr><td>

Open Filter Set Edit Modal

</td><td>

Opens the edit filter set modal with the given name

</td><td>

N/A

</td></tr><tr><td>

Open Filter Set Modal

</td><td>

Opens the filter set modal

</td><td>

N/A

</td></tr><tr><td>

Set Filter Set Name

</td><td>

Inputs the given value as the new filter set's name

</td><td>

N/A

</td></tr><tr><td>

Create New Filter Set From Existing Selections

</td><td>

Creates a new filter set from the current filter selections

</td><td>

N/A

</td></tr><tr><td>

Select All Options In Filter Set Modal Field

</td><td>

Selects all options in the given field in the filter set modal

</td><td>

N/A

</td></tr><tr><td>

Clear Option In Filter Set Modal Field

</td><td>

Clears the item at the given index in the given field in the filter set modal

</td><td>

String

</td></tr><tr><td>

Get Journal Tile Field Name

</td><td>

Returns the type of a Journal Tile \(work\_notes or comments\) at the given index

</td><td>

String

</td></tr><tr><td>

Get Activity Tile Type

</td><td>

Returns the type of an activity tile displayed in the activity stream

</td><td>

N/A

</td></tr><tr><td>

Click Save Filter Set Button

</td><td>

Clicks the save button in the filter set modal

</td><td>

N/A

</td></tr><tr><td>

Get Filter Set Name

</td><td>

Inputs the given value as the new filter set's name

</td><td>

String

</td></tr><tr><td>

Open Filters

</td><td>

Opens the filter section

</td><td>

N/A

</td></tr><tr><td>

Can Find Filter Set With Name

</td><td>

Expected return-   True: Returns True if a filter set with the given name exists
-   False: Returns False if a filter set with the given name doesn't exists

</td><td>

Boolean

</td></tr><tr><td>

Clear All Options In Filter Set Modal Field

</td><td>

Clears all options in the given field in the filter set modal

</td><td>

N/A

</td></tr></tbody>
</table>## Activity Stream Compose

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Select Field|Selects a compose journal field tab or dropdown menu|Boolean|
|Is Journal Popped Out|Tests if the journal field composition for the given field name is shown as being edited outside of compose|N/A|
|Is Stacked View Enabled|Tests if Stacked View is enabled|Boolean|
|Is Stacked View Available|Tests if Stacked View is available|Boolean|
|Is Email Popped Out|Tests if the email composition is shown as if being edited outside of compose|N/A|
|Check If Tab Selected|Tests if a compose tab is selected|Boolean|
|Set Journal Text|Enters text into the editor of the provided field|N/A|
|Click pop-in button for journal editor|Clicks on the pop in button for journal editor|N/A|
|Select Tab|Selects a compose journal field tab|Boolean|
|Click pop-out button for journal editor|Clicks on the pop out button for journal editor|N/A|
|Click Post Button|Clicks on the editor post button|N/A|
|Click pop-in button for email editor|Clicks on the pop in button for email editor|N/A|
|Get Journal Text|Reads the text in the editor of the provided field|String|
|Is Using Tabs|Tests if the component is using now-tabs to display the fields|N/A|
|Toggle Stacked View|Clicks the Stacked View Toggle|N/A|
|Is Field Selected|Tests if a compose field is selected|N/A|
|Click pop-out button for email editor|Clicks on the pop out button for email editor|N/A|

## Alert

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Check if alert collapsed|Checks if the alert is currently collapsed|Boolean|
|Toggle alert collapse state|Toggles the collapse state of the alert if its collapsible|N/A|
|Check if alert contains action|Determines if the alert has an action button|Boolean|
|Check if alert is collapsible|Checks if the alert can be collapsed|Boolean|
|Click alert button|Clicks the action button for the alert|N/A|
|Get alert title|Retrieves the title of the alert|String|
|Check if the alert text is focusable|Checks if the alert text can be focused|Boolean|

## Avatar

<table id="table_jts_jvr_1fc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Click the avatar

</td><td>

Clicks the avatar.**Note:** The avatar gets clicked only if the interaction mode is being set to a button or a link.

</td><td>

N/A

</td></tr><tr><td>

Get the initials of the avatar

</td><td>

Returns the text value of the avatar if it has initials.

</td><td>

N/A

</td></tr><tr><td>

Check if the avatar has an image

</td><td>

Returns true if the avatar displays an image.

</td><td>

Boolean

</td></tr><tr><td>

Check if the avatar has initials

</td><td>

Returns true if the avatar returns the user initials.

</td><td>

Boolean

</td></tr><tr><td>

Check if the avatar is anonymous

</td><td>

Checks if the avatar doesn't have an image or the user initials.

</td><td>

Boolean

</td></tr></tbody>
</table>## Badge

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Get the badge text|Returns the text content of the badge|String|

## Breadcrumb

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click item|Clicks the matching breadcrumb item|N/A|

## Button

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click|Clicks the button|N/A|
|Get Text|Expected return value: Retrieves the text of the button|String|

## Button bare

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click|Clicks the button|N/A|
|Get Text|Expected return value: Retrieves the text of the button|String|

## Button circular

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click|Clicks the button|N/A|
|Get Text|Expected return value: Retrieves the text of the button|String|

## Button iconic

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click|Clicks the button|N/A|
|Get Text|Expected return value: Retrieves the text of the button|String|

## Button stateful

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click|Clicks the button|N/A|
|Get Text|Expected return value: Retrieves the text of the button|String|

## Card Base Container

<table id="table_jyw_xtn_y2c"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Click

</td><td>

Clicks the card**Note:** This is applicable only for interactive cards.

</td><td>

N/A

</td></tr><tr><td>

is Selected

</td><td>

Expected return-   True: Returns True if the card is currently marked as selected
-   False: Returns False if the card is currently not marked as selected

</td><td>

Boolean

</td></tr></tbody>
</table>## Card Base Header

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Get Caption Text|Expected return value: Retrieves the text of the card caption|String|
|Get Heading Level|Expected return value: Retrieves the heading level|String|
|Get Heading Text|Expected return value: Retrieves the text of the card header|String|
|Get Tagline Text|Expected return value: Retrieves the text of the card tagline|String|

## Checkbox

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click checkbox|Clicks the checkbox|N/A|

## Collapse

<table id="table_uvw_zqn_y2c"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Check if collapse is collapsed

</td><td>

Expected return-   True: Returns True if the collapse is currently not expanded
-   False: Returns False if the collapse is currently expanded

</td><td>

N/A

</td></tr></tbody>
</table>## Color selector

<table id="table_blb_5gq_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Get trigger label

</td><td>

Retrieves the trigger label

</td><td>

String

</td></tr><tr><td>

Open color selector panel

</td><td>

Opens the color selector panel popover

</td><td>

N/A

</td></tr><tr><td>

Check if color selector panel is displayed

</td><td>

Expected return-   True: Returns True if the color selector panel is displayed
-   False: Returns False if the color selector panel is not displayed

</td><td>

Boolean

</td></tr></tbody>
</table>## Custom popover

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click popover trigger|Simulates a click on the slotted trigger element for the popover|N/A|
|Popover panel visibility|Checks if the popover is opened and its panel is visible|Boolean|

## Date-Time

<table id="table_yv2_bvx_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Check if item is disabled

</td><td>

Expected return-   True: Returns True if the matching item in the calendar is disabled
-   False: Returns False if the matching item in the calendar is enabled

</td><td>

Boolean

</td></tr><tr><td>

Set input value

</td><td>

Sets value on native input, includes dispatch of event

</td><td>

N/A

</td></tr><tr><td>

Click Action

</td><td>

Clicks the first matching footer action

</td><td>

N/A

</td></tr><tr><td>

Check if calendar item is focused

</td><td>

Expected return-   True: Returns True if the matching item in the calendar is focused
-   False: Returns False if the matching item in the calendar is not focused

</td><td>

Boolean

</td></tr><tr><td>

Check if calendar panel is displayed

</td><td>

Expected return-   True: Returns True if the calendar panel is displayed
-   False: Returns False if the calendar panel is not displayed

</td><td>

Boolean

</td></tr><tr><td>

Select date item

</td><td>

Selects the matching date item in the calendar

</td><td>

N/A

</td></tr><tr><td>

Click on the input

</td><td>

Clicks on the input of now-date-time and opens the calendar

</td><td>

N/A

</td></tr><tr><td>

Check if item is selected

</td><td>

Expected return-   True: Returns True if the matching item in the calendar is selected
-   False: Returns False if the matching item in the calendar is not selected

</td><td>

Boolean

</td></tr></tbody>
</table>## Date-Time-Interval

<table id="table_ppd_wvx_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Set the end input value

</td><td>

Expected return-   True: Returns True if the matching item in the calendar is disabled
-   False: Returns False if the matching item in the calendar is enabled

</td><td>

N/A

</td></tr><tr><td>

Check if calendar panel is displayed

</td><td>

Sets value on native input, includes dispatch of event

</td><td>

Boolean

</td></tr><tr><td>

Check if item is selected

</td><td>

Clicks the first matching footer action

</td><td>

Boolean

</td></tr><tr><td>

Click the start input

</td><td>

Expected return-   True: Returns True if the matching item in the calendar is focused
-   False: Returns False if the matching item in the calendar is not focused

</td><td>

N/A

</td></tr><tr><td>

Check if calendar item is focused

</td><td>

Expected return-   True: Returns True if the calendar panel is displayed
-   False: Returns False if the calendar panel is not displayed

</td><td>

Boolean

</td></tr><tr><td>

Check if preset is selected

</td><td>

Selects the matching date item in the calendar

</td><td>

Boolean

</td></tr><tr><td>

Check if item is disabled

</td><td>

Clicks on the input of now-date-time and opens the calendar

</td><td>

Boolean

</td></tr><tr><td>

Click Action

</td><td>

Expected return-   True: Returns True if the matching item in the calendar is selected
-   False: Returns False if the matching item in the calendar is not selected

</td><td>

N/A

</td></tr><tr><td>

Click the end input

</td><td>

Clicks on the start input of now-date-time and opens the calendar

</td><td>

N/A

</td></tr><tr><td>

Select a preset

</td><td>

Selects the matching preset item from the preset list

</td><td>

N/A

</td></tr><tr><td>

Select a date item

</td><td>

Selects the matching date item in the calendar

</td><td>

N/A

</td></tr><tr><td>

Set the start input value

</td><td>

Sets start value on native input, include dispatch of events

</td><td>

N/A

</td></tr></tbody>
</table>## Dropdown

<table id="table_gvv_1nr_1fc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Click trigger

</td><td>

Click the dropdown

</td><td>

N/A

</td></tr><tr><td>

Number of selected items

</td><td>

Returns the number of selected items in the dropdown menu

</td><td>

Numeric

</td></tr><tr><td>

Get text

</td><td>

Retrieves the text content of the dropdown menu

</td><td>

String

</td></tr><tr><td>

Check selection

</td><td>

Returns true of the matching item of the menu is selected**Note:** You also need to select a timeframe for the matching item

</td><td>

Boolean

</td></tr><tr><td>

Check panel display

</td><td>

Returns true of the menu is selected

</td><td>

Boolean

</td></tr><tr><td>

Select first matching item

</td><td>

Selects the first matching item in the menu**Note:** You also need to select a timeframe for the matching item

</td><td>

N/A

</td></tr></tbody>
</table>## Flyout Menu

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Check if the flyout menu panel is displayed|Returns true if the flyout menu is opened and the list panel is visible|Boolean|
|Check selection|Returns true if the matching item of the panel is selected|Boolean|
|Click flyout menu trigger|Clicks the slotted trigger element for the flyout menu|N/A|
|Select first matching item|Selects the first matching item found in the panel|N/A|
|Number of selected items|Returns the number of selected items in the flyout menu panel|Numeric|

## Heading

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Get Text|Expected return value: Retrieves the text of the heading|String|

## Highlighted value

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Get the highlighted-value text|Expected return value: Retrieves the text of the highlighted value|String|

## Input

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Set value|Sets value on native input, includes dispatch of event|String|

## Input password

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Set value|Sets value on native input, includes dispatch of event|String|

## Input phone

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Set value|Sets value on native input, includes dispatch of event|String|

## Input URL

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Set value|Sets value on native input, includes dispatch of event|String|

## List

<table id="table_r55_sgw_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Apply filter on the list

</td><td>

Applies filter on the list using encoded query

</td><td>

Boolean

</td></tr><tr><td>

Open a record in the list

</td><td>

Opens a record in the list by clicking on first cell link of record row

</td><td>

Boolean

</td></tr><tr><td>

Validate record visibility in the list

</td><td>

Validates if the record with the given sysid is present in the list

</td><td>

Boolean

</td></tr><tr><td>

Click a list UI action button

</td><td>

Clicks the UI action button with the given sysid

</td><td>

Boolean

</td></tr><tr><td>

Validate the visibility of list's declarative actions

</td><td>

Validates the visibility of declarative action buttonFor example, the **New** button. It is validated based on its sysid.

</td><td>

Boolean

</td></tr></tbody>
</table>## Loader

<table id="table_kjz_dkw_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Click the loader action

</td><td>

Clicks the action associated with the loader

</td><td>

N/A

</td></tr><tr><td>

Get the loader text

</td><td>

Returns the text of the loader

</td><td>

String

</td></tr><tr><td>

Check if loader has action

</td><td>

Expected return-   True: Returns True if the loader has an action defined
-   False: Returns False if the loader doesn't have an action defined

</td><td>

Boolean

</td></tr></tbody>
</table>## Loader Custom

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Get the loader custom text|Returns the text of the loader custom|String|

## Modeless Dialog

<table id="table_emm_tkw_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Click window action

</td><td>

Clicks the matching window action.**Note:** The matcher could correspond to the index of the button within the buttons collection.

</td><td>

N/A

</td></tr><tr><td>

Check if dialog is closed

</td><td>

Expected return-   True: Returns True if the dialog is opened
-   False: Returns False if the dialog is not opened

</td><td>

Boolean

</td></tr><tr><td>

Get the now-modeless-dialog text

</td><td>

Returns the text of the now-modeless dialog

</td><td>

String

</td></tr></tbody>
</table>## now-alert-list

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Toggle alert list collapsed state|Checks if the alert is currently collapsed|N/A|
|Check if alert list can collapse|Toggles the collapse state of the alert if its collapsible|Boolean|
|Dismiss alerts|Determines if the alert has an action button|N/A|
|Check if alert list collapsed|Checks if the alert can be collapsed|Boolean|

## now-card-footer

<table id="table_hvh_5lw_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Get Footer End Text

</td><td>

Returns the text of the card footer's right side**Note:** This is the end part of the footer text

</td><td>

String

</td></tr><tr><td>

Get Footer Text

</td><td>

Returns the text of the card footer

</td><td>

String

</td></tr><tr><td>

Get Footer Start Text

</td><td>

Returns the text of the card footer's left side**Note:** This is the start part of the footer text

</td><td>

String

</td></tr></tbody>
</table>## now-collapse-trigger

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Finish collapse transition|Allows now-collapse to finish transitioning|N/A|

## now-color-selector-panel

<table id="table_gzp_5tw_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Get color name

</td><td>

Returns the name of the color

</td><td>

String

</td></tr><tr><td>

Select color swatch by id

</td><td>

Selects the color swatch from color groups by the color id

</td><td>

N/A

</td></tr><tr><td>

Set hex value

</td><td>

Sets the hex value.**Note:** The valid value is either 3 or 6 hexadecimal characters without \#.

</td><td>

N/A

</td></tr><tr><td>

Set color name

</td><td>

Sets the name of the color in the color name edit input field

</td><td>

N/A

</td></tr><tr><td>

Set slider value

</td><td>

Sets the value of hue slider

</td><td>

N/A

</td></tr><tr><td>

Click action

</td><td>

Clicks the first matching footer action

</td><td>

N/A

</td></tr><tr><td>

Set rgb value

</td><td>

Sets the rgb value

</td><td>

N/A

</td></tr><tr><td>

Set hsl value

</td><td>

Sets the hsl value

</td><td>

N/A

</td></tr></tbody>
</table>## now-date-time-calendar

<table id="table_xph_r5w_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Check if item is disabled

</td><td>

Expected return-   True: Returns True if the matching item in the calendar is disabled
-   False: Returns False if the matching item in the calendar is enabled

</td><td>

Boolean

</td></tr><tr><td>

Check if item is focused

</td><td>

Expected return-   True: Returns True if the matching item in the calendar is focused
-   False: Returns False if the matching item in the calendar is not focused

</td><td>

Boolean

</td></tr><tr><td>

Get active month

</td><td>

Returns a numeric value of the currently selected month

</td><td>

Numeric

</td></tr><tr><td>

Check if item is selected

</td><td>

Expected return-   True: Returns True if the matching item in the calendar is selected
-   False: Returns False if the matching item in the calendar is not selected

</td><td>

Boolean

</td></tr><tr><td>

Get active year

</td><td>

Returns a numeric value of the currently selected year

</td><td>

Numeric

</td></tr><tr><td>

Select date item

</td><td>

Selects the matching date item in the calendar

</td><td>

N/A

</td></tr></tbody>
</table>## now-dropdown-custom-target

<table id="table_w22_tvw_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Check panel display

</td><td>

Expected return-   True: Returns True if the panel is displayed
-   False: Returns False if the if the panel is not displayed

</td><td>

Boolean

</td></tr><tr><td>

Select first matching item

</td><td>

Selects the first matching item found in the panel

</td><td>

N/A

</td></tr><tr><td>

Check selection

</td><td>

Expected return-   True: Returns True if the matching item in the panel is selected
-   False: Returns False if the matching item in the panel is not selected

</td><td>

Boolean

</td></tr><tr><td>

Number of selected items

</td><td>

Returns the number of selected items in the dropdown panel

</td><td>

Numeric

</td></tr></tbody>
</table>## now-dropdown-list

<table id="table_tyy_jww_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Check if item is selected

</td><td>

Checks if the item is selected in the panel

</td><td>

Boolean

</td></tr><tr><td>

Get selected items count

</td><td>

Retrieves the number of items currently selected within the dropdown panel

</td><td>

Numeric

</td></tr><tr><td>

Check panel display

</td><td>

Expected return-   True: Returns True if the panel is displayed
-   False: Returns False if the panel is not displayed

</td><td>

Boolean

</td></tr><tr><td>

Get panel item count

</td><td>

Returns the number of items in the dropdown panel

</td><td>

Numeric

</td></tr><tr><td>

Select first matching item

</td><td>

Selects the first matching item in the panel

</td><td>

N/A

</td></tr></tbody>
</table>## now-flyout-menu-list

<table id="table_h4p_1xw_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Get number of selected items

</td><td>

Returns the number of selected items in the flyout-menu panel

</td><td>

Numeric

</td></tr><tr><td>

Get number of items

</td><td>

Returns the number of items in the flyout-menu panel

</td><td>

Numeric

</td></tr><tr><td>

Check if the flyout menu panel is displayed

</td><td>

Expected return-   True: Returns True if the panel is displayed
-   False: Returns False if the panel is not displayed

</td><td>

Boolean

</td></tr><tr><td>

Select item

</td><td>

Selects the first matching item in the panel

</td><td>

N/A

</td></tr><tr><td>

Check if item is selected

</td><td>

Expected return-   True: Returns True if the matching item in the panel is selected
-   False: Returns False if the matching item in the panel is not selected

</td><td>

Boolean

</td></tr></tbody>
</table>## now-input-date-time

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Set input value|Sets value on native input, includes dispatch of event|N/A|

## now-modal

<table id="table_zxm_szw_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Is Displayed

</td><td>

Expected return-   True: Returns True if the modal is currently displayed
-   False: Returns False if the modal is currently not displayed

</td><td>

Boolean

</td></tr><tr><td>

Get Content

</td><td>

Returns the text of the modal

</td><td>

N/A

</td></tr><tr><td>

Has Footer

</td><td>

Expected return-   True: Returns True if the modal contains a footer
-   False: Returns False if the modal doesn't contain a footer

</td><td>

Boolean

</td></tr><tr><td>

Dismiss

</td><td>

Clicks the dismiss action of the modal

</td><td>

N/A

</td></tr><tr><td>

Get Heading

</td><td>

Returns the heading value of the modal

</td><td>

String

</td></tr><tr><td>

Click Action

</td><td>

Clicks the first matching footer action

</td><td>

N/A

</td></tr></tbody>
</table>## now-record-list-connected

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Apply filter on the list|Applies the filter in the form of encodedQuery|N/A|
|Click a list UI action button|Selects a UI action button in the list|N/A|
|Validate record visibility in the list|Validates if the selected record is visible in the list|Boolean|
|Validate the visibility of list's declarative actions|Validates if the list's declarative action is visible or not|Boolean|
|Open a record in the list|Opens the selected record from the list|N/A|

## now-tabs

<table id="table_us5_f1x_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Select tab by matcher

</td><td>

Selects a tab based on the provided criteria**Note:** It also allows substring matching

</td><td>

N/A

</td></tr><tr><td>

Check if matching tab is selected

</td><td>

Checks if the tab matching the provided criteria is currently selected

</td><td>

Boolean

</td></tr></tbody>
</table>## now-tabs-vertical

<table id="table_kzf_m1x_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Check if matching tab is selected

</td><td>

Checks if the tab matching the provided criteria is currently selected

</td><td>

N/A

</td></tr><tr><td>

Select tab by matcher

</td><td>

Selects a tab based on the provided criteria**Note:** It also allows substring matching

</td><td>

Boolean

</td></tr></tbody>
</table>## now-uxf-tab-set

<table id="table_dxm_bpr_1fc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Assert tab selected by label

</td><td>

Returns true if the tab with the given label is present. An error is shown if the tab is not found.**Note:** You must enter the exact name in the label to check if it exists.

</td><td>

Boolean

</td></tr><tr><td>

Select tab by order

</td><td>

Selects a tab by its order in the tab set. The order starts from 1.**Note:** You must enter the required order of the tab you want to be selected.

</td><td>

N/A

</td></tr><tr><td>

Select tab by label

</td><td>

Selects a tab by its label.**Note:** You must enter the required label of the tab you want to be selected.

</td><td>

N/A

</td></tr></tbody>
</table>## pagination-control

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Get page label|Returns page label|String|
|Check if page selected|Checks if the page matching the provided criteria is currently selected|Boolean|
|Select page size|Selects a page size from the dropdown control|N/A|
|Click go-to-next-page button|Simulates a click on the go-to-next-page button|N/A|
|Set input value|Sets value on input field and dispatches associated events|N/A|
|Click go-to-last-page button|Simulates a click on the go-to-last-page button|N/A|
|Click go-to-previous-page button|Simulates a click on the go-to-previous-page button|N/A|
|Click go-to-first-page button|Simulates a click on the go-to-first-page button|N/A|

## pill

<table id="table_p5t_5kx_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Get the pill text

</td><td>

Returns the text content of the pill

</td><td>

String

</td></tr><tr><td>

Dismiss pill

</td><td>

Clicks the dismiss button of the pill

</td><td>

N/A

</td></tr><tr><td>

Check if pill is dismissible

</td><td>

Expected return-   True: Returns True if the pill is dismissible
-   False: Returns False if the pill is not dismissible

</td><td>

Boolean

</td></tr><tr><td>

Click pill

</td><td>

Clicks the pill

</td><td>

N/A

</td></tr></tbody>
</table>## Radio buttons

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Select a radio button|Clicks the matching radio button, toggling its selected state|N/A|

## Select

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click trigger element|Simulates a click on the trigger element|N/A|
|Check if dropdown displayed|Determines if the dropdown list is currently visible on the screen|Boolean|
|Select matching item|Selects the matching item in the dropdown list|N/A|

## sn-canvas-tabs

<table id="table_xcv_5rr_1fc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Assert tab with label exist

</td><td>

Returns true if the tab with the required label exist

</td><td>

Boolean

</td></tr><tr><td>

Assert tab with label is selected

</td><td>

Returns true if the tab with the required label is selected

</td><td>

Boolean

</td></tr><tr><td>

Close tab by order

</td><td>

Closes the tab by its order in the tab set. The order starts from 1.**Note:** You must enter the required order of the tab you want to be closed.

</td><td>

N/A

</td></tr><tr><td>

Close tab with label

</td><td>

Closes the tab by its label in the tab set.**Note:** You must enter the required label of the tab you want to be closed.

</td><td>

N/A

</td></tr><tr><td>

Select tab by order

</td><td>

Selects a tab by its order in the tab set. The order starts from 1.**Note:** You must enter the required order of the tab you want to be selected.

</td><td>

N/A

</td></tr><tr><td>

Select tab with label

</td><td>

Selects a tab by its label.**Note:** You must enter the required label of the tab you want to be selected.

</td><td>

N/A

</td></tr></tbody>
</table>## sn-canvas-toolbar

<table id="table_rsz_2wn_y2c"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Assert button exists by group and tool tip

</td><td>

Verifies that a button with the given tooltip is present within the group.-   group: top or bottom
-   toolTip:
-   Expected return
    -   True: Returns True if a button with the given tooltip is present within the group
    -   False: Returns False if a button with the given tooltip is not present within the group

</td><td>

Boolean

</td></tr><tr><td>

Assert button selected by group and tool tip

</td><td>

Selects a button with the given tooltip within the group.

</td><td>

Boolean

</td></tr><tr><td>

Select button by group and order

</td><td>

Selects a button within the toolbar group by its ordering. The order starts from 1. Groups can either be top or bottom.

</td><td>

N/A

</td></tr><tr><td>

Select button by group and tool tip

</td><td>

Selects a button within the toolbar group by its toolTip values. The order starts from 1. ToolTip value

</td><td>

N/A

</td></tr></tbody>
</table>## Split button

<table id="table_xbm_xlx_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Is Panel Displayed

</td><td>

Expected return-   True: Returns True if the panel is displayed
-   False: Returns False if the panel is not displayed

</td><td>

Boolean

</td></tr><tr><td>

Is Item Selected

</td><td>

Returns true if the panel's matching item is selectedExpected return-   True: Returns True if the matching item in the panel is selected
-   False: Returns False if the matching item in the panel is not selected

</td><td>

Boolean

</td></tr><tr><td>

Click

</td><td>

Clicks the primary action of the split-button

</td><td>

N/A

</td></tr><tr><td>

Get button text

</td><td>

Returns the text content of the split-button

</td><td>

String

</td></tr><tr><td>

Click Trigger

</td><td>

Clicks the split-button's dropdown trigger

</td><td>

N/A

</td></tr><tr><td>

Select Item

</td><td>

Selects the first matching item found in the panel

</td><td>

N/A

</td></tr><tr><td>

Count Selected Items

</td><td>

Returns the number of selected items in the dropdown panel of the split-button

</td><td>

Numeric

</td></tr></tbody>
</table>## Stepper

<table id="table_l2z_1nx_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Is Step Selected

</td><td>

Expected return-   True: Returns True if the step is currently selected
-   False: Returns False if the step is currently not selected

</td><td>

Boolean

</td></tr><tr><td>

Click next page button

</td><td>

Clicks the next page button

</td><td>

N/A

</td></tr><tr><td>

Click previous page button

</td><td>

Clicks the previous page button

</td><td>

N/A

</td></tr><tr><td>

Select a step

</td><td>

Selects a step

</td><td>

N/A

</td></tr></tbody>
</table>## Tabs

<table id="table_nhz_hnx_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Select tab by order

</td><td>

Selects a tab by its order in the tab set**Note:** The order starts at 1.

</td><td>

Boolean

</td></tr><tr><td>

Select tab by label

</td><td>

Selects a tab by its label**Note:** An error is shown if the tab is not found.

</td><td>

N/A

</td></tr><tr><td>

Assert tab selected by label

</td><td>

Asserts that a tab with the given label is selected.**Note:** An error is shown if the tab is not found.

</td><td>

N/A

</td></tr></tbody>
</table>## Test link

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Get text|Returns the text of the text-link|String|
|Click|Clicks the link|N/A|

## Text area

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Set textarea value|Sets value on native textarea, includes dispatch of events|N/A|

## Toggle

|Actions|Data values and description|Data types|
|-------|---------------------------|----------|
|Click trigger element|Simulates a click on the trigger element|N/A|

## Typeahead

<table id="table_e24_d4x_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Set input value

</td><td>

Sets value on typeahead input and dispatches associated events

</td><td>

N/A

</td></tr><tr><td>

Select item

</td><td>

Selects one of the items of the typeahead

</td><td>

N/A

</td></tr><tr><td>

Click the input

</td><td>

Clicks on the input of the typeahead

</td><td>

N/A

</td></tr><tr><td>

Check if panel is displayed

</td><td>

Expected return-   True: Returns True if the panel is opened and visible
-   False: Returns False if the panel is not opened and visible

</td><td>

Boolean

</td></tr></tbody>
</table>## Typeahead multi

<table id="table_cvj_m4x_zfc"><thead><tr><th>

Actions

</th><th>

Data values and description

</th><th>

Data types

</th></tr></thead><tbody><tr><td>

Select item

</td><td>

Selects one of the items of the typeahead

</td><td>

N/A

</td></tr><tr><td>

Click the input

</td><td>

Clicks on the input of the typeahead

</td><td>

N/A

</td></tr><tr><td>

Check if panel is displayed

</td><td>

Expected return-   True: Returns True if the panel is opened and visible
-   False: Returns False if the panel is not opened and visible

</td><td>

Boolean

</td></tr><tr><td>

Set input value

</td><td>

Sets value on typeahead input and dispatches associated events

</td><td>

N/A

</td></tr></tbody>
</table>-   **[Configurable workspace components examples](../concept/atf-conf-ws-comp-examples.md)**  
To grasp how to interact with configurable workspace components, review these examples.

**Parent Topic:**[Automated Test Framework \(ATF\) reference](../concept/atf-ref-overview.md)

