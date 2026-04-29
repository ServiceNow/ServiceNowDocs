---
title: Transaction Manager: Layouts - The stages progress chevron
description: You can configure a progress bar using layout JSON or YAML and define it either statically or dynamically. See code snippets.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transaction Manager: Layouts, Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager: Layouts - The stages progress chevron

You can configure a progress bar using layout JSON or YAML and define it either statically or dynamically. See code snippets.

## Purpose

The Stages Progress Chevron component is a visual representation of a transaction’s stage progression, typically displayed as a horizontal chevron bar. It can be defined statically or dynamically and is configurable through layout JSON.

## Configuration options

The component is placed at the root level of the layout JSON \(alongside `header` or `tierDef`\).

## Static definition

Define a list of stages manually.

JSON:

```
"stageProgress": {
  "stageList": [
    { "value": "draft", "label": "Draft" },
    { "value": "stage2", "label": "Stage 2" },
    ...
  ],
  "currentStage": "draft"
}
```

YAML:

```
stageProgress:
  stageList:
    - value: draft
      label: Draft
    - value: stage2
      label: Stage 2
    # ... add more stages as needed
  currentStage: draft
```

-   `stageList` defines each stage’s `value` and display `label`.
-   `currentStage` highlights the active stage.

    If `currentStage` is omitted, it defaults to `txn.stage`. This allows you to use in a default layout used by multiple stages.


## Custom picklist-based definition

Use custom fields to dynamically populate the chevron.

JSON:

```
"stageProgress": {
  "stageListField": "txn.custom.stageList",
  "currentStageField": "txn.custom.stageList"
}
```

YAML:

```
stageProgress:
  stageListField: txn.custom.stageList
  currentStageField: txn.custom.stageList
```

-   `stageListField` specifies where to pull the list of available stages.
-   `currentStageField` specifies the field that contains the current stage value.

This method supports:

-   Exclusion rules to hide or disable specific stages.
-   Determination rules to set the value of the current stage.

    Determination rules are useful when multiple stages should display as a single chevron.


## Combination use

You can mix static and dynamic configurations:

-   Use a static `stageList` with a dynamic `currentStageField`.
-   If neither `stageList` nor `stageListField` is defined, nothing displays.
-   If neither `currentStage` nor `currentStageField` is defined, `txn.stage` is used by default.
-   If both static and dynamic versions are present, the dynamic version takes precedence.

## Theming

The component supports theming using CSS custom properties. The following table shows a non-exhaustive list of relevant variables.

|Variable|Description|
|--------|-----------|
|`--lgk-ProgressStep-chevron-size`|Overall chevron size|
|`--lgk-ProgressStep-chevron-width`|Fixed width for chevrons|
|`--lgk-ProgressStep-chevron-minWidth`|Minimum width per chevron|
|`--lgk-ProgressStep-chevron-padding`|Padding inside each chevron|
|`--lgk-ProgressStep-chevron-disabled-opacity`|Opacity for disabled/inactive chevrons|
|`--lgk-ProgressStep-incomplete-backgroundColor`|Background for incomplete steps|
|`--lgk-ProgressStep-incomplete-chevron-color`|Chevron icon color for incomplete steps|
|`--lgk-ProgressStep-current-backgroundColor`|Background for current step|
|`--lgk-ProgressStep-current-chevron-color`|Chevron icon color for current step|
|`--lgk-ProgressStep-chevron-label-fontSize`|Font size for stage labels|
|`--lgk-ProgressStep-chevron-label-fontWeight`|Font weight for stage labels|

**Tip:** You can inspect the element in your browser to explore more custom properties.

