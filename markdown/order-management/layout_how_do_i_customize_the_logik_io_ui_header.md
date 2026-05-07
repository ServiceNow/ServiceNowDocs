---
title: Customizing the CPQ UI header
description: Customize the CPQ UI header to reflect your brand with logos, text, and background styles. Configure header elements and buttons—such as Cancel, Reset, Return, and Switch Layout—through the layout CSV file to create a branded, user-friendly configuration experience.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Customizing the CPQ UI header

Customize the CPQ UI header to reflect your brand with logos, text, and background styles. Configure header elements and buttons—such as Cancel, Reset, Return, and Switch Layout—through the layout CSV file to create a branded, user-friendly configuration experience.

![Logo](../images/cpq-layout-logik-header.png)

The CPQ header lets you brand the configuration page with a logo. Essential buttons and actions are also customizable. CSV layout upload supports these features.

## Branding options

The header accommodates text, a logo, or both. If using text, the logo must be relatively narrow, so it fits without overlap.

If you want to remove or replace the blue Salesforce-like background frame, use the backgroundStyle control.

![Logo](../images/cpq-layout-logik-header-1.png)

![Logo](../images/cpq-layout-logik-header-2.png)

All header elements are defined in a header row component, in the values column. Logically, the header component is the first informational row in your CSV file, with the header values definition in cell I2. The following screenshot shows a spreadsheet that is not yet exported to a file.

![CSV file](../images/cpq-layout-logik-header-csv-1.png)

The header value contains instructions for several header elements, so here's a breakdown of common content in that cell:

```
{
"text":"Company/Product Name",
"url":"<image url>",
"backgroundStyle": "url(http://www.some.url/bg.png) transparent no-repeat top center / cover",
"cancelButton": {
	"confirmation": true,
	"label": "Cancel",
	"visible": true
	},
"resetButton": {
	"confirmation": true,
	"label": "Reset",
	"visible": true
	},
"returnButton": {
	"label": "Quote"
	},
"switchLayoutButton": {
	"visible": true
	} 
}
```

As a general guideline, we recommend that administrators include both text and URL keys in the header component row. If the Admin does not intend to leverage either text or URL, they should include the key and an empty value. Examples:

`"text": ""`

The key: value pair above indicates that no text is displayed, where as the pair below leaves the image empty.

`"url": ""`

Customize the background style \(the frame surrounding the configuration pane\) with the following:

`"backgroundStyle": "url(http://www.some.url/bg.png) transparent no-repeat top center / cover"`

Here, `http://www.some.url/bg.png` is the location of a publicly available image. The remaining style instructions are recommended:

Adjust the header definition in your layout spreadsheet. Export to a CSV file and upload to the appropriate blueprint. Navigation:

CPQ Admin -&gt; Blueprints -&gt; \[click appropriate blueprint\] -&gt; Layouts tab -&gt; \[click appropriate layout name\] - Import Layout.

## Button configurations

The CPQ UI offers four buttons: Cancel, Reset, Return, and Switch Layout. Return, commonly labeled Quote, is required. All others are optional.

In the following table, bracketed properties are the default values.

<table id="table_byb_qls_4hc"><thead><tr><th>

Button

</th><th>

Visible

</th><th>

Confirmation

</th><th>

Default Label

</th><th>

Behavior

</th></tr></thead><tbody><tr><td>

Cancel

</td><td>

\[true\], false

</td><td>

\[true\], false

</td><td>

Cancel

</td><td>

When configuring a solution for the first time, Cancel takes the user back to the Product Selection page in Salesforce \(SFDC\).

 When reconfiguring, Cancel returns the user to the SFDC Quote Line Editor \(QLE\) without saving changes.

</td></tr><tr><td>

Reset

</td><td>

true, \[false\]

</td><td>

\[true\], false

</td><td>

Reset

</td><td>

Resets all fields to their initial states so that the user can start over without moving from the page.

</td></tr><tr><td>

Return

</td><td>

N/A

</td><td>

N/A

</td><td>

Quote

</td><td>

Pushes the bill-of-material \(BOM\) into SFDC and returns to the user to the QLE.

</td></tr><tr><td>

Switch Layout

</td><td>

\[true\], false

</td><td>

N/A

</td><td>

N/A

</td><td>

If multiple layouts are defined for this Blueprint, displays the next layout.

</td></tr></tbody>
</table>By default, Cancel, Return/Quote, and Switch Layout buttons display. Cancel and Reset allow the administrator to set a confirmation parameter. When true, a popup requires end users to confirm their intentions, as follows.

![Cancel screen](../images/cpq-layout-logik-header-cancel.png)

All header elements are defined in a header row component, in the values column. Here is a screenshot of the spreadsheet before it is exported in CSV format:

![CSV file](../images/cpq-layout-logik-header-csv-2.png)

The header value contains instructions for several elements. In the graphic below, the parameters relevant to each button definition are separated by green dashed lines:

![Script](../images/cpq-layout-logik-header-dashed-lines.png)

To copy this text to your local clipboard for editing, use the code block in the Branding Options section above.

Adjust the header definition in your layout spreadsheet. Export to a CSV file and upload to the appropriate blueprint. Navigation:

CPQ Admin -&gt; Blueprints -&gt; \[click appropriate blueprint\] -&gt; Layouts tab -&gt; \[click appropriate layout name\] -&gt; Import Layout.

## Currency display

You also use the values column of the header row component of the CSV layout upload file to configure how currency displays in the Shopping Cart. For more information, see [Customizing the currency display in the shopping cart](layout_how_do_i_customize_currency_display_in_shopping_cart.md).

