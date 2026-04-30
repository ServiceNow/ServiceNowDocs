---
title: Transaction Manager: Layouts - UI effects
description: Learn how to add functionality to a button by programming UI effects in either YAML or JSON.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 5
breadcrumb: [Transaction Manager: Layouts, Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Layouts - UI effects

Learn how to add functionality to a button by programming UI effects in either YAML or JSON.

In Transaction Manager, UI effects are layout elements that add specific functionalities to a button. Unlike with events, users cannot create new UI effects, only customize the ones that ServiceNow CPQ has established.

If an event is also present on the button, the UI effect will run after the event runs.

## Example

One example of a UI effect in action would be having a button to open a searchable list of the products that could be added to a transaction. Here’s how that could be written in the layout:

```
      ...
      {
        "type": "button",
        "event": "productSearch",
        "label": "Add Products",
        "uiEffect": {
          "type": "productSearch",
          "target": "slideout"
        },
        "columnOrder": 6,
        "variableName": "productSearch"
      },
      ...

```

Here’s how that button might appear in the resulting UI:

![Add products](../images/cpq-txn-mgr-layouts-ui-effects-add-button.png)

## Programming UI effects

A UI effect is defined by a combination of parameters. All UI effects will have a type, and some will also have a target, location, and/or options.

These are the possible values for each parameter:

-   **type**: url, anchor, productSearch, lineDetail, reconfigure, addFavorite, manageFavorites, refreshSession, showTier
-   **target**: inline, tab, window, modal, slideout, lineDrawer, fullScreen
-   **location**: \[a URL or an element id\]
-   **options**: \[depends on type\]

## Analysis of types

-   **url** requires a location in the form of a url. Pressing the button will take users to that url by way of a particular target \(inline, tab, window, modal iframe, or slideout iframe\). Using curly braces, admins can dynamically pass field values into the URL. Common use cases would be passing a value to an output document or opening a record page in Salesforce.
-   **anchor** requires a location, which will be an element id in the layout. Pressing the button will focus on or scroll to that element. If there are any related parent-elements, those will be opened in tabs or an accordion structure. The target should be inline.
-   **productSearch** opens the product catalog in the target \(either slideout or modal\). A variable name is required. The UI effect must be added to the gridHeaderButtons element. The options include:

    -   Show products list: products - true \(show\), false \(hide\)
    -   Show favorites list: favorites - true \(show\), false \(hide\)
    -   Location of button placement: actionLocation - footer, header, or both
        -   Default to footer if not specified
        -   Buttons include Cancel, Add Line, Configure, Done Configuring
    The following code would show products, hide favorites, and place buttons on the header only:

    ```
    ...
    "options": {
      "products": true,
      "favorites": false,
      "actionLocation": header
    },
    ...
    ```

-   **lineDetail** must be on a line-level button. Pressing the button opens the line-detail layout in the target \(modal, slideout, or lineDrawer\).
-   **reconfigure** can be on a line- or header-level button \(requires a selection of lines if header-level\), opens configurations in the target \(modal, slideout, or lineDrawer\). **reconfigure** includes the option to define location of buttons \(see productSearch above\) for more detail.
-   **addFavorites** can be on a line-level or header-level button \(requires a selection of lines if header-level\) and opens a window to describe and create a favorite from the selection. No other properties are supported.
-   **manageFavorites** opens the Favorites Manager in the specified target \(modal, slideout, or inline\).
-   **refreshSession** will check if the session has been modified, and if so, will refresh the sessionId and merge in changes.
-   **showTier** opens the Line Item Grid in fullscreen if target = fullScreen and location = lineItems. This works with any tier, but for the purposes of this feature, you’d fill the location with the tier variablename of the line items.

Currently, there is no validation of layout JSONs, and some property combinations are not supported. Unsupported combinations are likely to fail without indicating any errors.

## Implicit event calls

Some UI effects will, by their very nature, involve running certain related events. For example, triggering either the `productSearch` UI effect or the `reconfigure` UI effect will cause `upsertLines` event to run.

## Access conditions

A user’s ability to access a UI effect cannot be controlled directly, the way it can with events. There are no setting comparable to the following event settings:

![Transaction Manager: Layouts - UI effects](../images/cpq-txn-mgr-layouts-ui-effects-event-access.png)

However, the access conditions for a UI effect can be changed by its context in the transaction or by any related events.

When a UI effect has an implicit event associated with it, the access conditions of the event will determine the access conditions of the button and, in turn, the UI effect. So, if an administrator wanted to limit the conditions under which a `productSearch` UI effect could be triggered, then they could add those limitations to the `upsertLines` event.

A button on the line grid with the UI effect `reconfigure` will be hidden on lines that are not configurable. At the header level, it will only be enabled if every selected line is configurable.

Finally, if an event is used in addition to a UI effect on a button, access for both is determined by the intersection of their individual access-settings. In other words, both the UI effect and the event must be accessible for the button to be accessible. If one of the two is either disabled or hidden, then that is sufficient to disable or hide the entire button.

## Common cases

-   Product searching \(the `addLines` UI effect implicitly calls the `upsertLines` event\):
    -   JSON Code Snippet

        ```
        {
          "type": "button",
          "variableName": "addLines",
          "label": "Add Lines",
          "uiEffect": {
            "type": "productSearch",
            "target": "slideout"
          }
        }
        ```

    -   YAML Code Snippet

        ```
        type: button
        variableName: addLines
        label: Add Lines
        uiEffect:
          type: productSearch
          target: slideout
        ```

-   Line details drawer:
    -   JSON Code Snippet

        ```
        "lineLevelButtons": [
         {
           "icon": "settings",
           "label": "reconfig",
            "uiEffect": {
               "type": "lineDetail",
                "target": "lineDrawer"
              },
            "variableName": "reconfig"
          }
        ```

    -   YAML Code Snippet

        ```
        lineLevelButtons:
        -icon: settings
         label: reconfig
         uiEffect:
           type: lineDetail
           target: lineDrawer
         variableName: reconfig
        ```

-   Product search with favorites enabled:
    -   JSON Code Snippet

        ```
        {
          "type": "button",
          "variableName": "addLines",
          "label": "Add Lines",
          "uiEffect": {
            "type": "productSearch",
            "target": "slideout"
            "options": {
              "products": true,
              "favorites": true,
            }
          }
        }
        ```

    -   YAML Code Snippet

        ```
        type: button
        variableName: addLines
        label: Add Lines
        uiEffect:
          type: productSearch
          target: slideout
          options:
            products: true
            favorites: true
        ```

-   Open URL link in new tab:
    -   JSON Code Snippet

        ```
        {
          "columnorder": 1,
          "label": "Google it",
          "type": "event",
          "variableNane": "LinkToSite",
            "uieffect": {
                "type": "url",
                "target": "tab",
                "location": "https://google.com/search?q=I{txn.search}" 
            }
        }
        ```

    -   YAML Code Snippet

        ```
        columnorder: 1
        label: Google it
        type: event
        variableName: LinkToSite
        uieffect:
          type: url
          target: tab
          location: "https://google.com/search?q=I{txn.search}"
        ```

-   Refresh session:
    -   JSON Code Snippet

        ```
        {
          "type": "button",
          "variableName": "Refresh",
          "label": "Refresh",
          "uiEffect": {
            "type": "refreshSession"
          }
        }
        ```

    -   YAML Code Snippet

        ```
        type: button
        variableName: Refresh
        label: Refresh
        uiEffect:
          type: refreshSession
        ```

-   Reconfigure:
    -   JSON Code Snippet

        ```
        "lineLevelButtons": [
          {
             "icon": "settings",
             "label": "Reconfigure",
              "uiEffect": {
                  "type": "reconfigure",
                  "target": "modal"
               },
             "variableName": "reconfig"
          }
        ```

    -   YAML Code Snippet

        ```
        lineLevelButtons:
        -icon: settings
         label: Reconfigure
         uiEffect:
           type: reconfigure
           target: modal
         variableName: reconfig
        ```

-   Add to Favorites:
    -   JSON Code Snippet

        ```
        {
          "label": "Add To Favorites",
          "uiEffect": {
            "type": "addFavorite"
            },
          "variableName": "addFavorites"
        }
        ```

    -   YAML Code Snippet

        ```
        label: Add To Favorites
        uiEffect:
          type: addFavorite
        variableName: addFavorites
        ```

-   Manage Favorites:
    -   JSON Code Snippet

        ```
        {
          "label": "Manage Favorites",
          "uiEffect": {
            "type": "manageFavorites",
            "target": "modal"
            },
         "variableName": "manageFavorites"
        }
        ```

    -   YAML Code Snippet

        ```
        label: Manage Favorites
        uiEffect:
          type: manageFavorites
          target: slideout
        variableName: manageFavorites
        ```


