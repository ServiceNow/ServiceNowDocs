---
title: Filter condition attributes
description: Use these filter condition attributes to customize how your data is filtered for condition types that are set in your mobile apps.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure a custom filter, Mobile list screen filters, List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Filter condition attributes

Use these filter condition attributes to customize how your data is filtered for condition types that are set in your mobile apps.

**Important:** Make sure that you enter the accepted values for filter condition attributes as shown in the following table. These values are case sensitive. For example, if you want to configure a **Display Type** attribute for a **Date/Time** filter condition type so that a date-time picker appears in the mobile app screen, enter `DateTimePicker` exactly. Be sure to use the same capitalization and add no spaces between the words.

<table id="table_cmr_hjt_pwb"><thead><tr><th>

Filter condition type

</th><th>

Accepted filter condition attribute names

</th><th>

Accepted values \(\* = default setting\)

</th></tr></thead><tbody><tr><td rowspan="4">

Date/Time

</td><td rowspan="2">

Operator

</td><td>

`Between` \*

</td></tr><tr><td>

`On`**Note:** This value is only accepted if the Display Type filter condition attribute is set to `DateTimePicker`.

</td></tr><tr><td rowspan="2">

Display Type

</td><td>

`DateTimeRangePicker` \*

</td></tr><tr><td>

`DateTimePicker`**Note:** This value is only accepted if the Operator filter condition attribute is set to `On`.

</td></tr><tr><td rowspan="4">

Date

</td><td rowspan="2">

Operator

</td><td>

`Between` \*

</td></tr><tr><td>

`On`

</td></tr><tr><td rowspan="2">

Display Type

</td><td>

`DateTimeRangePicker` \*

</td></tr><tr><td>

`DateTimePicker`**Note:** This value is only accepted if the Operator filter condition attribute is set to `On`.

</td></tr><tr><td rowspan="2">

ChoiceList

</td><td>

Operator

</td><td>

`OneOf` \*

</td></tr><tr><td>

Display Type

</td><td>

`ChoiceList` \*

</td></tr><tr><td rowspan="3">

String

</td><td rowspan="2">

Operator

</td><td>

`Contains` \*

</td></tr><tr><td>

`Keywords`

</td></tr><tr><td>

Display Type

</td><td>

`Text` \*

</td></tr><tr><td rowspan="2">

StringUtf8

</td><td>

Operator

</td><td>

`Contains` \*

</td></tr><tr><td>

Display Type

</td><td>

`Text` \*

</td></tr><tr><td rowspan="6">

Integer

</td><td>

Operator

</td><td>

`Between` \*

</td></tr><tr><td rowspan="2">

Display Type

</td><td>

`Box` \*

 This configures a text box in which end users can enter the value on their mobile device screen.

</td></tr><tr><td>

`Slider`

</td></tr><tr><td>

Min

</td><td>

Any positive or negative whole number. For example `2` or `-2`.

</td></tr><tr><td>

Max

</td><td>

Any positive or negative whole number. For example, `15` or `-15`.

</td></tr><tr><td>

SliderStepSize

</td><td>

Any positive whole number. For example, `7`.

</td></tr><tr><td rowspan="2">

Duration

</td><td>

Operator

</td><td>

`Between` \*

</td></tr><tr><td>

Display Type

</td><td>

`DurationPicker` \*

</td></tr><tr><td rowspan="6">

FloatingPoint

</td><td>

Operator

</td><td>

`Between` \*

</td></tr><tr><td rowspan="2">

Display Type

</td><td>

`Box` \*

 This configures a text box in which end users can enter the value on their mobile device screen.

</td></tr><tr><td>

`Slider`

</td></tr><tr><td>

Min

</td><td>

Any positive or negative decimal number that sets the lower value in a range of accepted values. For example, `2.0` or `-2.5` or `.251`.

</td></tr><tr><td>

Max

</td><td>

Any positive or negative decimal number that sets the higher value in a range of accepted values. For example, `15.0` or `-15.8` or `.158`.

</td></tr><tr><td>

SliderStepSize

</td><td>

Any positive decimal number. For example, `7` or `7.3` or `.73`.

</td></tr><tr><td rowspan="6">

Decimal

</td><td>

Operator

</td><td>

`Between` \*

</td></tr><tr><td rowspan="2">

Display Type

</td><td>

`Box` \*

 This configures a text box in which end users can enter the value on their mobile device screen.

</td></tr><tr><td>

`Slider`

</td></tr><tr><td>

Min

</td><td>

Any positive or negative decimal number that sets the lower value in a range of accepted values. For example, `2.0` or `-2.5` or `.251`.

</td></tr><tr><td>

Max

</td><td>

Any positive or negative decimal number that sets the higher value in a range of accepted values. For example, `15.0` or `-15.8` or `.158`

</td></tr><tr><td>

SliderStepSize

</td><td>

Any positive decimal number. For example, `7.0` or `7.3` or `.73`.

</td></tr><tr><td rowspan="6">

Long

</td><td>

Operator

</td><td>

`Between` \*

</td></tr><tr><td rowspan="2">

Display Type

</td><td>

`Box` \*

 This configures a text box in which end users can enter the value on their mobile device screen.

</td></tr><tr><td>

`Slider`

</td></tr><tr><td>

Min

</td><td>

Any positive or negative whole 64-bit number that sets the lower value in a range of accepted values. For example, `2,000,000,000`.

</td></tr><tr><td>

Max

</td><td>

Any positive or negative whole 64-bit number that sets the higher value in a range of accepted values. For example, `1,000,000,000,000,000,000`.

</td></tr><tr><td>

SliderStepSize

</td><td>

Any positive whole 64-bit number. For example, `7,000,000,000`.

</td></tr><tr><td rowspan="3">

Price

</td><td>

Operator

</td><td>

`Between` \*

</td></tr><tr><td rowspan="2">

Display Type

</td><td>

`Box` \*

 This configures a text box in which end users can enter the value on their mobile device screen.

</td></tr><tr><td>

`Slider`

</td></tr><tr><td rowspan="3">

Currency

</td><td>

Operator

</td><td>

`Between` \*

</td></tr><tr><td rowspan="2">

Display Type

</td><td>

`Box` \*

 This configures a text box in which end users can enter the value on their mobile device screen.

</td></tr><tr><td>

`Slider`

</td></tr><tr><td rowspan="2">

ReferenceList

</td><td>

Operator

</td><td>

`OneOf` \*

</td></tr><tr><td>

Display Type

</td><td>

`ReferenceList` \*

</td></tr><tr><td rowspan="2">

Boolean

</td><td>

Operator

</td><td>

`Equals` \*

</td></tr><tr><td>

Display Type

</td><td>

`Boolean` \*

</td></tr></tbody>
</table>