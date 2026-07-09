---
title: Quote transaction layouts
description: Layouts define the quote user interface in ServiceNow Quote Experience, controlling which fields, events, and UI effects are visible and how the quote is organized for users in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-layouts.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 11
breadcrumb: [Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Quote transaction layouts

Layouts define the quote user interface in ServiceNow Quote Experience, controlling which fields, events, and UI effects are visible and how the quote is organized for users in ServiceNow CPQ.

Layouts in ServiceNow Quote Experience retain much of the look and feel of the configuration experience. Layouts can be managed in the administration interface using the visual layout editor or directly in YAML. The visual layout editor is selected by default. The option to edit layouts in JSON is retired in favor of the visual editor.

## Layout formats

Layouts can be edited using the visual editor or in YAML. The visual editor provides a graphical interface for building layouts without editing code. Administrators can toggle to YAML using the view toggle in the layout subheader. The YAML for each element is also accessible in the Raw Value section of the element properties. Changes take effect when the layout is saved and the blueprint is deployed.

If errors exist in the YAML, the **Save** button is disabled. To identify errors, select the error messages button in the subheader, or check for red marks in the YAML view .

## Layout and stage mapping

A layout's variable name maps it to a stage. To associate a layout with a specific stage, use the stage variable name as the layout name. A layout named `layout` maps to any stage that has no specific layout defined. The text `default` is appended to all layout variable names.

The following example shows how stages map to layouts when stages are named Draft, Approved, and Fulfilled, and layouts are named Draft and Layout.

|Stage|Layout used|
|-----|-----------|
|Draft|`draft`|
|Approved|`layout`|
|Fulfilled|`layout`|

The Line Detail layout displays details of a selected line in the quote lines grid, opened via the Line Detail UI effect. Its variable name must end with `_linedetail` and follows the same stage mapping convention. For example, a Line Detail layout for the Draft stage must be named `draft_linedetail`.

## Layout settings

Access layout settings by selecting the gear icon in the layout subheader. The following settings are available.

-   **Branding**

    Customizes the quote header appearance.

-   **Currency Display**

    Sets the currency display style: code, symbol, or neither.

-   **When price is 0, display**

    Sets the behavior when a price value is zero.

-   **When price is undefined, display**

    Sets the behavior when a price value is undefined.

-   **Allow selecting disabled options**

    Users can select disabled picklist options. Useful for displaying an explanation message when a disabled option is selected.

-   **Highlight field changes**

    Briefly highlights fields when their values are updated by rules or integrations. Enable this setting when concurrent users are expected or when fields update frequently.

-   **Hide Header**

    Hides the header section of the layout.


## Layout structure

Layouts are organized using tiers, columnsets, and a line item grid.

-   **Tiers**

    Tiers are the top-level sections of the layout hierarchy. Use tiers to organize transaction information into logical groups that are easier to find and understand. Columnsets, nested tiers, or a line item grid can be placed within a tier. A line item grid must be the only element in its tier. Tier types include Accordion, Expandable, Tabs, Vertical tabs, Headings, and Pages. The type and depth of a tier are configured on the Tier Definition tab.

-   **Columnsets**

    Columnsets organize fields and events horizontally within a tier. Multiple columnsets in the same tier arrange content vertically. Fields, images, text, and buttons can be added within a columnset.

    Fields are added to the elements array of a columnset. After adding a field, additional field properties can be set on the Edit Field Info tab. Changing a field display type to "text area" enables users to resize the field .

    Events are represented as buttons in a columnset. To add an event, add a button to a columnset and enable the **Event Button** setting, then select the event from the Event picklist.

-   **Line item grid**

    The line item grid displays the product and pricing information for the transaction lines. By default, the layout editor includes a line item grid with three sections:

    -   **Line item grid header** — buttons that appear above the grid at runtime.
    -   **Line item grid column** — fields that appear as columns in the grid.
    -   **Line level buttons** — buttons that appear on each individual line in the grid.
    The following layout properties apply to the line item grid and must be defined in the main YAML editor. Each property is enabled when its value is `true`.

    -   `showLineNumbers` — enables user-friendly sequential line numbers for visible lines. Numbering resets when a filter or search is applied.
    -   `supportLongText` — enables a popover on a field when the user selects it.
    -   `autoScrollIntoView` — automatically scrolls the view to keep the transaction body and line item grid in sync .

## Line numbering options

Three options are available for displaying line numbers in the quote lines grid. The `showLineNumbers` layout property is the preferred option for most implementations: it performs efficiently and has no line limit .

-   **`showLineNumbers` layout property**

    Displays sequential line numbers for visible lines \(1, 2, 3\). Numbers reset when a filter or search is applied to the grid. No line limit. Use this method when there is no line limit requirement.

-   **`txn.line.orderNumber` system field**

    Displays hierarchical line numbering for all lines — for example, 1, 1.1, 2, 2.1, 2.2, 2.2.1. Numbers do not reset when a filter or search is applied. Maximum of 2,000 lines. The field has the same layout properties as other line-level fields and is added in the `lineGrid` section of the layout.

    **Note:** To enable this field, submit a request to customer support through the ServiceNow CPQ Support portal.

-   **`txn.line.number` system field**

    Displays sequential line numbering for all lines \(1, 2, 3\). Numbers do not reset when a filter or search is applied. Maximum of 2,000 lines. The field has the same layout properties as other line-level fields and is added in the `lineGrid` section of the layout.

    **Note:** To enable this field, submit a request to customer support through the ServiceNow CPQ Support portal.


## Line-level button icons

Line-level event buttons in the line item grid can display an icon from the SLDS Utility library. Icons must be defined in the YAML, either in the Raw Value section of the line button properties or in the main YAML editor using the `icon` property.

|Icon value|Description|
|----------|-----------|
|`automate`|Hollow gear|
|`buyer_group_qualifier`|Three people with a check mark|
|`chevrondown`|Chevron pointing down|
|`chevronleft`|Chevron pointing left|
|`chevronright`|Chevron pointing right|
|`chevronup`|Chevron pointing up|
|`choice`|Option button|
|`clear`|White X on solid background|
|`clock`|Clock|
|`close`|X icon|
|`custom_apps`|Wrench|
|`delete`|Trash can|
|`down`|Triangle pointing down|
|`edit`|Pencil|
|`favorite`|Star|
|`left`|Triangle pointing left|
|`lightning_extension`|Lightning bolt and gear|
|`right`|Triangle pointing right|
|`question`|Question mark|
|`search`|Magnifying glass|
|`settings`|Solid gear|
|`target_mode`|Arrow pointing at center of target|
|`threedots`|Three horizontal dots|
|`threedots_vertical`|Three vertical dots|

## Product list search

The Product List Search object defines the runtime UI for the add lines and product search flow. Properties are configured in three locations.

-   **UI effect button properties**

    Configure on the button that carries the Product Search UI effect.

    -   **UI Effect Target** — how the product search opens \(slideout or modal\).
    -   **Show Products** — adds the Products tab to the search.
    -   **Show Favorites** — adds the User Favorites tab to the search.
    -   **Action Location** — placement of action buttons on the product search display \(footer, header, or both\).
-   **Product List Search object properties**

    Configure on the Product Search object in the layout.

    -   **Primary Default Sort** — up to two sort parameters. Available fields: `modified`, `created`, `Name` \(default\), `partnerId`, `productCode`, `description`, `unitPrice`, `externallyConfigurable`. Sort order per parameter: `asc` or `desc`.
    -   **Search on Submit** — determines whether search results update as the user types or only when the user selects **Submit**.
-   **Field-level properties**

    Configure on each field in the Product List Search object.

    -   **Column Width** — CSS-compatible value to define the column width.
    -   **Alignment** — alignment of the column header and values.
    -   **Enable Sorting** — when enabled, the column can be sorted .
    -   **Enable Long Text Popover** — when enabled, displays a popover when the user selects a value in the field.

## UI effects

UI effects add specific functionality to a layout button. Users can customize existing UI effects but cannot create new ones. When a UI effect and an event are both present on the same button, the UI effect runs after the event. For full parameter reference, access conditions, and code examples, see [ServiceNow Quote Experience layout UI effects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-ui-effects.md).

The following UI effect types are available.

-   **URL**

    Opens the associated URL inline, in a modal, in a slideout panel, or in a new tab or window. Field values can be passed dynamically into the URL using curly braces.

-   **Anchor**

    Navigates to a specified element ID within the transaction layout. Opens related parent elements in tabs or an accordion structure.

-   **Product search**

    Opens the product catalog and starts the Add Products flow. Must be added to a `gridHeaderButtons` element. Implicitly runs the `upsertLines` event.

-   **Line detail**

    Opens the line detail layout for a selected line. Must be on a line-level button. Opens in a modal, slideout, or line drawer.

-   **Reconfigure**

    Opens selected products in the Configurator for reconfiguration. Can be on a line-level or header-level button. At the header level, requires a selection of lines. Implicitly runs the `upsertLines` event.

-   **Add favorite**

    Opens a window to describe and create a favorite from the selection. Can be on a line-level or header-level button. At the header level, requires a selection of lines.

    **Note:** To share favorites across users, a tenant setting must be enabled. Contact customer support to enable favorites sharing.

-   **Manage favorites**

    Opens the Favorites Manager in a modal, slideout, or inline view.

-   **Refresh session**

    Checks whether the session has been modified and, if so, refreshes the session ID and merges changes.

-   **Export lines**

    Exports to a CSV file all lines that meet the current sort, filter, and column visibility settings. Must be on a header-level button.

-   **Show tier**

    Opens the line item grid in full screen when `target = fullScreen` and `location = lineItems`. Can work with any tier; for full screen, set the location to the tier variable name of the line items.


## Theming

ServiceNow Quote Experience layouts can be customized with themes by setting properties in the layout YAML or JSON. Themes are enabled using the Customize Theme tab. For the full theme property reference, including button, input, label, and header styling, see [ServiceNow Quote Experience layout UI effects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-ui-effects.md).

## Stage progress chevron

The Stages Progress Chevron component displays a horizontal chevron bar that shows a transaction's progression through its stages. It can be defined statically using a fixed stage list or dynamically using custom picklist fields, and is configured through the layout YAML or JSON. For configuration options, combination rules, and CSS theming variables, see [Stage progress chevron](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-stage-progress-chevron.md).

## YAML reference snippets

Layout structure:

```
# Layout version
version: 1
# Layout identifiers
label: Example layout
variableName: default_ExampleLayout
# Tier definitions
tierDef:
  - depth: 1
    representation: BasicContainer
# Layout
layout:
  label: layoutsection
  variableName: layoutsection
  tiers:
    - label: tier1
      variableName: tier1
      depth: 1
```

Columnset with fields:

```
columnSets:
  - elements:
      - type: field
        columnOrder: 1
        variableName: txn.opportunity.id
      - type: field
        columnOrder: 1
        variableName: txn.custom.opportunityName
      - type: field
        classInfo: mw20
        columnOrder: 1
        variableName: txn.custom.primaryContact
    variableName: col1
```

Field properties:

```
fields:
  - type: Text
    label: Custom line field
    variableName: txn.line.custom.customText
  - type: ReadOnlyText
    label: TXN Number
    variableName: txn.custom.tXNNumber
```

Line item grid with line-level and header buttons:

```
- depth: 1
  label: Line Items
  lineGrid:
    columns:
      - order: 1
        variableName: txn.line.product.name
      - order: 2
        variableName: txn.line.product.partnerId
    showLineNumbers: true
    lineLevelButtons:
      - icon: settings
        label: Line Details
        uiEffect:
          type: lineDetail
          target: slideout
        variableName: reconfig
      - event: cloneLine
        label: Clone Lines
        variableName: cloneLine
      - label: Add To Favorites
        uiEffect:
          type: addFavorite
        variableName: addFavorites
    gridHeaderButtons:
      - label: Add Lines
        uiEffect:
          type: productSearch
          target: slideout
          options:
            products: true
            favorites: true
        variableName: productSearch
      - label: Reconfigure Lines
        uiEffect:
          type: reconfigure
          target: slideout
        variableName: reconfig
    autoScrollIntoView: true
  variableName: lineItems
```

Product list search:

```
productList:
  columns:
    - label: Product ID
      sortable: true
      variableName: id
    - label: Product Name
      variableName: name
    - label: Product description
      variableName: description
      supportLongText: true
    - label: Price
      variableName: unitPrice
  defaultSort:
    - externallyConfigurable,desc
    - name
```

**Related topics**  


[Create a quote transaction layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-layout.md)

[ServiceNow Quote Experience layout UI effects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-ui-effects.md)

[Stage progress chevron](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-stage-progress-chevron.md)

