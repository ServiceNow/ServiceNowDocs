---
title: Transaction Manager: Layouts
description: Layouts in Transaction Manager can be managed in the Admin UI or via API calls in either JSON or YAML formats. This topic provides the details of the various fields, buttons, and effects, and provides code snippets.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 13
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Layouts

Layouts in Transaction Manager can be managed in the Admin UI or via API calls in either JSON or YAML formats. This topic provides the details of the various fields, buttons, and effects, and provides code snippets.

In Transaction Manager, layouts retain much of the look and feel of the configuration user experience. These layouts are created and managed in either JSON or YAML formats and can be managed in the Admin UI or via API. Transaction fields, event buttons, UI effects, and transaction lines are available for display and are detailed below.

When you create a layout in Transaction Manager, you give the layout a name and a variable name. The Name value can be whatever you would like it to be. However, the variable name of the layout file must follow one of the following naming conventions in order for the software to locate the layout as part of the Blueprint.

Transaction layout files need to have their Layout File variable name be in either one of the two following formats:

-   &lt;blueprintVarName&gt;\_&lt;stageVarName&gt;

    Examples:`default_draft.yaml`OR`default_draft.json`

-   &lt;blueprintVarName&gt;\_layout

    Examples:`default_layout.yaml`OR`default_layout.json`


An optional layout feature is the Line Detail layout, which displays details on a selected line in the Line Item Grid. This view is initiated via the Line Detail UI effect. This layout requires its own layout file. The variable name of the Transaction Line Detail layout file needs to be in one of the following two formats:

-   &lt;blueprintVarName&gt;\_&lt;stageVarName&gt;\_linedetail

    Examples:`default_draft_linedetail.yaml`or`default_draft_linedetail.json`

-   &lt;blueprintVarName&gt;\_layout\_linedetail

    Examples:`default_layout_linedetail.yaml`or`default_layout_linedetail.json`


For more information about the Line Detail UI effect, see [Transaction Manager: Layouts - UI effects](transaction-manager-layouts-ui-effects.md).

## Layout formats \(JSON and YAML\)

Layouts can be managed in either JSON or YAML. This is a step in our progression towards a visual-based layout editor, as the YAML data format will serve as the underlying data for the visual editor. YAML will be selected by default, but Admins can toggle to JSON.

YAML provides several benefits, including:

-   Better readability: fewer extraneous wrappers like quotes and brackets
-   Schemas ease-of-use:
    -   Enhanced validation
    -   Allows property help on hover
    -   Autocomplete with acceptable values
-   Supports comments

**Note:** YAML has more validation capabilities. There may be cases when the JSON format is valid and save-able, but when viewing the same layout in YAML, errors will be identified and saving will be disabled. In this case, Admins can still toggle to and save in the JSON format.

## Creating a new layout

To create a new layout, navigate to the Transaction Manager Admin UI, click **Layouts** in the Admin Menu on the left, and then click **+ Add Layout** to add a new layout to the blueprint.

![Transaction Manager: layouts](../images/cpq-txn-mgr-layouts-new-1.png)

The layout requires a name and a variable name. Click in the Name field and enter the name of the new layout. As the Name value is being entered in the Name field the same value is being mirrored in the Variable Name field. By default, Transaction Manager makes the variable name the same as the Name value that the Admin enters. The variable name however in created using “camel case” and all spaces and special characters are removed from the name. For example, If you type “My First Layout” for the Name field, the Variable Name field will contain “myFirstLayout”. If you want to create your own custom variable names, click the pencil icon at the right end of the Variable Name field and you will be allowed to enter your own value for Variable Name.

![Transaction Manager: layouts](../images/cpq-txn-mgr-layouts-new-2.jpeg)

The code for the layout is then entered into the editor below the Name and Variable Name fields. Notice that the Name and variable name values that you created are automatically placed into the code for the new layout. The code for the rest of the layout definition can either be entered directly in the Editor or it can be created in another tool and then copy/pasted into the editor. Below are code examples to add various objects into the layout.

Use these examples as a starting point for creating your layout. Once you are done, you can Save your layout by clicking **Save** in the top right corner of the page.

If there are errors in the code, the Save button will be disabled. To identify errors, select the error messages button in the sub-header or look for red marks on the right hand side of the code display area as you scroll down through the code. These red marks denote an error in the code, and you should see the offending item in the code underlined with a red underline.

![lTransaction Manager: layouts](../images/cpq-txn-mgr-layouts-new-3.jpeg)

## General layout information

At the top of the layout file is some General layout Information that details overall layout characteristics. These general characteristics include:

-   **Version**

    The version of the layout JSON.

-   **Label**

    The display name of the layout.

-   **Variable name**

    The variable name of the layout.

-   **Currency**

    Allows you to define the currency symbol to display in the layout in currency fields. Using the value “symbol” simply tells the layout to use whatever the default currency symbol is for the ServiceNow CPQ environment.

-   **TierDef**

    Allows you to define the type of layout you want to display to the user. You can choose from Accordion, Expandable, Tabs, Vertical tabs, Headings, Pages

-   **Layout**

    You can define the display name of the layout as well as the variable name of the layout.


