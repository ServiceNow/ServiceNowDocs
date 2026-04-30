---
title: Transaction Manager: Layouts - Theming options
description: Transaction Manager layouts can be adjusted by setting JSON and YAML properties.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 2
breadcrumb: [Transaction Manager: Layouts, Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Layouts - Theming options

Transaction Manager layouts can be adjusted by setting JSON and YAML properties.

Include the following JSON at the top level of the layout JSON:

```
  "theme": {
    "base": "slds",
    "otterKit": true,
    "properties": {
      "body-color": "#000",
      "spacing-sm": "0.15rem",
      "label-color": "var(--token-color-black-500)",
      "pill-radius": "2px",
      "header-color": "#30578d",
      "border-radius": "2px",
      "body-font-size": "0.875rem",
      "label-font-size": "0.75rem",
      "body-font-weight": "700",
      "bom-border-color": "#7e8592",
      "body-border-color": "#7e8592",
      "body-border-width": "0",
      "button-font-color": "600",
      "pill-border-color": "#30578d",
      "body-border-radius": "0",
      "input-border-color": "#999",
      "input-border-width": "1px",
      "button-border-width": "1px",
      "font-weight-regular": "700",
      "header-border-color": "#7e8592",
      "header-logo-padding": "0.5rem",
      "input-border-radius": "2px",
      "internal-icon-color": "#aeaeae",
      "body-wrapper-padding": "0",
      "button-border-radius": "2px",
      "button-neutral-color": "#30578d",
      "button-primary-color": "#30578d",
      "int-option-font-size": "0.875rem",
      "token-color-black-500": "#444",
      "combobox-option-margin": "0 0 0 10px",
      "header-logo-min-height": "50px",
      "pill-remove-icon-color": "#4d4d4d",
      "container-border-radius": "0",
      "header-margin-block-end": "0",
      "token-color-neutral-950": "#aeaeae",
      "combobox-option-font-size": "0.875rem",
      "slds-c-button-line-height": "1.875rem",
      "slds-c-input-color-border": "#000",
      "button-primary-focus-color": "#0065cc",
      "button-primary-hover-color": "#0065cc",
      "slds-c-input-radius-border": "2px",
      "button-neutral-border-color": "#30578d",
      "button-primary-border-color": "#30578d",
      "expand-header-border-radius": "2px",
      "button-primary-disabled-color": "#666",
      "button-neutral-backgroundColor": "#fff",
      "button-primary-backgroundColor": "#fff",
      "expand-header-border-color-focus": "#7e8592",
      "button-primary-focus-border-color": "#0065cc",
      "button-primary-hover-border-color": "#0065cc",
      "button-neutral-focus-backgroundColor": "#fff",
      "button-neutral-hover-backgroundColor": "#fff",
      "button-primary-disabled-border-color": "#666",
      "button-primary-focus-backgroundColor": "#fff",
      "button-primary-hover-backgroundColor": "#fff",
      "button-primary-disabled-backgroundColor": "#efefef",
      "token-color-primary-outline-border-color": "#ff0000",
      "expand-header-content-padding-inline-start": "0"
    }
  },
```

YAML:

```
theme:
  base: slds
  otterKit: true
  properties:
    body-color: "#000"
    spacing-sm: "0.15rem"
    label-color: "var(--token-color-black-500)"
    pill-radius: "2px"
    header-color: "#30578d"
    border-radius: "2px"
    body-font-size: "0.875rem"
    label-font-size: "0.75rem"
    body-font-weight: "700"
    bom-border-color: "#7e8592"
    body-border-color: "#7e8592"
    body-border-width: "0"
    button-font-color: "600"
    pill-border-color: "#30578d"
    body-border-radius: "0"
    input-border-color: "#999"
    input-border-width: "1px"
    button-border-width: "1px"
    font-weight-regular: "700"
    header-border-color: "#7e8592"
    header-logo-padding: "0.5rem"
    input-border-radius: "2px"
    internal-icon-color: "#aeaeae"
    body-wrapper-padding: "0"
    button-border-radius: "2px"
    button-neutral-color: "#30578d"
    button-primary-color: "#30578d"
    int-option-font-size: "0.875rem"
    token-color-black-500: "#444"
    combobox-option-margin: "0 0 0 10px"
    header-logo-min-height: "50px"
    pill-remove-icon-color: "#4d4d4d"
    container-border-radius: "0"
    header-margin-block-end: "0"
    token-color-neutral-950: "#aeaeae"
    combobox-option-font-size: "0.875rem"
    slds-c-button-line-height: "1.875rem"
    slds-c-input-color-border: "#000"
    button-primary-focus-color: "#0065cc"
    button-primary-hover-color: "#0065cc"
    slds-c-input-radius-border: "2px"
    button-neutral-border-color: "#30578d"
    button-primary-border-color: "#30578d"
    expand-header-border-radius: "2px"
    button-primary-disabled-color: "#666"
    button-neutral-backgroundColor: "#fff"
    button-primary-backgroundColor: "#fff"
    expand-header-border-color-focus: "#7e8592"
    button-primary-focus-border-color: "#0065cc"
    button-primary-hover-border-color: "#0065cc"
    button-neutral-focus-backgroundColor: "#fff"
    button-neutral-hover-backgroundColor: "#fff"
    button-primary-disabled-border-color: "#666"
    button-primary-focus-backgroundColor: "#fff"
    button-primary-hover-backgroundColor: "#fff"
    button-primary-disabled-backgroundColor: "#efefef"
    token-color-primary-outline-border-color: "#ff0000"
    expand-header-content-padding-inline-start: "0"
```

## Remove padding on page body

`"body-wrapper-padding": "0"` in the layout JSON above.

## Style field labels

`"label-color": "var(--token-color-black-500)"` and

`"label-font-size": "0.75rem"` in the layout JSON above.

## Style buttons and button labels

`"button-font-color": "600"` and

`"button-font-weight": "700"` in the layout JSON above.

## Number formatting

Administrators can use the `minPrecision` property to require a minimum number of decimal places.

You can use the `showCurrency` property to display or hide the currency symbol.

-   minPrecision

    JSON:

    ```
    {
     "type": "FormattedNumber",
     "label": "Just minPrecision",
     "format": {
       "type": "decimal",
       "minPrecision": 2
      },
     "variableName": "txn.custom.someNumber"
    }
    ```

    YAML:

    ```
    type: FormattedNumber
    label: Just minPrecision
    format:
      type: decimal
      minPrecision: 2
    variableName: txn.custom.someNumber
    ```

    In this example, if txn.custom.someNumber is set to 4.5, the layout will display 4.50.

-   showCurrency

    JSON:

    ```
    {
     "type": "FormattedNumber",
     "label": "With Hidden Currency",
     "format": {
       "type": "currency",
       "minPrecision": 2,
       "showCurrency": false
      },
       "variableName": "txn.custom.genericNum"
    }
    ```

    YAML:

    ```
    type: FormattedNumber
    label: With Hidden Currency
    format:
      type: currency
      minPrecision: 2
      showCurrency: false
    variableName: txn.custom.genericNum
    ```

    In this example, if txn.custom.genericNum, a defined currency type that will show the currency symbol by default, is set to 4.5, the layout will display 4.50.


