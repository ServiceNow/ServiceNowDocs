---
title: Field type display options
description: Field type display options
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/field-type-display-options.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure fields, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Field type display options

Field type display options

Users have many display options for the different field types. These are defined in the layout CSV in the Component Display Type column using the values in the parentheses for each type.

The admin uses the Component Display Type column to define how a field will display on a layout. The following types are available.

<table id="table_nn4_zhl_jhc"><thead><tr><th>

Field type

</th><th>

Component display types

</th></tr></thead><tbody><tr><td>

Text

</td><td>

ReadOnlyText

 Text

 TextArea

 Date

 LocationLookup

</td></tr><tr><td>

Boolean

</td><td>

Boolean

 Radio

 RadioButtons

 Checkbox

</td></tr><tr><td>

Number

</td><td>

Number

 NumberWithSubmit

 Slider

 ReadOnlyText

 ReadOnlyCurrency

 FormattedNumber

</td></tr><tr><td>

Picklist \(single-select\)

</td><td>

Picklist

 ReadOnlyPicklist

 ExtendedPicklist

 ExtendedPicklistDisplayOnly

 Radio

 RadioButtons

 VerticalRadio

 SingleSelectPicklistGrid

 VisualPicker

</td></tr><tr><td>

Picklist \(multi-select\)

</td><td>

MultiSelectPicklist

 MultiSelectExtendedPicklist

 MultiSelectExtendedPicklistDisplayOnly

 MultiSelectPicklistGrid

 MultiSelectVisualPicker

 Checkbox

 VerticalCheckbox

</td></tr><tr><td>

Product picker

</td><td>

ProductPickerGrid

 VisualProductPicker

</td></tr></tbody>
</table>## Text component display type

Text fields accept a maximum of 2000 entered characters. Administrators can specify minimum and maximum field lengths and a static default value. Text fields can have the following component display types.

Text: A single-line input. Examples demonstrate unpopulated and populated text fields because they are displayed on to the end user.

\[Omitted image "cpq-fields-text-examples-111.png"\] Alt text: Single-line input

TextArea: A multi-line input field. The example shows a text area with force-set values populated.

\[Omitted image "cpq-fields-text-area-examples-112.png"\] Alt text: Sample output

ReadOnlyText: A display-only option. The example shows a text area with a heading and the displayed field details.

\[Omitted image "cpq-fields-read-only-text-113.png"\] Alt text: Readonly text value

Date: A single-line input and searchable calendar option. Users can enter a date or search by using the calendar icon.

\[Omitted image "cpq-fields-date-114.png"\] Alt text: Date

LocationLookup: uses the Google Places API to pull address data that can be used for unique location configuration and pricing.

\[Omitted image "cpq-fields-location-lookup-115.png"\] Alt text: Location lookup

## Boolean component display type

Boolean fields only accept two values: True and False. False is the default state. Administrators can specify labels for each state. Unless specified, the default label for True is Enabled, and the default label for False is Disabled.

Boolean: Displays as a switch.

\[Omitted image "cpq-fields-boolean-122.png"\] Alt text: Booolean component

Radio: Displays as square radio buttons.

\[Omitted image "cpq-fields-radio-123.png"\] Alt text: Radio button

RadioButtons: Displays as circular radio buttons.

\[Omitted image "cpq-fields-radio-buttons-124.png"\] Alt text: Radio button

Checkbox: Displays either checked or unchecked.

\[Omitted image "cpq-fields-checkbox-126.png"\] Alt text: Boolean check box

## Number component display type

Numbers fields accept only numeric characters. Administrator must specify whether the field will be used as a number, as currency, or as a percentage. Optional settings include minimum, maximum, and default values. The unit label setting is not used in the application.

Number: Users can enter a number using the keyboard or modify it by using the up and down buttons.

\[Omitted image "cpq-fields-number-116.png"\] Alt text: Target number

NumberWithSubmit: Users enter the number by using the keyboard and must click the "Apply" button before their input is accepted.

\[Omitted image "cpq-fields-number-with-submit-118.png"\] Alt text: Demo fields number

Slider: Users slide through range of available numbers. This field appears only if the field definition has a maximum value.

