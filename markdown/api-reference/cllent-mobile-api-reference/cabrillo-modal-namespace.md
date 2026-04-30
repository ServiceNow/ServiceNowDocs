---
title: cabrillo.modal - Client
description: Cabrillo JS functions for presenting web content inside of native modals.Use to dismiss a modal that has been presented with the presentModal\(\) function.Presents content in a native modal interface.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# cabrillo.modal - Client

Cabrillo JS functions for presenting web content inside of native modals.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## cabrillo.modal - dismissModal\(Object data\)

Use to dismiss a modal that has been presented with the presentModal\(\) function.

A presented modal is responsible for dismissing itself and passing any results back to the presenting context. The dismissModal\(\) function must be called from the presented context not from the presenting context.

|Name|Type|Description|
|----|----|-----------|
|data|Object|Optional. An object to pass back to the presenting context when the presented context dismisses itself.|

|Type|Description|
|----|-----------|
|promise|If successful, an unresolved object, otherwise an error.|

```
// Any object can be passed back to the presenting context when the presented context dismisses itself.
var results = {
    team: 'Mobile'
    company: 'ServiceNow'
}

cabrillo.modal.dismissModal(results).then(function() {
    console.log('Modal was dismissed and results were passed to presenting context.');
}, function(error) {
    console.log(error);
});
```

## cabrillo.modal - presentModal\( String title, String url, String closeButtonStyle, String modalPresentationStyle\)

Presents content in a native modal interface.

<table id="table_zcl_dxm_wbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

title

</td><td>

String

</td><td>

Title of the modal interface.

</td></tr><tr><td>

url

</td><td>

String

</td><td>

The URL to open the modal. This must be an internal instance URL \(fully qualified or relative; a relative URL is preferred\).

</td></tr><tr><td>

closeButtonStyle

</td><td>

String

</td><td>

Close button style of the modal interface. Possible values:

-   cabrillo.modal.CLOSE\_BUTTON\_STYLE\_CANCEL
-   cabrillo.modal.CLOSE\_BUTTON\_STYLE\_CLOSE
-   cabrillo.modal.CLOSE\_BUTTON\_STYLE\_DONE

For more information, see [Cabrillo JS constants - close button styles](../../namespace-topics/concept/cabrillo-constants.md#).

</td></tr><tr><td>

modalPresentationStyle

</td><td>

String

</td><td>

Presentation style of the modal interface. Possible values:

-   cabrillo.modal.MODAL\_PRESENTATION\_STYLE\_FULL\_SCREEN
-   cabrillo.modal.MODAL\_PRESENTATION\_STYLE\_FORM\_SHEET

For more information, see [Cabrillo JS constants - modal presentation styles](../../namespace-topics/concept/cabrillo-constants.md#).

**Note:** This parameter is only supported on Apple iOS.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|promise|If successful, a Cabrillo.ModalResponse object, otherwise an error.|

Present a native modal that loads a custom URL. This presents a custom Service Portal page in a form sheet style modal. The promise is fulfilled when the modal is dismissed. See the dismissModal\(\) function for custom dismissal capabilities.

```
cabrillo.modal.presentModal('Portal Page',
    '/$sp.do?id=my_modal_page',
    cabrillo.modal.CLOSE_BUTTON_STYLE_CLOSE,
    cabrillo.modal.MODAL_PRESENTATION_STYLE_FORM_SHEET
).then(function(response) {
    // The results from the modal are in a results key on the response object.
    var results = response && response.results ? response.results : null;

    if (results) {
        console.log('Modal dismissed with results.', results);
    } else {
        console.log('Modal dismissed without results.');
    }
}, function(error) {
    console.log(error);
});
```

