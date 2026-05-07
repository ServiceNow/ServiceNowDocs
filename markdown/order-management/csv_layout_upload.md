---
title: CSV layout upload
description: Learn how to create and upload a CSV file that contains a layout specification.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Set up layouts, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# CSV layout upload

Learn how to create and upload a CSV file that contains a layout specification.

Layouts are defined in a blueprint. When more than one layout is defined for a blueprint, end users rotate through them using the alternate layout button in the upper-right corner of the buyside UI.

Layouts are defined via CSV file that contains all instructions for the layout. For ease of administration, we recommend that admins build their layout in a spreadsheet \(Google Sheets, Microsoft Excel, or similar\) and export to CSV format.

## Creating and editing a layout

Access a layout from its corresponding blueprint administration page.

1.  In the CPQ Admin navigation pane, click **Blueprints** \(2\).
2.  Click the Layouts tab \(3\).
3.  Click the name of the blueprint you want to access.

![CSV layout upload](../images/cpq-csv-layout-upload-layouts-tab.png)

To start a new layout, click **Create Layout**. To edit an existing layout, click the name of a layout in the list.

You can also edit a layout in the Layout Wizard. After you redeploy your blueprint, the new UI changes appear on the buyside.

When you begin a new layout, the New Layout window opens. You can import a CSV file by dropping it in the box or click to select it from your computer. \(i\) You can also download a sample layout file for your reference. \(ii\)