\[Omitted image "cpq-fields-number-slider-119.png"\] Alt text: Target number

ReadOnlyText and ReadOnlyCurrency: Display-only options, similar to ReadOnlyText for text fields. ReadOnlyCurrency is a display-only option with currency formatting.

\[Omitted image "cpq-fields-read-only-currency-120.png"\] Alt text: Number field test

FormattedNumber: Users can enter a number by using the keyboard or modify it by using the up and down buttons. When the field loses focus, it displays in the format defined in the layout CSV.

\[Omitted image "cpq-fields-formatted-number-121.png"\] Alt text: General fields screen

## Picklist component display type \(single-select\)

Picklists allow only specified options to be selected. Administrator must specify whether the field is single-select or multi-select, and if it is single-select, whether the values should be evaluated as a text fields or a number fields. The administrator can also add field options, set the order, specify a default value, and add picklist extension data.

Picklist:

\[Omitted image "cpq-fields-picklist-131.png"\] Alt text: Picklist option

ReadOnlyPicklist: selection only: the user cannot type and filter options.

\[Omitted image "cpq-fields-picklist-read-only-132.png"\] Alt text: CSV file

Radio: Displays all options in a square label display, making all options visible without the use of a menu.

\[Omitted image "cpq-fields-picklist-radio-130.png"\] Alt text: Radio button

RadioButtons:

\[Omitted image "cpq-fields-picklist-single-select-128.png"\] Alt text: Picklist display

VerticalRadio: Options appear as vertical radio buttons.

\[Omitted image "cpq-fields-picklist-vertical-radio-129.png"\] Alt text: Picklist options

Visual Picker: Displays the fieldʼs options using an associated image with a label below the image. Currently selected options are highlighted with a checkmark.

\[Omitted image "cpq-fields-picklist-visual-133.png"\] Alt text: Visual picker

## Picklist component display type \(multi-select\)

Checkbox: Displays options in row format with checkbox selection. multi-select picklists only.

\[Omitted image "cpq-fields-multi-select-checkbox-134.png"\] Alt text: Checkbox options

Vertical Checkbox: displays checkbox selection in vertical alignment. multi-select picklists only.

\[Omitted image "cpq-fields-multi-select-checkbox-vertical-checkbox-135.png"\] Alt text: check box options

ReadOnlyPicklist: \(same as single-select\)

MultiSelectPicklist:

\[Omitted image "cpq-fields-multi-select-picklist-1-136.png"\] Alt text: Picklist options

\[Omitted image "cpq-fields-multi-select-picklist-2-137.png"\] Alt text: Options

## Picklist extension \(PLE\)

ExtendedPicklist and MultiSelectExtendedPicklist: Includes additional details from the PLE and lets users choose from a menu. The example shows that this single-select extended picklist displays details from two columns from the associated PLE. Images can be added to field options.

\[Omitted image "cpq-fields-picklist-extension-1-138.png"\] Alt text: Extended picklist

ExtendedPicklistDisplayOnly, MultiSelectExtendedPicklistDisplayOnly: Includes additional details from the PLE and displays the selection. Options are determined by rule and default options. Not user editable.

\[Omitted image "cpq-fields-picklist-extension-2-139.png"\] Alt text: Extended picklist

SingleSelectPicklistGrid, MultiSelectPicklistGrid, andSingleSelectPicklistGridCheckbox: Includes additional details from the PLE and displays field options in a grid. The Checkbox version lets the end user deselect their option.

\[Omitted image "cpq-fields-picklist-extension-3-140.png"\] Alt text: CXV file

## Product picker component display type

Product pickers are similar to a picklists with extended data. Product pickers can add products to a bill of materials and map additional data to product list fields, including extended data, without writing standard rules.

ProductPickerGrid: Shows the product picker and its subfields in a grid format, much like a picklist extension.

\[Omitted image "cpq-fields-product-picker-grid.png"\] Alt text: Picklistcomponent

VisualProductPicker: Shows the product picker and its subfields as a Visual Picker.

\[Omitted image "cpq-fields-product-picker-visual.png"\] Alt text: Visual picker

**Related topics**  


[Configure fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/fields_101.md)

