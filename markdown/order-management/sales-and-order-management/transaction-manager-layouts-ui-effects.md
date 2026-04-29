---
title: Transaction Manager: Layouts - UI effects
description: Learn how to add functionality to a button by programming UI effects in either YAML or JSON.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Transaction Manager: Layouts, Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager: Layouts - UI effects

Learn how to add functionality to a button by programming UI effects in either YAML or JSON.

In Transaction Manager, UI effects are layout elements that add functionalities to a button. Users can customize the UI effects that CPQ has established. However, users cannot create new UI effects as they do events.

If a UI effect and an event are present on the same button, the UI effect runs after the event runs.

## Example: Opening a list

As an example, a UI effect might enable a button to open a searchable list of products that could be added to a transaction. Here’s how that could be written in the layout:

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

A UI effect is defined by a combination of parameters. All UI effects have a type, and some may have a target, location, or options.

Each parameter has the following possible values:

-   **type**: **url**, **anchor**, **productSearch**, **lineDetail**, **reconfigure**, **addFavorite**, **manageFavorites**, **refreshSession**, **showTier**
-   **target**: **inline**, **tab**, **window**, **modal**, **slideout**, **lineDrawer**, **fullScreen**
-   **location**: \[a URL or an element id\]
-   **options**: \[depends on type\]

## Analysis of types

-   **url** requires a location in the form of a URL. Pressing the button takes users to the URL by way of a particular target \(inline, tab, window, modal iframe, or slideout iframe\). Using curly braces, admins can dynamically pass field values into the URL. Common use cases are passing a value to an output document or opening a record page in Salesforce.
-   **anchor** requires a location as an element ID in the layout. Pressing the button focuses on or scrolls to the element. Related parent elements are opened in tabs or an accordion structure. The target should be inline.
-   **productSearch** opens the product catalog in the target in either a slideout or a modal window. A variable name is required. The UI effect must be added to the gridHeaderButtons element. Options include the following:

    -   Show products list: **products** - **true** \(show\), **false** \(hide\)
    -   Show favorites list: **favorites** - **true** \(show\), false \(hide\)
    -   Location of button placement: **actionLocation** - **footer**, **header**, or both
        -   Defaults to **footer** if not specified
        -   Buttons include "Cancel", "Add Line", "Configure", and "Done Configuring"
    The following code shows products, hides favorites, and places buttons only on the header:

    ```
    ...
    "options": {
      "products": true,
      "favorites": false,
      "actionLocation": header
    },
    ...
    ```

-   **lineDetail** must be on a line-level button. Pressing the button opens the line-detail layout in the target \(**modal**, **slideout**, or **lineDrawer**\).
-   **exportLines** must be on a header-level button. Pressing the button exports the transaction lines to a CSV file.
-   **reconfigure** can be on a line-level or a header-level button. If the button is header-level, it requires a selection of lines. The **reconfigure** type opens configurations in the target \(**modal**, **slideout**, or **lineDrawer**\). **reconfigure** includes the option to define the location of buttons. For more detail, see **productSearch** above.
-   **addFavorites** can be on a line-level button or a header-level button. If the button is header-level, it requires a selection of lines. **addFavorites** opens a window to describe and create a favorite from the selection. No other properties are supported.

    **Note:** To share favorites, a tenant setting must be enabled. To enable favorites sharing, submit a support ticket.

-   **manageFavorites** opens the Favorites Manager in the specified target \(**modal**, **slideout**, or **inline**\).
-   **refreshSession** checks whether the session has been modified. If so, **refreshSession** refreshes the sessionId and merges in changes.
-   **showTier** opens the Line Item Grid in full screen if `target = fullScreen` and `location = lineItems`. **showTier** works with any tier, but for the purposes of this feature, the location should be filled in with the tier variable name of the line items.

Currently, layout JSONs are not validated, and some property combinations are not supported. Unsupported combinations are likely to fail without indicating errors.

## Implicit event calls

Some UI effects involve running related events. For example, triggering either the **productSearch** UI effect or the **reconfigure** UI effect runs the **upsertLines** event.

## Access conditions

A user’s ability to access a UI effect cannot be controlled in the same way as events. There are no setting comparable to the following event settings:

![Transaction Manager: Layouts - UI effects](../images/cpq-txn-mgr-layouts-ui-effects-event-access.png)

However, the access conditions for a UI effect can be changed by its context in the transaction or by related events.

When a UI effect has an implicit event associated with it, the access conditions of the event determine the access conditions of the button and, in turn, the UI effect. Therefore, if an administrator wants to limit the conditions under which a **productSearch** UI effect can be triggered, they can add those limitations to the **upsertLines** event.

A button on the line grid that has the **reconfigure** UI effect is hidden on lines that are not configurable. At the header level, it is enabled only when every selected line is configurable.

If an event and a UI effect are both present on a button, access for both is determined by the intersection of their individual access settings. For the button to be accessible, both the UI effect and the event must be accessible. If either is disabled or hidden, the entire button is disabled or hidden.

## Common cases

-   Product searching \(the `addLines` UI effect implicitly calls the `upsertLines` event\):
    -   JSON code snippet

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

    -   YAML code snippet

        ```
        type: button
        variableName: addLines
        label: Add Lines
        uiEffect:
          type: productSearch
          target: slideout
        ```

-   Line details drawer:
    -   JSON code snippet

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

    -   YAML code snippet

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
    -   JSON code snippet

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

    -   YAML code snippet

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
    -   JSON code snippet

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

    -   YAML code snippet

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
    -   JSON code snippet

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

    -   YAML code snippet

        ```
        type: button
        variableName: Refresh
        label: Refresh
        uiEffect:
          type: refreshSession
        ```

-   Reconfigure:
    -   JSON code snippet

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

    -   YAML code snippet

        ```
        lineLevelButtons:
        -icon: settings
         label: Reconfigure
         uiEffect:
           type: reconfigure
           target: modal
         variableName: reconfig
        ```

-   Add to favorites:
    -   JSON code snippet

        ```
        {
          "label": "Add To Favorites",
          "uiEffect": {
            "type": "addFavorite"
            },
          "variableName": "addFavorites"
        }
        ```

    -   YAML code snippet

        ```
        label: Add To Favorites
        uiEffect:
          type: addFavorite
        variableName: addFavorites
        ```

-   Manage favorites:
    -   JSON code snippet

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

    -   YAML code snippet

        ```
        label: Manage Favorites
        uiEffect:
          type: manageFavorites
          target: slideout
        variableName: manageFavorites
        ```

-   Export lines YAML snippet:

    ```
    label: Export Lines
    uiEffect:
      type: exportLines
    variableName: exportLines
    ```


