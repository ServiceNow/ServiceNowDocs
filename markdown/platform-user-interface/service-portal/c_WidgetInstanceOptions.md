---
title: Widget option schema
description: Widget instances allow users to uniquely configure each widget they add to a page. Use the option schema to define the parameters for your widget.Widget instances allow users to uniquely configure each widget they add to a page. Edit the option schema to define basic parameters for your widget.Create a table to store widget instance options instead of editing the existing option schema. When using a table as your widget option schema, you can define custom fields using any ServiceNow field type, add filters to fields, and search or query instance options.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 5
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Widget option schema

Widget instances allow users to uniquely configure each widget they add to a page. Use the option schema to define the parameters for your widget.

## Storing instance options

When developing a widget, you can edit the option schema to create parameters for your widget, or you can create a table to store instance options. If you edit the existing option schema, any instance options defined are stored in JSON format in the **Additional options, JSON format** field in the sp\_instance table. The following field types are available:

-   String
-   Boolean
-   Integer
-   Reference
-   Choice
-   Field\_list \(depends on table\)
-   Field\_name \(depends on table\)
-   Glide\_list

To use other field types not supported in the option schema, create an extension table to store your custom widget option schema. Using a table enables you to:

-   Add any ServiceNow field type, including fields with advanced customization, to the option schema.
-   Define a complex option schema.
-   Search and filter instance options.

**Note:** While storing options in a table enables you to define more complex options, this method is more difficult to maintain than editing the option schema. To avoid creating unnecessary tables and adding additional server calls to your widget, edit the existing option schema when possible. Store options in a table only when complex or searchable options are required.

## Using options in a widget

Access options in the widget from both the client script and the server script using the **options** global variable. You can access any option value in your widget client script or server script using `options.optionName`.

**Client script**

```
function() {
  /* widget controller */
  var c = this;
    console.log(c.options.text_color) //Outputs the text_color option for this instance
}
```

**Server script**

```
(function() {
     $sp.log(options.text_color) //Logs the value of the text_color option to the browser console.
})();
```

## Defining default options

Before an option value is set on an instance, it appears as an undefined value when you access that option variable. Use the widget server script to specify default values for your options.

```
(function() {
  options.text_color=options.text_color||"blue";
  options.maximum_entry_count=options.maximum_entry_count||5;
})
```

**Parent Topic:**[Developing custom widgets](widget-dev-guide.md)

## Edit the widget option schema

Widget instances allow users to uniquely configure each widget they add to a page. Edit the option schema to define basic parameters for your widget.

### Before you begin

You must have cloned or created a new widget.

Role required: admin or sp\_admin

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration** &gt; **Widget Editor**.

2.  Select the widget you want to configure the option schema for.

3.  Click the menu icon \(![Menu icon](../image/MenuIcon.png)\) and select **Edit option schema**.

    This option only appears for users that have the right to edit the widget.

4.  Click **+** to add a widget option.

5.  Define a label, name, type, hint and form section.

    More fields appear depending on the **type** you select.

    Adding flexible widget options allows you to create more reusable widgets. You can add default values to help users understand each widget option. If you do not select a form section, the default is set to **Other options**.

    ![Widget options schema form with fields completed as follows: label=time zone, name=zone, type=string, hint=blank, default value=America/Denver](../image/WidgetOptionsSchemaFields.png)

6.  Click **Save**.

    The option schema you defined is stored in JSON format in the **Option schema** field in the sp\_widget table. Based on this option schema, each instance of the widget can use individually defined instance options.

7.  Test the option schema by adding the widget to a page in the Service Portal Designer.

    1.  Navigate to **Service Portal** &gt; **Service Portal Configuration** &gt; **Service Portal Designer**.

    2.  Add the widget to a page and click the edit icon on the widget instance to view the instance options.

    3.  [Configure the widget instance options](c_ConfigureWidgetInstances.md).

    4.  View the configuration by navigating to the instance record in the sp\_instance table.

        The instance options are stored in JSON format in the **Additional options, JSON format** field.


## Store instance options in a table

Create a table to store widget instance options instead of editing the existing option schema. When using a table as your widget option schema, you can define custom fields using any ServiceNow field type, add filters to fields, and search or query instance options.

### Before you begin

Role required: admin or sp\_admin

### About this task

To define a custom option schema, add fields to an sp\_instance extension table, then set your widget to use the extension table as a data source. Using an extension table enables you to:

-   Add any ServiceNow field type, including fields with advanced customization, to the option schema.
-   Define complex widget options.
-   Search and filter instance options.

**Note:** While storing options in a table enables you to define more complex options, this method is more difficult to maintain than editing the option schema. To avoid creating unnecessary tables and adding additional server calls to your widget, edit the existing option schema when possible. Store options in a table only when complex or searchable options are required.

### Procedure

1.  Create a table that extends an sp\_instance table to store your custom option schema.

    1.  Navigate to **System Definition** &gt; **Tables**.

    2.  Click **New**.

    3.  Define a label and name.

    4.  In the **Extends table** field, select an sp\_instance table that provides the necessary fields.

        |Instance table|Description|
        |--------------|-----------|
        |Instance \[sp\_instance\]|Includes base instance fields.|
        |Instance with Table \[sp\_instance\_table\]|Includes sp\_instance fields and fields to display table data such as Table and Filter.|

    5.  Save the form.

2.  Define custom fields in the extension table.

    You can define any field type to use in your option schema by adding new columns in the **Columns** list.

3.  Update your widget to use the extension table as a data source.

    1.  Navigate to **Service Portal** &gt; **Widgets**.

    2.  Open the widget you would like to create custom options for.

    3.  In the **Data table** field, select your sp\_instance extension table.

        ![Card List Instance extension table selected in the Data table field.](../image/data-table-field.png)

4.  Configure the extension table form to display the desired fields.

    Fields configured on the form are available as instance options.

    1.  Navigate to the extension table form: `<yourInstance>/<your_extenstion_table>.do`.

    2.  Right-click the header menu and select **Configure** &gt; **Form Layout**.

    3.  Add the fields to the form.

    4.  Click **Save**.

5.  Configure the widget to display the desired fields as instance options.

    1.  Navigate to **Service Portal** &gt; **Widgets**.

    2.  Open the widget that has the extension table set as the data source.

    3.  Use the **Fields** slushbucket to select fields to display as instance options.

        ![My Custom Field moved to the Selected column.](../image/custom-option-field.png)

    4.  Save the form.


### What to do next

Test the option schema by adding the widget to a page in the Service Portal Designer. Click the edit icon on the widget instance to view the instance options. After [configuring the widget instance options](c_ConfigureWidgetInstances.md), view the configuration by navigating to the instance record in the sp\_instance extension table.

