---
title: ServiceNow Quote Experience layout UI effects
description: Reference for UI effect types, parameters, access conditions, and YAML and JSON code examples for configuring button behavior in ServiceNow Quote Experience layouts in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-ui-effects.html
release: australia
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 4
breadcrumb: [Quote transaction layouts, Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# ServiceNow Quote Experience layout UI effects

Reference for UI effect types, parameters, access conditions, and YAML and JSON code examples for configuring button behavior in ServiceNow Quote Experience layouts in ServiceNow CPQ.

## UI effects overview

UI effects are layout elements that add specific functionality to a button. Administrators can customize existing UI effects but can't create new ones. When a UI effect and an event are both present on the same button, the UI effect runs after the event.

A UI effect is defined by a combination of parameters. All UI effects have a `type`. Some also have a `target`, `location`, or `options`.

## UI effect parameters

|Parameter|Possible values|
|---------|---------------|
|`type`|`url`, `anchor`, `productSearch`, `lineDetail`, `reconfigure`, `addFavorite`, `manageFavorites`, `refreshSession`, `showTier`, `exportLines`|
|`target`|`inline`, `tab`, `window`, `modal`, `slideout`, `lineDrawer`, `fullScreen`|
|`location`|A URL or an element ID in the layout.|
|`options`|Depends on the UI effect type. See the following type reference.|

**Note:** Layout JSON is not validated and some parameter combinations aren't supported. Unsupported combinations may fail without indicating errors.

## UI effect type reference

-   **`url`**

    Opens a URL inline, in a tab, in a window, or in a modal or slideout iframe. Requires a `location` value containing the URL. Use curly braces to pass field values dynamically into the URL — for example, `https://example.com/search?q={txn.custom.searchTerm}`. Common use cases include passing values to output documents or opening record pages in external systems.

-   **`anchor`**

    Navigates to a specified element ID in the layout. Focuses or scrolls to the element and opens related parent elements in tabs or an accordion structure. Set `target` to `inline`. Requires a `location` value containing the element ID.

-   **`productSearch`**

    Opens the product catalog and starts the Add Products flow. Implicitly runs the `upsertLines` event. Must be added to the `gridHeaderButtons` element. Target options: `slideout` or `modal`.

    Options:

    -   `products: true` — shows the Products tab.
    -   `favorites: true` — shows the User Favorites tab.
    -   `actionLocation: footer | header | both` — placement of the action buttons \(Add Line, Configure, Done Configuring, Cancel\). Defaults to `footer` if not specified.
-   **`lineDetail`**

    Opens the line detail layout for a selected line. Must be on a line-level button. Target options: `modal`, `slideout`, `lineDrawer`.

-   **`reconfigure`**

    Opens selected products in the Configurator for reconfiguration. Implicitly runs the `upsertLines` event. Can be on a line-level or header-level button. At the header level, requires a selection of lines. Target options: `modal`, `slideout`, `lineDrawer`. Supports the same `actionLocation` option as `productSearch`.

-   **`addFavorite`**

    Opens a window to describe and create a favorite from the line selection. Can be on a line-level or header-level button. At the header level, requires a selection of lines. No other properties are supported.

    **Note:** To share favorites across users, a tenant setting must be enabled. Contact customer support to enable favorites sharing.

-   **`manageFavorites`**

    Opens the Favorites Manager. Target options: `modal`, `slideout`, `inline`.

-   **`refreshSession`**

    Checks whether the session has been modified and, if so, refreshes the session ID and merges changes. No additional parameters required.

-   **`exportLines`**

    Exports to a CSV file all lines that meet the current sort, filter, and column visibility settings. Must be on a header-level button. No additional parameters required.

-   **`showTier`**

    Opens a tier in full screen. To open the line item grid in full screen, set `target: fullScreen` and `location` to the tier variable name of the line items \(typically `lineItems`\). Works with any tier.


## Implicit event calls

Some UI effects run a related event automatically. The `productSearch` and `reconfigure` UI effects both implicitly call the `upsertLines` event when triggered.

## Access conditions

Access to a UI effect can't be controlled in the same way as access to an event. There are no UI settings comparable to the event access settings for UI effects directly.

However, access to a UI effect can be changed by its context or by related events.

-   When a UI effect has an implicit event associated with it, the access conditions of that event determine the access conditions of the button and UI effect. To restrict when a `productSearch` UI effect can be triggered, apply those restrictions to the `upsertLines` event.
-   A `reconfigure` button in the line item grid is hidden on lines that aren't configurable. At the header level, it is enabled only when every selected line is configurable.
-   When a button has both an event and a UI effect, access is determined by the intersection of their individual access settings. If either the event or the UI effect is disabled or hidden, the entire button is disabled or hidden.

## Code examples

Product search \(YAML\):

```
type: button
variableName: addLines
label: Add Lines
uiEffect:
  type: productSearch
  target: slideout
```

Product search with favorites enabled \(YAML\):

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

Line details drawer \(YAML\):

```
lineLevelButtons:
  - icon: settings
    label: reconfig
    uiEffect:
      type: lineDetail
      target: lineDrawer
    variableName: reconfig
```

Reconfigure \(YAML\):

```
lineLevelButtons:
  - icon: settings
    label: Reconfigure
    uiEffect:
      type: reconfigure
      target: modal
    variableName: reconfig
```

Open URL in new tab with dynamic field value \(YAML\):

```
columnorder: 1
label: Google it
type: event
variableName: LinkToSite
uieffect:
  type: url
  target: tab
  location: "https://google.com/search?q={txn.custom.search}"
```

Add to favorites \(YAML\):

```
label: Add To Favorites
uiEffect:
  type: addFavorite
variableName: addFavorites
```

Manage favorites \(YAML\):

```
label: Manage Favorites
uiEffect:
  type: manageFavorites
  target: slideout
variableName: manageFavorites
```

Refresh session \(YAML\):

```
type: button
variableName: Refresh
label: Refresh
uiEffect:
  type: refreshSession
```

Export lines \(YAML\):

```
label: Export Lines
uiEffect:
  type: exportLines
variableName: exportLines
```

**Related topics**  


[Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md)

[Create a quote transaction layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-layout.md)

