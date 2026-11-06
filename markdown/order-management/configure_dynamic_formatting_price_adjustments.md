---
title: Configure dynamic formatting for the adjustment value field
description: Configure the transaction layout so that the adjustment value field displays as a currency amount or a percentage, based on the selected adjustment type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/configure\_dynamic\_formatting\_price\_adjustments.html
release: australia
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 1
breadcrumb: [Formatting manual price adjustment values, Pricing in the ServiceNow Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure dynamic formatting for the adjustment value field

Configure the transaction layout so that the adjustment value field displays as a currency amount or a percentage, based on the selected adjustment type.

## Before you begin

Role required: admin

You need administrator access to transaction layouts in productized pricing.

## About this task

The following table describes the properties of the dynamic format type, which sets a field's display format based on the value of another field.

|Property|Description|
|--------|-----------|
|`type`|Set to `dynamic`.|
|`controller`|The variable name of the field whose value determines the format of the target field.|
|`rules`|An ordered array of rules. Each rule has a `format` and a `values` array.|
|`format` \(in a rule\)|The format to apply when the rule matches. It uses the same schema as the outer format. You can't nest a `dynamic` format inside a rule.|
|`values` \(in a rule\)|The underlying values of the controller field for which the rule applies. Use the underlying values, not the display labels.|

## Procedure

1.  Navigate to **CPQ Administration** &gt; **Transaction** &gt; **Layouts**.

2.  Open the layout that contains the manual adjustment fields.

3.  Switch to the YAML editor.

    The visual editor doesn't support this change.

4.  Find the discount adjustment value field \(`txn.line.pricing.discount.value`\).

    Keep `type` as `FormattedNumber`. Change only the `format` property. The adjustment type field \(`txn.line.pricing.discount.adjustmentType`\) must be a `Picklist` in the same layout. The discount reason field \(`txn.line.pricing.discount.description`\) is optional.

5.  Replace the fixed `format` with a dynamic format that uses the adjustment type field as the controller.

    ```
    format:
      type: dynamic
      controller: txn.line.pricing.discount.adjustmentType
      rules:
        - format:
            type: currency
          values: [MARKDOWN_AMT, PRICE_OVERRIDE]
        - format:
            type: unit
            unit: percent
          values: [MARKDOWN_PER]
    ```

    In `values`, use the underlying values of the adjustment type field, not the display labels. Rules are evaluated in order, and the first matching rule applies. Don't use `type: percent` for `MARKDOWN_PER`, because it doesn't match how the adjustment is sent to pricing.

6.  Save the layout, then deploy it.

7.  Reload the transaction and check the display for each adjustment type.


## Verification results

|Adjustment type|Value entered|Adjustment value display|Net price after reprice|
|---------------|-------------|------------------------|-----------------------|
|MARKDOWN\_PER|10|10%|$45 \(−$5\)|
|MARKDOWN\_AMT|10|$10|$40 \(−$10\)|
|PRICE\_OVERRIDE|10|$10|$10 \(−$40\)|

