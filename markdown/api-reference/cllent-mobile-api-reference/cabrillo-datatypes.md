---
title: Cabrillo JS data types
description: These are common data types used by Cabrillo JS APIs.Defines an attachment.Defines attachment options.Defines a button. Different interface contexts may support a subset of a button's properties.Contains the result passed from a modal window that was dismissed.Specifies a request to navigate to a list or record.Contains the location and dimensions of a rectangle.Defines a spinner.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# Cabrillo JS data types

These are common data types used by Cabrillo JS APIs.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## Cabrillo.Attachment

Defines an attachment.

|Name|Type|Description|
|----|----|-----------|
|content\_type|String|The attachment content type.|
|ext|String|The attachment file extension.|
|file\_name|String|The full file name of the attachment including the extension.|
|sys\_created\_by|String|The user name of the user that created the attachment.|
|sys\_id|String|The attachment record sys\_id.|
|sys\_updated\_on|String|The date the attachment record was updated.|
|table\_name|String|Name of the table containing the record to which the attachment is attached.|
|table\_sys\_id|String|The sys\_id of the record that to which the attachment is attached.|
|thumbnail|String|The URL for the image thumbnail of the attachment. Only applies to image attachments.|

## Cabrillo.AttachmentOptions

Defines attachment options.

<table id="table_t2c_pkw_2bb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isSingleSelection

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the document picker for uploading files allows multi-selection.

 Valid values:

-   true: Only one file to upload can be selected at a time.
-   false: Multiple files to upload can be selected at a time.

 Default: False

</td></tr></tbody>
</table>## Cabrillo.Button

Defines a button. Different interface contexts may support a subset of a button's properties.

<table id="table_kq1_hmw_2bb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

backgroundColor

</td><td>

String

</td><td>

Background color of the button or badge. A string containing hex, RGB, HSL, or an x11-named color.**Note:** The color can't be set for [buttons in the navigation bar](../../CabrilloViewLayout-client/concept/cabrillo-viewLayout-namespace.md#). The color can be set for [bottom buttons](../../CabrilloViewLayout-client/concept/cabrillo-viewLayout-namespace.md#).

</td></tr><tr><td>

badgeCount

</td><td>

Number

</td><td>

Number value to display on the button's badge.

</td></tr><tr><td>

buttonId

</td><td>

String

</td><td>

Required. Unique id for the button. This value is returned in the button action payload to indicate which button the user tapped.

</td></tr><tr><td>

buttonStyle

</td><td>

String

</td><td>

Used to customize the style of the button.

</td></tr><tr><td>

enabled

</td><td>

Boolean

</td><td>

Indicates whether the button is enabled.

</td></tr><tr><td>

imageName

</td><td>

String

</td><td>

Specifies an image. Possible values are: -   add: Displays an add button.
-   back: Displays a back arrow image to navigate back.
-   cart: Displays a shopping cart.
-   close: Displays an X image to navigate back.
-   edit: Displays an edit button.
-   filter: Displays a filter button.
-   menu: Displays a menu button.
-   search: Displays a search button.

</td></tr><tr><td>

textColor

</td><td>

String

</td><td>

The text color of the badge or button. A string containing hex, RGB, HSL, or an x11-named color.**Note:** The color can't be set for [buttons in the navigation bar](../../CabrilloViewLayout-client/concept/cabrillo-viewLayout-namespace.md#). The color can be set for [bottom buttons](../../CabrilloViewLayout-client/concept/cabrillo-viewLayout-namespace.md#).

</td></tr><tr><td>

title

</td><td>

String

</td><td>

Title of the button. The string should be localized.

</td></tr></tbody>
</table>## Cabrillo.ModalResponse

Contains the result passed from a modal window that was dismissed.

|Name|Type|Description|
|----|----|-----------|
|results|Object|The result from the dismissed modal window.|

## Cabrillo.NavigationRequest

Specifies a request to navigate to a list or record.

|Name|Type|Description|
|----|----|-----------|
|table|String|The table to navigate to. Required for both list and record navigation.|
|sysId|String|The sys\_id of the record to navigate to. Required for record navigation.|
|query|String|An encoded query for the requested list. Can be used to seed values for record navigation requests.|
|view|String|The list or record view.|

## Cabrillo.Rect

Contains the location and dimensions of a rectangle.

|Name|Type|Description|
|----|----|-----------|
|x|Number|The x origin of the rectangle.|
|y|Number|The y origin of the rectangle.|
|width|Number|The width in points.|
|height|Number|The height in points.|

## Cabrillo.Spinner

Defines a spinner.

<table id="table_t2c_pkw_2bb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mask

</td><td>

Boolean

</td><td>

Optional. Determines whether to display a mask behind the spinner.Valid values:

-   true: Displays a mask behind the spinner.
-   false: Does not display a mask behind the spinner.

Default: false

</td></tr><tr><td>

maskColor

</td><td>

String

</td><td>

Color of the mask, if enabled.

</td></tr></tbody>
</table>