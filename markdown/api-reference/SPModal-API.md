---
title: spModal - Client
description: Shows alerts, prompts, and confirmation dialogs in Service Portal widgets. The spModal class is available in Service Portal client scripts.Displays an alert.Displays a confirmation message.Opens a modal window using the specified options.Displays a prompt for user input.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# spModal- Client

Shows alerts, prompts, and confirmation dialogs in Service Portal widgets. The spModal class is available in Service Portal client scripts.

The spModal class is a lightweight wrapper for Angular UI bootstrap's [$uibModal](https://angular-ui.github.io/bootstrap/#/modal). You can use the spModal.open\(\) method to display a widget in a modal dialog.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## spModal - alert\(String message\).then\(fn\)

Displays an alert.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to display.|

|Type|Description|
|----|-----------|
|Boolean|The promise contains a single argument that contains true or false.|

```
// HTML template 
<button ng-click="c.onAlert()" class="btn btn-default">
    Alert
  </button>

// Client script
function(spModal) {
    var c = this;
  c.onAlert = function () {
        spModal.alert('How do you feel today?').then(function (answer) {
            c.simple = answer;
        });
    }
 }
```

## spModal - confirm\(String message\).then\(fn\)

Displays a confirmation message.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to display.|

|Type|Description|
|----|-----------|
|Boolean|The promise contains a single argument that contains true or false.|

```
// HTML template 
 <button ng-click="c.onConfirm()" class="btn btn-default"> Confirm </button> 
<span>{{c.confirmed}}</span>   

// Client script
function(spModal) {
  var c = this;
  c.onConfirm = function() {
        c.confirmed = "asking";
        spModal.confirm("Can you confirm or deny this?").then(function(confirmed) {
            c.confirmed = confirmed; // true or false
        })
    }
 } 
```

Confirm with HTML message:

```
//HTML template 
<button ng-click="c.onConfirmEx()" class="btn btn-default">
    Confirm - HTML message
  </button>
  <span>{{c.confirmed}}</span>

// Client script
function(spModal) {
  var c = this;
  // more control, passing options
    c.onConfirmEx = function() {
        c.confirmed = "asking";
        var warn = '<i class="fa fa-warning" aria-hidden="true"></i>';
        spModal.open({
            title: 'Delete this Thing?',
            message: warn + ' Are you <b>sure</b> you want to do that?'
        }).then(function(confirmed) {
            c.confirmed = confirmed;
        })
    }
}
```

## spModal - open\(Object options\).then\(fn\)

Opens a modal window using the specified options.

<table id="table_trg_vwy_my" class="parameters"><thead><tr><th>

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

An object that may have these properties. -   backdrop: Boolean\|String. Controls the presence of a backdrop.

Valid values:

    -   true: Displays backdrop.
    -   false: No backdrop.
    -   static: Disables modal closing by selecting the backdrop.
Default: true

-   buttons: Array. Buttons to show on the dialog. The default is Cancel and OK.
-   input: Boolean. When true, shows an input field on the dialog.

Default: false

-   keyboard: Boolean. When true, indicates that the dialog is closable using the ESC key.

Default: true

-   message: String. HTML that goes in the header.

Default: empty

-   noDismiss: Boolean. When true,indicates that the header section that contains the close icon is present.

Default: false

-   shared: Client-side object. Shares data with the embedded widget client script.
-   size: String. Size of the window. Valid values: 'sm' or 'lg'.

Default: empty

-   title: String. HTML that goes in the header.

Default: empty

-   value: String. Value of the input field.

Default: empty

-   widget: String. Widget ID or sys\_id to embed in the dialog.

Default: empty

-   widgetInput: Object. Sent to the embedded widget as input.

Default: null


</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following code example shows how to create a prompt with a label.

```
//HTML template
<button ng-click="c.onOpen()" class="btn btn-default">
    Prompt with label
  </button>
  <div ng-show="c.name">
    You answered <span>{{c.name}}</span>
  </div>

//Client code
function(spModal) {
  var c = this;
  c.onOpen = function() {
        //ask the user for a string
        spModal.open({
            title: 'Give me a name',
            message: 'What would you like to name it?',
            input: true,
            value: c.name
        }).then(function(name) {
            c.name = name;
        })
    }
}
```

The following code example shows how to use the custom buttons option.

```
//HTML template
<button ng-click="c.onAgree()" class="btn btn-default">
    Agree
  </button>
  <div ng-show="c.agree">
    You answered {{c.agree}}
  </div>

//Client script
function(spModal) {
  var c = this;
  c.onAgree = function() {
        // ask the user for a string
        // note embedded html in message
        var h = '<h4>Apple likes people to agree to lots of stuff</h4>'
        // Line feeds added to the following lines for presentation formatting.
        var m = 'Your use of Apple software or hardware products is based 
on the software license and other terms and conditions in effect for the 
product at the time of purchase. Your agreement to these terms is required 
to install or use the product. '
        spModal.open({
            title: 'Do you agree?',
            message: h + m,
            buttons: [
                {label:'✘ ${No}', cancel: true},
                {label:'✔ ${Yes}', primary: true}
            ]
        }).then(function() {
            c.agree = 'yes';
        }, function() {
            c.agree = 'no';
        })
    }
}
```

The following code example shows how to use the embedded widget option.

```
//HTML template
<button ng-click="c.onWidget('widget-cool-clock')" class="btn btn-default">
    Cool Clock
  </button>

//Client script
function(spModal) {
  var c = this;
  c.onWidget = function(widgetId, widgetInput) {
        spModal.open({
            title: 'Displaying widget ' + widgetId,
            widget: widgetId, 
            widgetInput: widgetInput || {}
        }).then(function(){
            console.log('widget dismissed');
        })      
    }
}
```

## spModal - prompt\(String message, String default\).then\(fn\)

Displays a prompt for user input.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to display.|
|default \(optional\)|String|A default value to use if the user does not provide a response.|

|Type|Description|
|----|-----------|
|String|The promise contains the user's response, or the default value if the user does not enter a response.|

```
//HTML template
 <button ng-click="c.onPrompt()" class="btn btn-default">
    Prompt
  </button>
  <div ng-show="c.name">
    You answered <span>{{c.name}}</span>
  </div>

// Client script
function(spModal) {
  var c = this;
  c.onPrompt = function() {
        spModal.prompt("Your name please", c.name).then(function(name) {
            c.name = name;
        })
    }
}
```

