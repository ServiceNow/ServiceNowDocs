---
title: cabrillo.viewLayout - Client
description: Cabrillo JS functions to provide access to native UI elements like buttons and spinners.Gets the current native view's title.Hides the back button on the client interface.Hides a native spinner in the current interface.Set buttons at the bottom of the current interface.Set buttons in the navigation bar of the current interface.Sets the current native view's title.Shows the back button on the client interface.Shows a native spinner in the current interface.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# cabrillo.viewLayout - Client

Cabrillo JS functions to provide access to native UI elements like buttons and spinners.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## cabrillo.viewLayout - getTitle\(\)

Gets the current native view's title.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|promise|If successful, resolves to the title text, otherwise an error.|

```
cabrillo.viewLayout.getTitle()
.then(function(title) {
   console.log(title);
}, function(error) {
   console.log(error);
});
```

## cabrillo.viewLayout - hideBackButton\(\)

Hides the back button on the client interface.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

```
cabrillo.viewLayout.hideBackButton();
```

## cabrillo.viewLayout - hideSpinner\(\)

Hides a native spinner in the current interface.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
cabrillo.viewLayout.hideSpinner();
```

## cabrillo.viewLayout - setBottomButtons\(Array buttons, Function execute\)

Set buttons at the bottom of the current interface.

Images and badges are not supported in bottom buttons.

|Name|Type|Description|
|----|----|-----------|
|buttons|Array of Cabrillo.Button objects|Describes the buttons to set. A maximum of one button is currently supported.|
|execute|Function|The function to call when a button is tapped. The function has no return value and takes the selected button index as its only parameter. The function must have a single parameter that is a Number.|

|Type|Description|
|----|-----------|
|promise|If successful, an unresolved object, otherwise an error.|

Set bottom buttons.

```
var buttons = [
    {
        title: 'Add to Cart',
        buttonId: 'btnAddCart',
        enabled: true,
        backgroundColor: '#3091F9',
        textColor: '#FFFFFF'
    }
];

cabrillo.viewLayout.setBottomButtons(buttons, (buttonIndex) => {
    console.log('Success. Received an event from the button.');
}).catch((err) => {
    console.log('Failed to register buttons.');
    console.error(err);
});
```

Clear bottom buttons.

```
cabrillo.viewLayout.setBottomButtons();
```

## cabrillo.viewLayout - setNavigationBarButtons\(Array buttons, Function execute\)

Set buttons in the navigation bar of the current interface.

Images and badges for buttons that appear in the overflow button menu are omitted. For this reason, it's best to provide a title and an image name when setting an image button in the navigation bar.

|Name|Type|Description|
|----|----|-----------|
|buttons|Array of Cabrillo.Button objects.|Describes the buttons to set. Buttons may overflow into an additional menu as needed.|
|execute|Function|The function to call when a button is tapped. The function has no return value and takes the selected button index as its only parameter. The function must have a single parameter that is a Number.|

|Type|Description|
|----|-----------|
|promise|If successful, an unresolved object, otherwise an error.|

Set navigation bar buttons.

```
var buttons = [
   {
      title: "Save",
      enabled: true,
      buttonId: "btnSave",
   },
];

cabrillo.viewLayout
   .setBottomButtons(buttons, (buttonIndex) => {
      console.log("Success. Received an event from the button.");
   })
   .catch((err) => {
      console.log("Failed to register buttons.");
      console.error(err);
   });
```

Handle multiple buttons.

```
var buttons = [
   {
      title: "Save",
      enabled: true,
      buttonId: "btnSave",
   },
   {
      title: "Delete",
      enabled: true,
      buttonId: "btnDelete",
   },
];

cabrillo.viewLayout
   .setNavigationBarButtons(buttons, (buttonIndex) => {
      switch (buttonIndex) {
         case 0:
            console.log("Received an event from the Save button.");
            break;
         case 1:
            console.log("Received an event from the Delete button.");
            break;
      }
   })
   .catch((err) => {
      console.log("Failed to register buttons.");
      console.error(err);
   });
