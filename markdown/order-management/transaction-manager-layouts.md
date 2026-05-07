---
title: Transaction Manager: Layouts
description: Layouts in Transaction Manager can be managed in the Admin UI by using the layout editor or directly in the YAML format. This topic provides the details of the various layout structures, fields, buttons, and effects, and provides code snippets.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Layouts

Layouts in Transaction Manager can be managed in the Admin UI by using the layout editor or directly in the YAML format. This topic provides the details of the various layout structures, fields, buttons, and effects, and provides code snippets.

In Transaction Manager, layouts retain much of the look and feel of the configuration user experience. In January 2026, a visual layout editor was introduced in Transaction Manager. Layouts can be edited in YAML format; however, the option to edit in JSON was retired in favor of the visual editor. Fields, events, UI effects, and lines are available for display and are detailed below.

## Layout formats \(visual and YAML\)

Layouts can be managed in either the visual editor or in YAML. The visual editor is selected by default, but admins can toggle to YAML.

## Creating a new layout

To create a new layout, navigate to the Transaction Manager Admin UI, click **Layouts** in the menu on the left, and then click **+ Add Layout** to add a new layout to the blueprint.

An existing layout can be copied by using the Save As function in the layout.

![Transaction Manager: layouts](../images/cpq-txn-mgr-layouts-new-1.png)

The layout requires a name and a variable name. Click in the Name field, enter the name of the new layout, and click **Save** to proceed. Although the name can later be edited in the layout, the variable name is not editable after the layout is saved.

When the layout is saved, the visual editor opens. The default layout includes a few key items, such as the main tier, a line item grid, and a product search capability.

## Layout names and stage association

The layout's variable name is used to map layouts to stages. To map a layout to a stage, use the stage name as the layout name. A layout named "layout" maps to any stage that has no layout mapped to it. The text `default` is appended to all layout variables.

For example, when the stages are named Draft, Approved, and Fulfilled, and the layouts are named Draft and Layout, the mapping is as follows:

|Stage|Layout name|
|-----|-----------|
|Draft|draft|
|Approved|layout|
|Fulfilled|layout|

The optional Line Detail layout displays details on a selected line in the line item grid. This view is initiated via the Line Detail UI effect. This layout requires its own layout file and the variable name must end with `_linedetail`. These layouts follow the same mapping as stages. Continuing the example above, if you want a Line Detail layout for the Draft stage, the name must be `draft_linedetail`.

![Transaction Manager: view of new layout](../images/cpq-txn-mgr-layouts-view-of-new.png)

The YAML code for the layout can be accessed by using the view toggle in the subheader. Admins can update the layout either by using the visual editor or by directly editing the YAML code. The YAML for each element can also be accessed in the Raw Value section of the element properties.

The **Save** button saves the current version of the layout. However, the blueprint must be deployed for the new version to be used in runtime. If there are errors in the layout, the Save button is disabled. To identify errors, select the error messages button in the subheader. In the YAML view, look for red marks on the right side of the display that indicate the location of the error.

![Transaction Manager layout](../images/cpq-txn-mgr-layouts-yaml-view.png)

## General layout information

Click the gear \(settings\) icon in the subheader to access the layout settings.

![Transaction Manager: layout properties dialog](../images/cpq-txn-mgr-layouts-properties.png)

Settings include the following:

-   **Branding**

    Customize the header.

-   **Currency Display**

    Set the currency display style: code, symbol, or neither.

-   **When price is 0, display**

    Set the behavior when the price is zero.

-   **When price is undefined, display**

    Set the behavior when the price is undefined.

-   **Allow selecting disabled options**

    Allow the user to select disabled items from a picklist. Use case is to display an explanation message if selected.

-   **Highlight field changes**

    When enabled, fields are briefly highlighted. Recommended when fields are updated via rules or integrations or if concurrent users are expected.

-   **Hide Header**

    Hides the header section of the layout.


## Theming

Transaction Manager layouts can be customized with themes. Themes can be enabled on the Customize Theme tab. For more information, see [Customizing CPQ with themes](customizing-cpq-with-themes.md).

## Stage progress chevrons

The Stages Progress Chevron component displays a horizontal chevron bar to visually represent a transaction’s progression through stages. It can be defined statically or dynamically and is configurable through layout YAML. For more information, see [Transaction Manager: Layouts - The stages progress chevron](transaction-manager-layouts-the-stages-progress-chevron.md).

## Tiers

Tiers are sections of information for your transaction. Tiers are the top of the hierarchical structure of a Transaction Manager layout. You can use tiers to organize your transaction information so that it is easier to find and understand for the buyside user. Columnsets, tiers, or a line item grid can be added within a tier, but a line item grid must be the only element in a tier.

Tier types include Accordion, Expandable, Tabs, Vertical tabs, Headings, and Pages. The type and depth of a tier can be configured on the Tier Definition tab.

