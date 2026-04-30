---
title: cabrillo.message - Client
description: Cabrillo JS functions to display messages in the native UI.Displays a message in the native UI.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# cabrillo.message - Client

Cabrillo JS functions to display messages in the native UI.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## cabrillo.message - showMessage\(String style, String title\)

Displays a message in the native UI.

<table id="table_oyf_tnn_wbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

style

</td><td>

String

</td><td>

Style of the banner.Possible values:

-   cabrillo.message.ERROR\_MESSAGE\_STYLE
-   cabrillo.message.INFO\_MESSAGE\_STYLE
-   cabrillo.message.SUCCESS\_MESSAGE\_STYLE
-   cabrillo.message.WARNING\_MESSAGE\_STYLE

For more information, see [Cabrillo JS constants - message styles](../../namespace-topics/concept/cabrillo-constants.md#).

</td></tr><tr><td>

title

</td><td>

String

</td><td>

Text to display in the banner.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|promise|If successful, an unresolved object, otherwise an error.|

```
var style = cabrillo.message.SUCCESS_MESSAGE_STYLE;
var title = "You did it!";

cabrillo.message.showMessage(
   style,
   title
).then(function(response) {
   console.log('success');
}, function(error) {
   console.log(error);
});
```

