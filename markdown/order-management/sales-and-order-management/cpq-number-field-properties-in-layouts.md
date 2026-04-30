---
title: Number field properties in layouts
description: Control how number fields behave and display in ServiceNow CPQ layouts using the step and precision properties. Define valid input intervals, enforce decimal formatting, and ensure consistent numeric entry for use cases like quantities and currency values.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-09-18"
reading_time_minutes: 2
breadcrumb: [Set up layouts, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Number field properties in layouts

Control how number fields behave and display in ServiceNow CPQ layouts using the step and precision properties. Define valid input intervals, enforce decimal formatting, and ensure consistent numeric entry for use cases like quantities and currency values.

When the input parameters of a number field are defined in the layout editor, either the step property or the precision property can be set.

These properties can conflict and should not be combined.

## The step property

The step property restricts entered values to multiples of the step \(or zero if undefined\). The step must be a whole positive integer, and the UI will truncate \(not round\) an entered value if it contains decimal places beyond that of the step value. A common use case for the step property is to limit inputs to whole numbers.

If the number entered is not a multiple of the step, the setting is not logged immediately, in case the user is entering a value slowly. The value will be reverted to its original value when the user clicks out of the field.

If the number entered is a multiple of the step, an input is logged after a 1-second delay.

Using a rule to set a value that is not a multiple of the step is not recommended. If the user clicks the up or down arrow in the input, the value is changed according to the step value, which may result in an invalid user-entered value.

The following Field Properties dialog illustrates one use of the step property.

![Number field properties in layouts](../images/cpq-step-property-example.png)

## The precision property

The precision property displays the number of decimal places provided, regardless of what is entered. When defined, the field will round \(not truncate\) if decimals are entered beyond the set number of decimal places. \(The complete number is saved on the server.\) A common use case for the precision property is to display currency in dollars and cents, such as 19.99 or 10.00.

The precision property defaults to 0 if not set.

The following Field Properties dialog illustrates one use of the precision property.

![Number field properties in layouts](../images/cpq-precision-property-example.png)

## The Display-Type-Specific Constraints Slider

![Number field properties in layouts](../images/cpq-layout-number-field-props-slider.png)

The step property is required for this component. Minimum and maximum values are included, but precision is not.

## NumberWithSubmit

![Number field properties in layouts](../images/cpq-layout-number-field-props-num-w-submit.png)

The precision property is included and defaults to 0. The step property is not included.

