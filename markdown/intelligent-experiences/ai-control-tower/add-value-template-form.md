---
title: Add value template form
description: Add value template form fields and descriptions.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [AI Control Tower Reference, AI Control Tower, Enable AI experiences]
---

# Add value template form

Add value template form fields and descriptions.

<table id="table_dz5_w1d_yfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Calculation builder

</td></tr><tr><td>

Persona

</td><td>

The user role for whom the value is being calculated. Select one of the following personas: Agent, Developer, Other, Requestor. The default persona is Other.For example, if the AI asset is Incident Summarization and the selected persona is Agent, the value calculations as per the value template are for Agent role only.

</td></tr><tr><td>

Usage

</td><td>

The usage metric of the AI asset, used to calculate the value. If you add a custom indicator, the usage value is derived from the indicator. Be sure to use a daily usage indicator.For example, if the AI asset is Incident Summarization, usage value is the daily executions of Incident Summarization.

</td></tr><tr><td>

Time value type

</td><td>

The type of time-based metric used in the calculation, for example, Constant or Indicator. If you are using a custom metric, select Indicator.

</td></tr><tr><td>

Time constant

</td><td>

A fixed time value \(in minutes\) used as a baseline in the calculation. For example, if the AI asset is Incident Summarization, time value is the average time saved per invocation of Incident Summarization.

</td></tr><tr><td>

Time indicator

</td><td>

The average time saved \(in minutes\) per invocation of the AI asset. If you add a custom indicator, this value is derived from the indicator.For example, if the AI asset is Incident Summarization, time value is the average time saved per invocation of Incident Summarization. This value is derived from the custom indicator added.

</td></tr><tr><td>

Acceptance rate type

</td><td>

The type of acceptance rate to use for the calculation, such as Indicator or Constant. If you are using a custom metric for calculations, select Indicator.

</td></tr><tr><td>

Acceptance rate constant

</td><td>

A fixed percentage or ratio used to represent an expected or target acceptance rate of the AI asset in the value calculation. The value should be between 1 and 100.For example, if the AI asset is Incident Summarization, acceptance rate is the percentage or ratio of Incident Summarization results that are acceptable for the users.

</td></tr><tr><td>

Acceptance rate indicator

</td><td>

A percentage or ratio used to represent an expected or target acceptance rate of the AI asset in the value calculation. If you add a custom indicator, this value is derived from the indicator. Be sure to use a daily indicator with a value between 1 and 100.For example, if the AI asset is Incident Summarization, acceptance rate is the percentage or ratio of Incident Summarization results that were accepted by the users. This value is derived from the custom indicator added.

</td></tr><tr><td colspan="2">

Attributes

</td></tr><tr><td>

Template name

</td><td>

A unique and descriptive name for the value template. This name appears in the list of templates and should clearly indicate its purpose.

</td></tr><tr><td>

Value template category

</td><td>

The categorization of the template based on its use case, for example, Productivity, Efficiency, Accuracy. Helps in organizing and filtering templates.

</td></tr><tr><td>

Department

</td><td>

The business unit or department associated with the value template. This helps in aligning the template with organizational goals.

</td></tr><tr><td>

Description

</td><td>

A brief explanation of what the value template does, including its purpose and how it contributes to measuring value.

</td></tr><tr><td colspan="2">

Calculation output

</td></tr><tr><td>

Instance

</td><td>

The instance where the value template is applied. This field is useful for managing value templates across instances.**Note:** You can validate a formula in a non-production instance before publishing it to a production instance. After initiating testing for a value template, you might need to wait up to 10 minutes for same-instance testing or 30 minutes for cross-instance testing. During this time, you can't edit or resend the template for testing, but you can continue working with other templates.

</td></tr></tbody>
</table>**Parent Topic:**[AI Control Tower Reference](aict-references.md)

