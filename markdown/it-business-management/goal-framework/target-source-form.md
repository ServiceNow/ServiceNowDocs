---
title: Target Source form
description: Use the Target Source form to create and configure a source for your targets so that the actual value of the target is auto-updated.
locale: en-US
release: yokohama
product: Goal Framework
classification: goal-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Target Source form

Use the Target Source form to create and configure a source for your targets so that the actual value of the target is auto-updated.

<table id="table_demand_benefit_plan_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the target source.

</td></tr><tr><td>

Active

</td><td>

Option to activate this target source for use.

</td></tr><tr><td>

Type

</td><td>

Type of target source. Available options:-   **Assessment/Survey**
-   **PA Indicator**
-   **Custom script**

</td></tr><tr><td>

Advanced

</td><td>

Enables the **Custom script** option for the target source type **Assessment/Survey** with the pre-defined script.This field is available when the **Type** field is set to **Assessment/Survey**.

</td></tr><tr><td>

Assessment metric type

</td><td>

Assessment metric type for the target source.**Tip:** A context variable is automatically created for the target source if the field is populated with a metric type of Evaluation method = Assessment.

 This field is available when the **Type** field is set to **Assessment/Survey**.

</td></tr><tr><td>

Assessment metric category

</td><td>

Assessment metric category for the assessment metric type.This field is available when the **Type** field is set to **Assessment/Survey**.

</td></tr><tr><td>

Description

</td><td>

Brief description of the target source.

</td></tr><tr><td>

PA Indicator

</td><td>

PA Indicator for the target source.This field is available when the **Type** field is set to **PA Indicator**.

</td></tr><tr><td>

Breakdown

</td><td>

Breakdown for the PA Indicator.This field is available when the **Type** field is set to **PA Indicator**.

</td></tr><tr><td>

Custom script

</td><td>

Custom script to fetch the required data from any ServiceNow AI Platform table for the target source.This field is available when the **Type** field is set to **Custom**. Or, when the **Type** field is set to **Assessment/Survey** and the **Advanced** field is set to **true**.

</td></tr></tbody>
</table>**Parent Topic:**[Goal Framework and Goal Framework for SPM reference](goal-framework-reference.md)