## Columnsets

As in configuration, columnsets are objects in the layout that enable you to organize fields and events on the runtime display. Fields and events can be arranged horizontally in a columnset. Fields and events are arranged vertically by using multiple columnsets in the same tier. You can add fields, images, text, and buttons within a columnset.

## Columnsets: fields

Fields are one type of object that can be placed in the Elements array of a columnset. Fields provide the data input source for the transaction. Fields can be added, removed, and ordered in a columnset on the Arrange Layout tab. Once added, additional field properties can be set on the Edit Field Info tab.

On the Edit Field Info tab, changing the field display type to "text area" lets the user resize the field.

## ColumnSets: events

Events are objects that cause certain actions to be taken. Events are typically represented in the layout as a button. To add an event, add a button to a columnset, and then toggle the **Event Button** setting. Once it is enabled, an event can be selected from the Event picklist.

![Transaction Manager: button properties with event enabled](../images/cpq-txn-mgr-layouts-button-properties-1.png)

## Line item grid

The Line Item Grid object displays the product information that is included in the transaction. Detailed product information and pricing information is displayed in the Line Item Grid object.

In the layout editor, a line item grid is included by default, and has the following three sections:

-   **Line item grid header**

    Buttons can be added and display atop the line item grid in runtime.

-   **Line item grid column**

    Fields can be added, removed, and ordered and display as columns on the line item grid.

-   **Line level buttons**

    Buttons can be added and display on each line in the line item grid.


The line item grid has the following layout properties, each of which is enabled when its value is `true`. The properties must be defined in the main YAML editor.

-   **showLineNumbers**: enables user-friendly line numbers
-   **supportLongText**: a Line Item Grid field property that enables a popover on the field when selected
-   **autoScrollIntoView**: smooths the scroll interaction between the transaction body and LIG

YAML code snippet:

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
          - label: Add To Favorites
            uiEffect:
              type: addFavorite
            variableName: addFavorites
          - label: Reconfigure Lines
            uiEffect:
              type: reconfigure
              target: slideout
            variableName: reconfig
        autoScrollIntoView: true
      variableName: lineItems