YAML code sample:

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

JSON code sample:

```
{
  "version": 1,
  "label": "Approved",
  "variableName": "default_approved",
  "currency": {
    "currencyDisplay": "symbol"
  },
  "tierDef": [
    {
      "depth": 1,
      "representation": "ExpandableSection"
    }
 ],
"layout": {
    "label": "layoutsection",
    "variableName": "layoutsection",
```

## Tiers

Tiers are sections of information for your transaction. Tiers are the top of the hierarchical structure of a Transaction Manager Layout. You can use tiers to organize your transaction information so that it is easier to find and understand for the buyside user.

For tiers you need to define:

-   **Label**

    The display name of the tier on the buyside UI \(the version of the layout JSON\).

-   **Variable name**

    The variable name of the tier.

-   **TierDef**

    Tiers can be nested in each other to allow you to create sections and sub-sections of information for your transaction. Tier depth defines at what level of the tier hierarchy does this tier reside. A value of 1 indicates the top level of the tier hierarchy.


YAML code sample:

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

JSON code sample:

```
"tiers": [
      {
        "label": "Transaction",
        "variableName": "transaction",
        "depth": 1,
```

## Columnvsets

As in configuration, Column sets are objects in the layout that allow you to organize fields and events on the buyside display. Fields and events can be arranged horizontally in a column set. Fields and events are arranged vertically by using multiple column sets in the same tier.

For each column set, you define:

-   **Variable name**

    The variable name of the column set.

-   **Elements**

    An array of the field and event objects that are to be displayed in this column set.


YAML code sample:

```
columnSets:
        - elements:
            - type: field
              columnOrder: 1
              variableName: txn.opportunity.id
          variableName: col1
```

JSON code sample:

```
"columnSets": [
          {
            "variableName": "col0",
            "elements": [
```

## Columnsets: fields

Fields are one type of object that are placed in the Elements array of a columnset.

For each field to be displayed in a column set, you need to define:

-   **Type**

    Either field or event.

-   **Variable name**

    The variable name of the field.

-   **Column order**

    Allows you to define the horizontal placement of the field in the column set. If all objects in the elements Array for a column set have the Column Order set to 1, the objects will be placed into the column set in the order that they appear in the array.

-   **Class info**

    A set of predefined HTML class types that allow you better control where in the layout an object resides.


YAML code sample:

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

JSON code sample:

```
"elements": [
              {
                "type": "field",
                "variableName": "txn.custom.status",
                "columnOrder": 1
              },
              {
                "type": "field",
                "variableName": "txn.custom.quoteName",
                "columnOrder": 1,
                "classInfo": "mw20"
              }
            ]
          },
```

## ColumnSets: events

Events are objects that cause certain actions to be taken, typically represented in the layout via a button.

For an event in the layout, you need to define:

-   **Type**

    Either field or event.

-   **Variable name**

    The variable name of the event.

-   **Label**

    The display name of the event, the name that will appear on the button.

-   **Column order**

    Allows you to define the horizontal placement of the field in the column set. If all objects in the elements Array for a column set have the Column Order set to 1, the objects will be placed into the column set in the order that they appear in the array.


YAML code sample:

```
To be added
```

JSON code sample:

```
"elements": [
             {
                "type": "event",
                "variableName": "submitForApproval",
                "label": "Submit for Approval",
                "columnOrder": 2
              },
              {
                "type": "event",
                "variableName": "revise",
                "label": "Revise",
                "columnOrder": 3
              },
```

## Line Item Grid \(LIG\)

The Line Item Grid object provides a display of the product information that is included in the Transaction. Detailed product information and pricing information is displayed in the Line Item Grid object.

For the Line Item Grid you need to define:

-   **Label**

    The display name of the Line Item Grid.

-   **Variable name**

    The variable name of the Line Item Grid.

-   **Depth**

    Allows you to define the tier depth at which the Line Item will be displayed.

-   **LineGrid**

    Here you define the Transaction Line level fields and the order in which they will be displayed. The Line Item Grid is a tabular structure where the fields define the columns displayed in the table.


The Line Item Grid has the following layout properties:

-   `showLineNumbers`: enables user-friendly line numbers; value of ‘true’ enables
-   `supportLongText`: a LIG field property, enables a popover on the field when selected; value of ‘true’ enables
-   `autoScrollIntoView`: smooths the scroll interaction between the transaction body and LIG; value of ‘true’ enables

YAML code sample:

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

JSON code sample:

```
{
        "label": "Line Items",
        "variableName": "lineItems",
        "depth": 1,
        "lineGrid": {
          "showLineNumbers": true,
          "autoScrollIntoView": true,
          "fields": [
            {
              "variableName": "txn.line.productName",
              "order": 1
              "supportLongText": true
            },
            {
              "variableName": "txn.line.productDescription",
              "order": 1
            },
            {
              "variableName": " txn.line.quantity",
              "order": 1
            },
```

## Line-level buttons

Line-level event buttons can be added on the right of the grid. They are specified in the `lineGrid` object. Buttons can use specified icons from the SLDS Utility library.

