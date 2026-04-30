---
title: Embedded widgets
description: Embed a widget in the HTML template, server script, or client script.Embed the cool clock widget multiple times using custom options.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Embedded widgets

Embed a widget in the HTML template, server script, or client script.

## Embed a widget in an HTML template

Use the `<widget></widget>` element to embed a widget in an HTML template. Pass in the ID of the widget you are trying to embed as a parameter.

```
<div>
    <widget id="widget-cool-clock"></widget>
</div>
```

If a widget has an option schema, you can define instance options in JSON format.

```
<widget id="widget-cool-clock" options='{"zone": "America/Los_Angeles","title": "San Diego, CA"}'></widget>
```

Alternatively, you can define options in the widget server script.

-   **HTML template**

    ```
    <widget id="widget-cool-clock" options='data.clockOptions'></widget>
    ```

-   **Server script**

    ```
    (function() {
      data.clockOptions = {"zone": "America/Los_Angeles","title": "San Diego, CA"};
    })();
    ```


## Embed a widget in a client script

Use [spUtil.get\(\)](https://www.servicenow.com/docs/access?context=spUtilAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) to get a widget model in the client script.

```
spUtil.get("widget-sc-cat-item", {sys_id: "your_catalog_item_sys_id"}).then(function(response) {
    c.catalogItemWidget = response;
});
```

When using the spUtil class in a widget client script, you must inject the class into the client script function. The following example embeds the Cool Clock widget:

-   **Client script**

    ```
    function(spUtil) {
        var c = this;
        spUtil.get("widget-cool-clock").then(function(response) {
                c.myClockWidget = response;
        });
    }
    ```

-   **HTML template**

    ```
    <sp-widget widget="c.myClockWidget"></sp-widget>
    ```


## Embed a widget in a server script

Use [$sp.getWidget\(\)](https://www.servicenow.com/docs/access?context=c_GlideSPScriptableScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) to get a widget model in the server script.

```
data.catalogItemWidget = $sp.getWidget("widget-sc-cat-item");
```

The following example embeds the Cool Clock widget:

-   **Server script**

    ```
    (function() {
        var coolClockOptions = {"zone": "America/Los_Angeles","title": "San Diego, CA"}
        data.coolClockWidget = $sp.getWidget('widget-cool-clock', coolClockOptions);
    })();
    ```

-   **HTML template**

    ```
    <sp-widget widget="data.coolClockWidget"></sp-widget>
    ```


## Widget model properties

When a widget model is called from within another widget, the HTML template, client script, and link function are loaded just as they are in the sp\_widget record. The data property is the result of the widget server script execution. Anything that you put on the data object on the server is available in the data object on the client.

|Property name|Type|Description|
|-------------|----|-----------|
|client\_script|string|Widget client script field.|
|css|string|Compiled CSS output from the SASS field for the widget.|
|data|object|Data object containing keys and values from the widget server script.|
|dependencies|array|Any third-party libraries to load before the widget executes.|
|options|object|Options used to initialize the widget.|
|template|string|HTML template field for the widget.|

**Parent Topic:**[Developing custom widgets](widget-dev-guide.md)

## Embed a widget multiple times with custom options

Embed the cool clock widget multiple times using custom options.

### Before you begin

Role required: admin or sp\_admin

### About this task

Create a widget that embeds multiple instances of the cool clock widget, each with a different time zone and title. Open the cool clock widget in the Widget Editor to see widget options referenced in the HTML template and the Client Script.

![Cool Clock widget with c.options.title, c.options.c_color, and c.options.zone highlighted](../image/CoolClockOptionsHighlighted.png "Cool Clock widget with Options highlighted")

### Procedure

1.  Clone the Cool Clock widget with the name `Embedded clock`.

2.  Replace the code blocks with the following:

    HTML Template

    ```
    <div class="panel panel-default">
      <div class="panel-heading">Time across the US</div>
      <div class="panel-body">
        <div class="row">
          <div class="col-sm-3" ng-repeat="myClock in c.data.clocks">
            <sp-widget widget="myClock"></sp-widget>
          </div>
        </div>
      </div>
    </div>
    ```

    CSS

    ```
    .panel {
        margin-top: 10px;
    }
    ```

    Client Script

    ```
    function() {
        // nothing to do here...
    }
    ```

    Server Script

    ```
    (function() {
        var options = [
            {zone: "America/Los_Angeles", title: "San Diego"},
            {zone: "America/Denver", title: "Denver"},
            {zone: "America/Chicago", title: "Chicago"},
            {zone: "America/New_York", title: "New York"}
        ];
    
        data.clocks = [];
        for (var i in options) {
            data.clocks.push($sp.getWidget("widget-cool-clock", options[i]));
        }
    })();
    ```


### Result

Each instance of the clock in the embedded clock widget appears with a different time zone.

![Embedded clock with four embedded widgets with four different time zones](../image/SampleClockOptions.png "Sample clock options")