```

Buttons placed in the navigation bar can be represented by an image.

```
var buttons = [
   {
      title: "Compose",
      buttonId: "btnCompose",
      imageName: "compose",
      enabled: true,
   },
];

cabrillo.viewLayout
   .setNavigationBarButtons(buttons, (buttonIndex) => {
      console.log("Success. Received an event from the button.");
   })
   .catch((err) => {
      console.log("Failed to register buttons.");
      console.error(err);
   });
```

A native back button is shown in the native app by default, but you can replace the back button with a Cabrillo button by setting a button's `buttonStyle` property.

```
var buttons = [
   {
      title: "Cancel",
      buttonId: "btnCancel",
      imageName: "close",
      buttonStyle: cabrillo.viewLayout.REPLACE_BACK_BUTTON_STYLE,
      enabled: true,
   },
   {
      title: "Done",
      enabled: true,
   },
];

cabrillo.viewLayout
   .setNavigationBarButtons(buttons, (buttonIndex) => {
      switch (buttonIndex) {
         case 0:
            c.log("Cancel button was clicked.");
            break;
         case 1:
            c.log("Done button was clicked.");
            break;
      }
   })
   .catch((err) => {
      c.log("Failed to register buttons.");
      c.error(err);
   });
```

Buttons are placed in the overflow button menu as needed. To force a button into the overflow button menu, set the button's buttonStyle property.

```
var buttons = [
   {
      title: "Save",
      buttonId: "btnSave",
      buttonStyle: cabrillo.viewLayout.MORE_MENU_BUTTON_STYLE,
      enabled: true,
   },
];

cabrillo.viewLayout
   .setNavigationBarButtons(buttons, (buttonIndex) => {
      console.log("Success. Received an event from the button.");
   })
   .catch((err) => {
      console.log("Failed to register buttons.");
      console.error(err);
   });
```

Buttons may have a badge when placed in the navigation bar. This example sets a button with a shopping cart icon and a badge count of 3. The badge has a blue background with white text.

```
var buttons = [
   {
      title: "Cart",
      buttonId: "btnCart",
      imageName: "cart",
      badgeCount: 3,
      backgroundColor: "#3091F9",
      textColor: "#FFFFFF",
      enabled: true,
   },
];

cabrillo.viewLayout
   .setNavigationBarButtons(buttons, (buttonIndex) => {
      console.log("Success. Received an event from the button.");
   })
   .catch((err) => {
      console.log("Failed to register buttons.");
      console.error(err);
   });
```

Clear navigation bar buttons.

```
cabrillo.viewLayout.setNavigationBarButtons();
```

## cabrillo.viewLayout - setTitle\(String title\)

Sets the current native view's title.

|Name|Type|Description|
|----|----|-----------|
|title|String|The title of the interface.|

|Type|Description|
|----|-----------|
|void| |

```
cabrillo.viewLayout.setTitle('My Title');
```

## cabrillo.viewLayout - showBackButton\(\)

Shows the back button on the client interface.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

```
cabrillo.viewLayout.showBackButton();
```

## cabrillo.viewLayout - showSpinner\(Object options\)

Shows a native spinner in the current interface.

<table id="table_ljp_jnn_wbb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

options

</td><td>

Object

</td><td>

Optional. Additional settings to modify the appearance of the spinner.```
{
  "mask": Boolean,
  "maskColor": "String"
}
```

</td></tr><tr><td>

options.mask

</td><td>

Boolean

</td><td>

Optional. Determines whether to display a mask behind the spinner.Valid values:

-   true: Displays a mask behind the spinner.
-   false: Does not display a mask behind the spinner.

Default: false

</td></tr><tr><td>

options.maskColor

</td><td>

String

</td><td>

Color of the mask, if enabled.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var options = { mask: true, maskColor: '#ffffff' };
cabrillo.viewLayout.showSpinner(options);
```