Available Icons:

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
</table>YAML code sample:

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

JSON code sample:

```
          "lineLevelButtons": [
            {
              "label": "Reconfigure",
              "uiEffect": {
                "type": "reconfigure",
                "target": "lineDrawer"
              },
              "variableName": "reconfig"
            },
            {
              "label": "Line Details",
              "icon": "threedots_vertical",
              "uiEffect": {
                "type": "lineDetail",
                "target": "lineDrawer"
              },
              "variableName": "lineDetail"
            },
            {
              "label": "Clone",
              "event": "cloneLine",
              "variableName": "clone"
            },
            {
              "label": "Delete",
              "event": "deleteLines",
              "variableName": "delete"
            }
          ],
```

## Fields

Fields provide the data input source for the Transaction. The layout needs to know what fields need to be displayed and how the fields should be displayed.

For each field you need to define:

-   **Type**

    The display type of the field. The display type values for Transaction Manager are the same as are available in Configuration.

    textArea - type provides an expanded editable area if the field is in the LIG.

-   **Variable name**

    The variable name of the field.

-   **Label**

    The display name of the field as it will appear to the buyside user.


YAML code sample:

```
fields:
  - type: Text
    label: Custom line field
    variableName: txn.line.custom.customText
  - type: ReadOnlyText
    label: TXN Number
    variableName: txn.custom.tXNNumber
```

JSON code sample:

```
"fields": [
    {
      "type": "ReadOnlyText",
      "variableName": "txn.custom.status",
      "label": "Transaction Status"
    },
    {
      "type": "Text",
      "variableName": "txn.custom.quoteName",
      "label": "Quote Name"
    },
    {
      "type": "Picklist",
      "variableName": "txn.custom.customerSegment",
      "label": "Customer Segment"
     },
     {
      "type": "Number",
      "variableName": "txn.custom.annualTransactionCount",
      "label": "Annual Transaction Count"
      },
```

## Text fields - resize

Text fields have a resizable property which can be enabled or disabled. It is enabled by default.

To disable resizing, pass “resizable: false” in raw value \(config\) or in layout json \(transaction\).

YAML code sample:

```
To be added
```

JSON code sample:

```
{
  "type": "TextArea",
  "label": "stg_transition_field",
  "variableName": "txn.custom.stg_transition_field",
  "resizable": false
}
```

## Product list

The productList object provides a set of layout properties for the Product List search results in the Add Lines / Product Search flow. Properties include:

-   `defaultSort`: define up to two parameters to sort Product List search results by
    -   The following fields can be used as parameters:
        -   modified
        -   created
        -   Name \(default if no parameters defined\)
        -   partnerId
        -   productCode
        -   description
        -   unitPrice
        -   externallyConfigurable
    -   Order can be defined per parameter \(‘asc’ or ‘desc’\) - will be ascending if not defined
-   `searchOnSubmit`: determines if user is required to select ‘Submit’ button to initiate a search

    A value of ‘true’ requires selection of ‘Submit’ button.

-   `columns`: add additional columns to Product List and determines their order

    -   Includes a `sortable` property; value of ‘true’ enables column to be sorted
    -   Includes an `alignment` property; ‘left’, ‘center’, ‘right’ are available options
    -   Includes a `width` property; CSS compatible value
    -   Includes a `supportLongText` property; value of ‘true’ enables a popover when selected

YAML code sample:

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

JSON code sample:

```
"productList": {
   "columns": [
     {
       "label": "Product ID",
       "sortable": true,
       "variableName": "id"
     },
     {
       "label": "Product Name",
       "variableName": "name"
     },
     {
       "label": "Product description",
       "supportLongText": true,
       "variableName": "description"
     },
     {
       "label": "Price",
       "variableName": "unitPrice"
      }
   ],
   "defaultSort": [
     "externallyConfigurable,desc",
     "name"
   ],
   "searchOnSubmit": true
 }
```

## UI effects

UI effects are layout elements that add specific functionalities to a Button. UI effects include:

-   **URL**

    Opens the associated URL inline, in a modal window, in slideout, or in a new tab or window,

-   **Anchor**

    Navigates to specified location in the transaction

-   **Product Search**

    Opens the product catalog, starting the Add Products flow

-   **Line Detail**

    Opens the line-detail layout

-   **Reconfigure**

    Opens the selected products to configuration UX

-   **Add Favorite**

    Opens a modal window to describe and create a favorite from the selection

-   **Manage Favorites**

    Opens the Favorites Manager

-   **Refresh Session**

    Checks whether the session has been modified, and if so, will refresh the sessionId and merge changes.


For more information, see [Transaction Manager: Layouts - UI effects](transaction-manager-layouts-ui-effects.md).

## Reference of a sample layout from UI

Please review the example UI configuration. The fields in the draft stage of the transaction end-user UI snapshot have been included in the sample JSON layout file attached below, which is configured for the draft stage.

![Transaction Manager: layouts](../images/cpq-txn-mgr-layouts-new-sample.jpeg)

[Sample Layout JSON](https://logikio.atlassian.net/wiki/spaces/CS/pages/1856471079/Txn+Mgr+-+Layouts)

