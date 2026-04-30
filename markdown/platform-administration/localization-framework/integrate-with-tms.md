---
title: Integrate with a translation management system
description: Integrate with any translation management system of your choice to localize the artifacts requested for translations.
locale: en-US
release: yokohama
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Translation Management System configurations, Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Integrate with a translation management system

Integrate with any translation management system of your choice to localize the artifacts requested for translations.

## Before you begin

Role required: localization\_admin

## Procedure

1.  Create subflows to request translations and to retrieve the translated content using Integration Hub subflows, actions, and connections and credentials.

    1.  Ensure that the error messages and codes from the TMS provider are mapped correctly with the error messages and codes supported the ServiceNow platform.

        |Error code|Error message|
        |----------|-------------|
        |40510|Error while requesting translations.|
        |40520|Error while retrieving translations.|
        |40500|Authentication failed.|

    2.  Ensure that the input and output fields are in the following format for the subflows:

<table id="table_ekn_4fc_5nb"><thead><tr><th>

Field Name

</th><th>

Description

</th><th>

Type

</th></tr><tr><th class="sub-head" colspan="3" align="left">

Inputs

</th></tr></thead><tbody><tr><td>

lftask\_number

</td><td>

Associated localization task number.

</td><td>

String

</td></tr><tr><td>

xliff\_1\_2\_content

</td><td>

Content of an artifact which must be translated in XLIFF 1.2 format.For example,

```
'csv', 'xliff 1.2'
```

</td><td>

String

</td></tr><tr><td>

source\_language

</td><td>

Language code of the source text.For example,

```
'en'
```

</td><td>

String

</td></tr><tr><td>

target\_language

</td><td>

Language code of the target text.For example,

```
'fr', 'it'
```

</td><td>

String

</td></tr><tr><td class="sub-head" colspan="3">

Outputs

</td></tr><tr><td>

project\_info

</td><td>

The ID for the project created for an artifact configuration.

</td><td>

Object

</td></tr><tr><td>

status

</td><td>

Status of the request.For example, Success or Failure.

</td><td>

Choice

</td></tr><tr><td>

error\_message

</td><td>

The reason for the error that populates when an error occurs.

</td><td>

String

</td></tr><tr><td>

error\_code

</td><td>

The error code that populates when an error occurs.

</td><td>

String

</td></tr></tbody>
</table><table id="table_nn3_rfc_5nb"><thead><tr><th>

Field Name

</th><th>

Description

</th><th>

Type

</th></tr><tr><th class="sub-head" colspan="3" align="left">

Inputs

</th></tr></thead><tbody><tr><td>

lftask\_number

</td><td>

Associated localization task number.

</td><td>

String

</td></tr><tr><td>

project\_info

</td><td>

The ID for the project created for an artifact configuration.

</td><td>

Object

</td></tr><tr><td class="sub-head" colspan="3" align="left">

Outputs

</td></tr><tr><td>

translated\_xliff\_1\_2

</td><td>

Translated XLIFF file received from the TMS.

</td><td>

String

</td></tr><tr><td>

status

</td><td>

Status of the request.For example, Success or Failure.

</td><td>

Choice

</td></tr><tr><td>

error\_message

</td><td>

The reason for the error that populates when an error occurs.

</td><td>

String

</td></tr><tr><td>

error\_code

</td><td>

The error code that populates when an error occurs.

</td><td>

String

</td></tr></tbody>
</table>2.  Create and configure a custom translation management system and activate it.

    See [Create a custom translation management system](create-custom-tms.md).

    **Note:** Localization Framework depends on Integration Hub to build integrations with third-party systems.


**Parent Topic:**[Translation Management System configurations](../concept/tms-configuration.md)