```

Line-level event buttons can have an icon defined. Icons must be defined in the YAML code in either the Raw Value section of the line button properties or in the main YAML editor. Buttons can use specified icons from the SLDS Utility library.

<table id="table_ykm_jll_hhc"><tbody><tr><td>

![hollow gear icon](../images/cpq-txn-mgr-sldc-icon-automate.png)automate

</td><td>

![icon of three people and a check mark](../images/cpq-txn-mgr-sldc-icon-buyer-group-qualifier.png)buyer\_group\_qualifier

</td><td>

![chevron pointing down](../images/cpq-txn-mgr-sldc-icon-chevron-down.png)chevrondown

</td><td>

![chevron pointing left](../images/cpq-txn-mgr-sldc-icon-chevronleft.png)chevronleft

</td><td>

![chevron pointing right](../images/cpq-txn-mgr-sldc-icon-chevronright.png)chevronright

</td><td>

![chevron pointing up](../images/cpq-txn-mgr-sldc-icon-chevronup.png)chevronup

</td></tr><tr><td>

![option button](../images/cpq-txn-mgr-sldc-icon-choice.png)choice

</td><td>

![white x on solid background](../images/cpq-txn-mgr-sldc-icon-clear.png)clear

</td><td>

![clock icon](../images/cpq-txn-mgr-sldc-icon-clock.png)clock

</td><td>

![x icon](../images/cpq-txn-mgr-sldc-icon-close.png)close

</td><td>

![wrench icon](../images/cpq-txn-mgr-sldc-icon-custom-apps.png)custom\_apps

</td><td>

![trash can icon](../images/cpq-txn-mgr-sldc-icon-delete.png)delete

</td></tr><tr><td>

![triangle pointing down](../images/cpq-txn-mgr-sldc-icon-down.png)down

</td><td>

![pencil icon](../images/cpq-txn-mgr-sldc-icon-edit.png)edit

</td><td>

![star icon](../images/cpq-txn-mgr-sldc-icon-favorite.png)favorite

</td><td>

![triangle pointing left](../images/cpq-txn-mgr-sldc-icon-left.png)left

</td><td>

![icon of lightning bolt and gear](../images/cpq-txn-mgr-sldc-icon-lightning-extension.png)lightning\_extension

</td><td>

![triangle pointing right](../images/cpq-txn-mgr-sldc-icon-right.png)right

</td></tr><tr><td>

![question mark](../images/cpq-txn-mgr-sldc-icon-question.png)question

</td><td>

![magnifying glass icon](../images/cpq-txn-mgr-sldc-icon-search.png)search

</td><td>

![solid gear icon](../images/cpq-txn-mgr-sldc-icon-settings.png)settings

</td><td>

![icon of arrow pointing at center of target](../images/cpq-txn-mgr-sldc-icon-target-mode.png)target\_mode

</td><td>

![three horizontal dots](../images/cpq-txn-mgr-sldc-icon-threedots.png)threedots

</td><td>

![three vertical dots](../images/cpq-txn-mgr-sldc-icon-threedots-vertical.png)threedots\_vertical

</td></tr></tbody>
</table>YAML code snippet:

```
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
```

Finally, there are three ways to display line numbers in the line item grid: by means of a layout property, or by either of two system fields:

-   The **showLineNumbers** layout property. Because it performs efficiently and has no limit to the number of lines, this is the recommended method.

    **showLineNumbers** displays sequential line numbers for visible lines. The numbering resets when a filter or a search applies to the line item grid.

-   The **txn.line.orderNumber** system field

    **txn.line.orderNumber** displays hierarchical line numbering for all lines \(for example: 1, 1.1, 2, 2.1, 2.2, 2.2.1\). The numbering does not reset when a filter or a search applies to the line item grid. Numbering can be applied to up to 2,000 lines.

    The field has the same layout properties as other line-level fields and can be added to the layout in the `lineGrid` section of the layout.

    To enable this field, submit a request to customer support.

-   The **txn.line.number** system field

    **txn.line.number** displays sequential line numbering for all lines \(that is, 1, 2, 3, and so on\).

    As with **txn.line.orderNumber**, numbering does not reset when a filter or a search is applied, and there is a maximum of 2,000 lines. The field has the same layout properties as other line-level fields and can be added to the layout in the `lineGrid` section of the layout. To enable this field, submit a request to customer support.


## Product list search

The Product List Search object provides a set of layout properties for the product list search results in the add lines/product search flow. By default, the product list search is added via the **Add Lines** UI effect button. Fields can be added, removed, and reordered in the Product Search object to define the runtime UI. Related properties can be found in three locations:

-   The button properties of the button with the Product Search UI effect
-   Product list search properties accessed via the Product Search object in the layout
-   Each of the fields in the Product List Search object on the layout

UI effect button properties include:

-   **UI Effect Target**

    Options for Product Search display

-   **Show Products**

    Adds the Products tab to the product search

-   **Show Favorites**

    Adds the User Favorites tab to the product search

-   **Action Location**

    The location of action buttons on the product search display


![Transaction Manager: button properties for the product list search object](../images/cpq-txn-mgr-layouts-button-properties-2.png)

The properties of the Product List Search object include:

-   Primary Default Sort: Define up to two parameters used to sort search results. The following fields can be used as parameters:

    -   modified
    -   created
    -   Name \(default if no parameters are defined\)
    -   partnerId
    -   productCode
    -   description
    -   unitPrice
    -   externallyConfigurable
    The order can be defined per parameter as `asc` or `desc`.

-   Search on Submit: Determines whether search results are updated as the user types or only when the user clicks **Submit**.

![Transaction Manager: product list properties](../images/cpq-txn-mgr-layouts-prod-list-properties.png)

Field-level properties include:

-   **Column Width**

    CSS compatible value to define width

-   **Alignment**

    Alignment of header and values

-   **Enable Sorting**

    When enabled, allows column to be sorted

-   **Enable Long Text Popover**

    When enabled, a popover is displayed when value in field is selected


![Transaction Manager: product list column properties](../images/cpq-txn-mgr-layouts-prod-list-col-properties.png)

## UI effects

UI effects are layout elements that add specific functionalities to a Button. UI effects include:

-   **URL**

    Opens the associated URL inline, in a modal window, in a slideout panel, or in a new tab or window.

-   **Anchor**

    Navigates to specified location in the transaction

-   **Product search**

    Opens the product catalog, starting the Add Products flow

-   **Line detail**

    Opens the line-detail layout

-   **Reconfigure**

    Opens the selected products to configuration UX

-   **Add favorite**

    Opens a modal window to describe and create a favorite from the selection

-   **Manage favorites**

    Opens the Favorites Manager

-   **Refresh session**

    Checks whether the session has been modified, and if so, refreshes the sessionId and merges changes.

-   **Export lines**

    Exports to a CSV file all lines in a transaction that meet the sort, filter, and show/hide column settings.


## YAML code snippets

Layout properties:

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

Tiers:

```
# Layout
layout:
  label: layoutsection
  variableName: layoutsection
  tiers:
    - label: tier1
      variableName: tier1
      depth: 1
```

Columnsets:

```
columnSets:
        - elements:
            - type: field
              columnOrder: 1
              variableName: txn.opportunity.id
          variableName: col1
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

Columnset with events:

```
To be added
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


[Transaction Manager: Layouts - UI effects](transaction-manager-layouts-ui-effects.md)

[Transaction Manager: Layouts - Theming options](transaction-manager-layouts-theming-options.md)

