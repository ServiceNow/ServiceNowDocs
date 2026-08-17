---
title: Stage progress chevron
description: Reference for configuring the Stages Progress Chevron component in ServiceNow Quote Experience layouts, including static and dynamic configuration options, combination rules, and CSS custom property theming in CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-stage-progress-chevron.html
release: australia
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Layouts, CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Stage progress chevron

Reference for configuring the Stages Progress Chevron component in ServiceNow Quote Experience layouts, including static and dynamic configuration options, combination rules, and CSS custom property theming in CPQ.

## Purpose

The Stages Progress Chevron component displays a horizontal chevron bar that visually represents a transaction's progression through its quote lifecycle stages. The component is placed at the root level of the layout YAML or JSON, alongside `header` or `tierDef`. It can be defined statically, dynamically, or as a combination of both methods.

## Static configuration

Use static configuration to define a fixed list of stages for the chevron. Each stage requires a `value` and a display `label`.

YAML:

```
stageProgress:
  stageList:
    - value: draft
      label: Draft
    - value: stage2
      label: Stage 2
    # add more stages as needed
  currentStage: draft
```

-   **`stageList`**

    Defines each stage's value and display label in the chevron.

-   **`currentStage`**

    Highlights the active stage in the chevron. If omitted, defaults to `txn.stage`, which allows the same layout to be used across multiple stages.


## Dynamic configuration

Use dynamic \(picklist-based\) configuration to populate the chevron from custom transaction fields. This method supports exclusion rules to hide or disable specific stages and determination rules to set the current stage value.

YAML:

```
stageProgress:
  stageListField: txn.custom.stageList
  currentStageField: txn.custom.stageList
```

-   **`stageListField`**

    Specifies the custom field that provides the list of available stages.

-   **`currentStageField`**

    Specifies the custom field that contains the current stage value. Determination rules are useful when multiple stages should display as a single chevron step.


## Combination and fallback rules

Static and dynamic configurations can be mixed. The following rules apply when both are present or when values are omitted.

-   A static `stageList` can be combined with a dynamic `currentStageField`.
-   If neither `stageList` nor `stageListField` is defined, nothing displays in the chevron.
-   If neither `currentStage` nor `currentStageField` is defined, `txn.stage` is used by default.
-   If both a static and a dynamic version of the same property are present, the dynamic version takes precedence.

## CSS custom property theming

The stage progress chevron supports theming using CSS custom properties. The following table lists the relevant variables. Inspect the element in your browser to explore additional custom properties.

|Variable|Description|
|--------|-----------|
|`--lgk-ProgressStep-chevron-size`|Overall chevron size.|
|`--lgk-ProgressStep-chevron-width`|Fixed width for each chevron.|
|`--lgk-ProgressStep-chevron-minWidth`|Minimum width per chevron.|
|`--lgk-ProgressStep-chevron-padding`|Padding inside each chevron.|
|`--lgk-ProgressStep-chevron-disabled-opacity`|Opacity for disabled or inactive chevrons.|
|`--lgk-ProgressStep-incomplete-backgroundColor`|Background color for incomplete steps.|
|`--lgk-ProgressStep-incomplete-chevron-color`|Chevron icon color for incomplete steps.|
|`--lgk-ProgressStep-current-backgroundColor`|Background color for the current step.|
|`--lgk-ProgressStep-current-chevron-color`|Chevron icon color for the current step.|
|`--lgk-ProgressStep-chevron-label-fontSize`|Font size for stage labels in the chevron.|
|`--lgk-ProgressStep-chevron-label-fontWeight`|Font weight for stage labels in the chevron.|

**Related topics**  


[Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-layouts.md)

[Create a quote transaction layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-layout.md)

[ServiceNow Quote Experience layout UI effects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-ui-effects.md)

