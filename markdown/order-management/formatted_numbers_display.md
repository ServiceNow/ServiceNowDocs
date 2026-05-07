---
title: Setting the number format of an editable field
description: Learn how to create a user-editable field that maintains a specified format.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Setting the number format of an editable field

Learn how to create a user-editable field that maintains a specified format.

If an Admin wants to display a number field to an end user in a certain format, but also allow users to edit that field, a solution is to set the display type of the field to be a formatted number.

![Number field screen](../images/cpq-formatted-numbers-display-154.png)

Currently, the only way to use number formatting on editable fields is to set this component display type from in the layout CSV itself. Once exported and opened with your preferred CSV editor \(excel in this example\) you can add the following to your fieldʼs row:

-   `FormattedNumber` to column F `(Component display type)`
-   `format: {...}` to column I `(value)`

![Layout CSV](../images/cpq-formatted-numbers-display-155.png)

Once this is saved, you can drag this layout CSV into the layout editor window, and it will replace the current layout. You can check that this change was done from both the Edit Field Info tab of the layout editor, where the display type will be blank:

![Layout CSV](../images/cpq-formatted-numbers-display-156.png)

And from the Arrange Layout Tab, where the field properties of your number field will have your inputted format in the Raw Value section:

![Layout CSV](../images/cpq-formatted-numbers-display-157.png)

![Layout CSV](../images/cpq-formatted-numbers-display-158.png)

After saving and deploying the Blueprint, you should get a similar result to the screenshot at the top of this page. Other formatting options are listed below:

```
{
	"format": {
		"type": "currency" | "percent" | "unit" | "decimal",
		"precision": 2, // Any positive integer
		"unit": Unit, // List of standard JS units, i18n supported
		"customUnit": string, // Any unit to append to the end of the value, untranslated
		"displayZeroPriceAs": string,
		"displayNullPriceAs": string
	}
}
```

Percent formatting automatically multiplies by 100. So a field value of 0.1 will display as 10% .

You can show only a percent sign with no math using `type: unit, unit: percent`.

To view a list of supported units, see [ECMAScript® 2026 Internationalization API Specification](https://tc39.es/ecma402/#table-sanctioned-single-unit-identifiers).

You can use customUnit for units not in this list.

**Parent Topic:**[Using CPQ](cpq-using.md)

