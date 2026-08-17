---
title: Value template form fields
description: Field descriptions for the value template form, used when you create or edit a value template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/measure-ai-reference-value-template-form.html
release: australia
topic_type: reference
last_updated: "2026-07-26"
reading_time_minutes: 1
breadcrumb: [Create a value template, Configure, Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# Value template form fields

Field descriptions for the value template form, used when you create or edit a value template.

## Template details

|Field|Description|
|-----|-----------|
|Template name|A unique and descriptive name for the value template. This name appears in the list of templates and should clearly indicate its purpose.|
|Value template category|The categorization of the template based on its use case, for example, Productivity, Efficiency, Accuracy. Helps in organizing and filtering templates.|
|Department|The business unit or department associated with the value template. This helps in aligning the template with organizational goals.|
|Description|A brief explanation of what the value template does, including its purpose and how it contributes to measuring value.|

## Calculation builder

The calculation builder defines the formula: Productivity = Usage × Time × Quality.

|Field|Description|
|-----|-----------|
|Persona|The user role for whom the value is calculated, for example, Agent, Requester.|
|Usage|The usage indicator for the AI system.|
|Time value type|The type of time-based metric used in the calculation, for example, Constant or Indicator. Choose a value that aligns with your performance goals.|
|Time constant \(in minutes\)|A fixed time value in minutes, used when Time value type is Constant. Useful for comparisons or normalization.|
|Time indicator|An indicator that provides the time value. Used when Time value type is Indicator.|
|Quality type|How the quality factor is provided: Constant, Indicator, or Quality Score. Quality Score is available when the AI Evaluations plugin is active.|
|Quality constant \(in %\)|A fixed quality percentage. Used when Quality type is Constant.|
|Default quality constant \(in %\)|A fallback quality percentage used when a quality score is unavailable. Used when Quality type is Quality Score.|
|Quality indicator|An indicator that provides the quality value. Used when Quality type is Indicator.|

## Calculation overview

<table id="table_bhz_brm_1kc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Instance

</td><td>

The instance where the value template is applied. This field is useful for managing value templates across instances.**Note:** You can validate a formula in a non-production instance before publishing it to a production instance.

</td></tr></tbody>
</table>