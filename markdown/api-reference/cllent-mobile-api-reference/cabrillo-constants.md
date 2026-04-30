---
title: Cabrillo JS constants
description: These are the constants used by Cabrillo JS.Constants to use when setting the style of a button.Constants to use when setting the close button style of modal interfaces.Constants to use when setting the style of a message.Constants to use when setting the presentation style of modal interfaces.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# Cabrillo JS constants

These are the constants used by Cabrillo JS.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## Cabrillo JS constants - button styles

Constants to use when setting the style of a button.

<table id="table_tq2_dc2_wbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cabrillo.viewLayout.MORE\_MENU\_BUTTON\_STYLE

</td><td>

String

</td><td>

Indicates that the button appears in the navigation bar's overflow button menu.

</td></tr><tr><td>

cabrillo.viewLayout.REPLACE\_BACK\_BUTTON\_STYLE

</td><td>

String

</td><td>

Replaces the native back button with a Cabrillo button. **Note:** Use this style with caution. If the webpage does not restore the native back button after using the Cabrillo replacement, the user may not be able to navigate back.

</td></tr></tbody>
</table>## Cabrillo JS constants - close button styles

Constants to use when setting the close button style of modal interfaces.

|Name|Type|Description|
|----|----|-----------|
|cabrillo.modal.CLOSE\_BUTTON\_STYLE\_CANCEL|String|The modal has a localized cancel button to close the modal.|
|cabrillo.modal.CLOSE\_BUTTON\_STYLE\_CLOSE|String|The modal has a localized close button to close the modal.|
|cabrillo.modal.CLOSE\_BUTTON\_STYLE\_DONE|String|The modal has a localized done button to close the modal.|

## Cabrillo JS constants - message styles

Constants to use when setting the style of a message.

The appearance of each message style can be customized using theme colors. For more information, see [Next Experience theming for mobile](https://www.servicenow.com/docs/access?context=explore-ne-theming&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|cabrillo.message.ERROR\_MESSAGE\_STYLE|String|The message is styled to indicate an error.|
|cabrillo.message.INFO\_MESSAGE\_STYLE|String|The message is styled to indicate non-critical information.|
|cabrillo.message.SUCCESS\_MESSAGE\_STYLE|String|The message is styled to indicate a success.|
|cabrillo.message.WARNING\_MESSAGE\_STYLE|String|The message is styled to indicate a warning.|

## Cabrillo JS constants - modal presentation styles

Constants to use when setting the presentation style of modal interfaces.

|Name|Type|Description|
|----|----|-----------|
|cabrillo.modal.MODAL\_PRESENTATION\_STYLE\_FULL\_SCREEN|String|The modal is presented full screen.|
|cabrillo.modal.MODAL\_PRESENTATION\_STYLE\_FORM\_SHEET|String|The modal is presented as a form sheet, but may adapt to full screen on small devices.|