[Sample layout file](https://drive.google.com/file/d/1lzNW_jGkdzdUGwm9rh8xL9BeSxhv3MEJ/view?usp=sharing)

![CSV layout upload](../images/cpq-csv-layout-upload-new-layout.png)

When you edit an existing layout:

Click **Export** to download the current layout file. \(a\)

Import a layout CSV file by clicking **Replace** \(b\).

Click **Save** \(c\) to replace the current layout with the edited layout. If CSV file upload fails, all errors found in the file will be shown to the administrator in an error dialog.

![CSV layout upload](../images/cpq-csv-layout-upload-example-layout.png)

## Using layout CSV file upload

For a thorough introduction to the layout CSV format, view the following 26-minute video:

[Layout CSV Overview](https://drive.google.com/file/d/1htNUPvKa168ZdBF6qXeyIEbTGJljvlyg/view?usp=sharing)

For an example of how a layout CSV is used, view the following 4-minute video:

[HiTech Layout Overview](https://drive.google.com/file/d/1sVs53kC6CBvRRbgqDD12Bq0ofwKI36Rd/view?usp=sharing)

Download the corresponding HiTech Layout CSV file:

[HiTech layout CSV file](https://drive.google.com/file/d/10soQrWkXtQajYb8bce68slzFxgMvmRTX/view?usp=sharing)

## Layout CSV format

Column headings are lower case.

The type column defines the layout components. The following table shows valid values for this column.

|Type value|Description|
|----------|-----------|
|tierDef|Properties: Pages, PagesWithLabels, PagesWithNavigation, ExpandableSection, Tab, TabWithNavigation, VerticalTab, VerticalTabWithNavigation, Accordion, AccordionWithNavigation|
|tier| |
|columnset| |
|image| |
|productlist| |
|productlistcolumn| |
|field| |

The path column value format gives a visual cue to the placement of the element override source label, and is not currently used by the application. Leave it empty.

`label` defines the label to display to the end-user in the UI for tiers and fields.

`variablename` defines a unique identifier for a tier or field.

-   For tiers, administrator should define distinct values.
-   For fields, populate the field variable name.

The component display type column defines how a field should be displayed. The following types are available.

<table id="table_xqt_fyn_bhc"><thead><tr><th>

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

</td></tr><tr><td>

Boolean

</td><td>

Boolean

 Radio

 RadioButtons

</td></tr><tr><td>

Number

</td><td>

Number

 Slider

 NumberWithSubmit

 ReadOnlyText

 ReadOnlyCurrency

 FormattedNumber

</td></tr><tr><td>

Picklist \(single-select\)

</td><td>

Extended picklist

 Extended picklistDisplayOnly

 Picklist

 ReadOnly picklist

 Radio

 RadioButtons

 SingleSelect picklistGrid

 VerticalRadio

 VisualPicker

</td></tr><tr><td>

Picklist \(multi-select\)

</td><td>

MultiSelectExtended picklist

 MultiSelectExtended picklistDisplayOnly

 MultiSelect picklist

 MultiSelect picklistGrid

 MultiSelectVisualPicker

 Checkbox

 VerticalCheckbox

</td></tr></tbody>
</table>`columnorder` is relevant for components in a column set. Used to provide the sort order of the Fields based on screen resolution in the responsive UI.

`classname` is used to reference predefined classes available in CPQ. For example, when placing an image, a class can define the flow of fields around that image. Add these class names to the layout CSV file in the className column. As max-height and grid controls interact with the width of the browser, we recommend you experiment with each class distinctly, exploring how the class responds to a variety of browser sizes.

<table id="table_z23_xkb_nhc"><thead><tr><th>

Effect

</th><th>

Applies to

</th><th>

Supported classes

</th><th>

Notes and examples

</th></tr></thead><tbody><tr><td rowspan="4">

Grid

</td><td rowspan="4">

Fields, Images

</td><td>

topleft1col1row, topleft1col2row ... topleft1col6row

</td><td>

topleft1col1row \{ grid-column: 1/2; \}

 topleft1col2row \{ grid-column: 1/2; grid-row: 1/3; \}

 topleft1col3row \{ grid-column: 1/2; grid-row: 1/4; \}

 topleft1col4row \{ grid-column: 1/2; grid-row: 1/5; \}

 topleft1col5row \{ grid-column: 1/2; grid-row: 1/6; \}

 topleft1col6row \{ grid-column: 1/2; grid-row: 1/6; \}

</td></tr><tr><td>

topleft2col1row, topleft2col2row ... topleft2col6row

</td><td>

topleft2col1row \{ grid-column: 1/3; \}

 topleft2col2row \{ grid-column: 1/3; grid-row: 1/3; \}

 topleft2col3row \{ grid-column: 1/3; grid-row: 1/4; \}

 topleft2col4row \{ grid-column: 1/3; grid-row: 1/5; \}

 topleft2col5row \{ grid-column: 1/3; grid-row: 1/6; \}

 topleft2col6row \{ grid-column: 1/3; grid-row: 1/6; \}

</td></tr><tr><td>

topleft3col1row, topleft3col2row ... topleft3col6row

</td><td>

topleft3col1row \{ grid-column: 1/4; \}

 topleft3col2row \{ grid-column: 1/4; grid-row: 1/3; \}

 topleft3col3row \{ grid-column: 1/4; grid-row: 1/4; \}

 topleft3col4row \{ grid-column: 1/4; grid-row: 1/5; \}

 topleft3col5row \{ grid-column: 1/4; grid-row: 1/6; \}

 topleft3col6row \{ grid-column: 1/4; grid-row: 1/6; \}

</td></tr><tr><td>

topright1col1row, topright1col2row ... topright1col6row

</td><td>

topright1col1row \{ grid-column: -2/-1; \}

 topright1col2row \{ grid-column: -2/-1; grid-row: 1/3; \}

 topright1col3row \{ grid-column: -2/-1; grid-row: 1/4; \}

 topright1col4row \{ grid-column: -2/-1; grid-row: 1/5; \}

 topright1col5row \{ grid-column: -2/-1; grid-row: 1/6; \}

 topright1col6row \{ grid-column: -2/-1; grid-row: 1/6; \}

</td></tr><tr><td>

Height

</td><td>

Fields

</td><td>

mh5, mh10, mh15 ... mh40

</td><td>

Maximum height from 5 rem to 40 rem, in increments of 5

</td></tr><tr><td>

Width

</td><td>

Fields

</td><td>

w5, w10, w15 ... w40

</td><td>

Maximum width from 5 rem to 40 rem, in increments of 5

</td></tr><tr><td>

Grid column width

</td><td>

Fields

</td><td>

lc-15m-15max, lc-15m-20max, lc-15m-25max, lc-15m-30max

</td><td>

These classes set the width of the columns in the layout grid.-   lc: layout column
-   15m: width of 15 rem
-   15max: maximum width of 15 rem

</td></tr><tr><td>

Display vertically, align center

</td><td>

Picklist Fields

</td><td>

vertical-layout, align-center

</td><td>

Default: horizontal \(when layout is vertical, default is left\)

</td></tr><tr><td>

Hide field label, hide field option label

</td><td>

Display components: Extended picklist, MultiSelectExtended picklist

</td><td>

hide-field-label, hide-field-option-label

</td><td>

 

</td></tr></tbody>
</table>The value column contains a JSON string to represent properties for element \(Field or productlistcolumn\) referenced on that row.

`placeholder` allows the Admin to define placeholder text that will display in a text field until the end-user inputs a value.

## Components with images

For picklist display components that include images, when options are disabled, the image is faded. Admins can override this behavior and force the image to look normal by applying the `override-disabled` class to the classname field in the layout.

**Note:** An earlier means of defining and editing layouts using JSON is available. When leveraging JSON, the files must be loaded into the application via REST API. Once a layout has been edited via JSON, CSV manipulation is no longer available. If a layout has been edited via JSON, the Current Layout button is disabled.

**Related topics**  


[Layout Wizard](layout_wizard.md)

[Layout editor](layout_editor.md)

[Configure the Matrix Loader](cpq-using-the-matrix-loader.md)

