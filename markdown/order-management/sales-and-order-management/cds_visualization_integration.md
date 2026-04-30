---
title: Integrating CDS or other third-party visualization tools
description: Integrate CDS Visual or other third-party tools for technical visualization. Sync configuration inputs with visual updates to enhance user experience.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 6
breadcrumb: [Integrating ServiceNow CPQ with visualization tools, ServiceNow CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Integrating CDS or other third-party visualization tools

Integrate CDS Visual or other third-party tools for technical visualization. Sync configuration inputs with visual updates to enhance user experience.

ServiceNow CPQ can be implemented to share field values with third-party visualization tools so that visualization is updated in real time as the user changes configuration inputs. This article discusses integrating the CDS Visual tool as an example. Depending on the CDS model setup, the visualization may render as CAD drawings, 2D images and 3D interactive images.

![Product visual](../images/cpq-cds-visualization.png)

The integration between ServiceNow CPQ and CDS is accomplished in the Blueprint layout definition. The following layout CSV file contains a sample of how the ServiceNow CPQ administrator defines where the CDS visualization will be rendered. It also specifies the CDS environment and ServiceNow CPQ field data to be sent.

[Layout\_CDS\_in\_sidebar \[Google Sheet\]](https://docs.google.com/spreadsheets/d/1UooX9WcinGssN4VpzEzu0pGTq4n_aTQ_Vp2epyI0kSk/edit?usp=sharing)

## Step-by-step guide

This article can help you decide how to add the CDS configuration.

1.  Open the layout editor in your ServiceNow CPQ configurator.
2.  Download your CSV layout file.
3.  Open your CSV layout file, and add the CDS layout element fields \(highlighted in detail below\).
4.  Re-upload your CSV layout file to ServiceNow CPQ. Your CDS layout element should now be present in the layout.
5.  Open the configuration options for your CDS layout element and add in the necessary JSON data lines.

## Technical configuration options

The integration between ServiceNow CPQ and CDS is accomplished in the Blueprint layout definition. The following layout CSV file helps demonstrate how the administrator defines where in the UI the CDS visualization will be rendered. It also specifies the CDS environment and the ServiceNow CPQ field data to be sent.

The layout can be updated directly in the layout editor. In the layout editor, create a new section named CDS in your CSV file using the fields highlighted in red below, and upload the new file to layout.

![Technical Configuration Options](../images/cpq-cds-csv.png)

From here, you can open the settings for this layout element, and configure the following fields using the CDS Properties JSON editor:

![Menu](../images/cpq-cds-settings.png)

These properties can be configured in this element. The following table provides the name and description for each element.

<table><thead><tr><th>

Property name

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

eventFields

</td><td>

no

</td><td>

Array or object of fields to send to CDS.

 An array will assume the contained strings are both ServiceNow CPQ variable names, and CDS variable names.

 An object will have key:value pairs. The Key is the ServiceNow CPQ variable name, and the value is the CDS variable name.

 Set fields are allowed to be defined here, using the format:

 `set.{setVariableName}.{fieldVariableName}`

</td></tr><tr><td>

eventSets

</td><td>

no

</td><td>

Array or object of sets to send to CDS.

 An array will assume the contained strings are both ServiceNow CPQ variable names, and CDS variable names.

 An object will have key:value pairs. The Key is the ServiceNow CPQ variable name, and the value is the CDS variable name.

 The set will be sent as a whole, up to 25 indexes long:

 ```
setVariableName: [
{
field1: 'value',
field2: 'value'
}
{
field1: 'value',
field2: 'value'
}
]
```

</td></tr><tr><td>

eventProductPickers

</td><td>

no

</td><td>

Sends the entire product picker's data as an array of objects to CDS.

 An array will assume the contained strings are both ServiceNow CPQ variable names, and CDS variable names.

 An object will have key:value pairs. The Key is the ServiceNow CPQ variable name, and the value is the CDS variable name.

 The product picker will be sent as a whole, up to 25 indexes long.

 Option \#1:

 ```
{
   "eventProductPickers": [
      "productPicker1",
      "productPicker2"
   ]
}
```

 Option \#2:

 ```
{
  "eventProductPickers": {
     "logikProductPicker1": "cdsProductPickerName1",
     "logikProductPicker2": "cdsProductPickerName2"    }
}
```

</td></tr><tr><td>

domain

</td><td>

yes

</td><td>

Domain of CDS visualization

</td></tr><tr><td>

env

</td><td>

no

</td><td>

Defaults to”qa” if not provided

</td></tr><tr><td>

setActiveTriggers

</td><td>

no

</td><td>

An array of variable names corresponding to a boolean field in a set. The listed fields will serve as a trigger for denoting which index of the set is active when being used in a set repeater.

 These are required if using a Basic Container or Expandable Section as the repeated tier type

</td></tr><tr><td>

height

</td><td>

no

</td><td>

Height of the visualization window in px - defaults to 500

</td></tr><tr><td>

width

</td><td>

no

</td><td>

Width of the visualization window in px - defaults to 500

</td></tr></tbody>
</table>## JSON string formatting

The final JSON string formatting should resemble the following:

```
{

"domain": "exampleDomain", "env": "qa"

"eventFields": ["field1", "field2", "field3"]

}
```

## Notes

-   In the layout definition sample, the CDS rendering will display in a BasicContainer sidebar positioned in the upper right.
    -   CDS can pass ServiceNow CPQ a JSON object to a text field.
    -   Use advanced rules to parse the JSON responses from CDS.
-   The JSON provided in the 'value' column \(column I\) of the CDS element row contains the following syntax:

    ```
    {
    "eventFields": [ "FIELD1",
    "FIELD2", "FIELD3"
    ],
    "domain": "CDS_DOMAIN", "env": "CDS_ENV_SECTOR"
    }
    ```

    `domain`: the name of the domain serving your project, as provided by CDS.

    `env`: the name of the environment service for your project, as provided by CDS. Example: "qa".

    The eventFields array contains the variable names of the ServiceNow CPQ fields that are passed to CDS. In the past, the norm has been that CDS will match their variables to the ServiceNow CPQ variable names. Confirm that this is the case for your implementation with CDS.

    `eventFields` must contain all fields that will be communicated between ServiceNow CPQ and CDS \(that is, both ServiceNow CPQ fields that control the CDS visual and fields that are passed back to ServiceNow CPQ based on changes made in the CDS visualization\).

-   Sets can also be passed to CDS, although only the first 25 indexes can be sent. This mirrors the above process except the property name is `eventSets` instead of `eventFields`.
-   Array or object of sets to send to CDS:
    -   An array will assume the contained strings are both ServiceNow CPQ variable name and CDS variable names.
    -   An object will have key:value pairs. The key is the ServiceNow CPQ variable name, and the value is the CDS variable name.
    -   This will be sent as a whole, up to 25 indexes long using the following syntax:

        ```
        setVariableName: [
        {
        field1: 'value', field2: 'value'
        },
        {
        field1: 'value', field2: 'value'
        },
        ]
        ```

-   Product pickers can also be passed to CDS with a restriction of only the first 25 indexes being able to be sent. This mirrors the above process, except the property name is `eventProductPickers` instead of `eventFields` or `setFields`. The following two syntaxes work:

    ```
    {
      "eventProductPickers": ["productPicker1", "productPicker2"]
    }
    ```

    ```
    {
      "eventProductPickers": {
        "logikProductPicker1": "cdsProductPickerName1",
        "logikProductPicker2": "cdsProductPickerName2"
      }
    }
    ```

-   CDS can be set up for two-way communication. One-way communication updates the CDS graphic when the user updates relevant ServiceNow CPQ fields. The second mode allows the user to manipulate the CDS graphic, and CDS will update the relevant ServiceNow CPQ field inputs. For standard fields, CDS writes back to the mapped ServiceNow CPQ field. If ServiceNow CPQ sets are being used in a two-way communication setup, ServiceNow CPQ and CDS administrators will need to coordinate the following setup:
    -   The ServiceNow CPQ Admin will define a distinct event field to which set data will be written from CDS.
    -   The CDS admin will specify this field as the destination for set data.
    -   The ServiceNow CPQ Admin will define determination rules that parse the field and populate the set.

