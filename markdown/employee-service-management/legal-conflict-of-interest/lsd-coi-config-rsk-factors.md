---
title: Configure risk factors
description: Configure risk factors to define the criteria the risk assessment functionality evaluates a request. Each risk factor uses one of three evaluation types: Condition, Skill, or Subflow.
locale: en-US
release: australia
product: Legal Conflict of Interest
classification: legal-conflict-of-interest
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure risk assessment, Configure, Legal Conflict of Interest, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure risk factors

Configure risk factors to define the criteria the risk assessment functionality evaluates a request. Each risk factor uses one of three evaluation types: Condition, Skill, or Subflow.

## About this task

Risk factors define the criteria evaluated when scoring a request. Each factor is assigned a weight that reflects its impact on the overall risk score. The utility supports three evaluation types:

-   Condition: Evaluates the disclosure against rule-based conditions defined in risk factor conditions. Each condition tests a specific field value and assigns a score when the condition is met. Use this type for deterministic, field-based evaluations.
-   Skill: Uses an AI skill to evaluate the disclosure. Use this type when the evaluation requires natural language understanding or analysis that cannot be expressed as a simple field condition.

    **Note:**

    -   The skill is available in the base system to evaluate an COI request only when you have installed and configured Legal Service Delivery - Prime that is a paid application.
    -   You can access the skill by navigating to **Now Assist Skill Kit** &gt; **Home** &gt; **Custom skills** and selecting Legal Risk Evaluator Prompt.
    For more information, see [Now Assist for Legal Service Delivery \(LSD\)](../../legal-request-management/concept/now-assist-lsd-landing.md).

-   Subflow: Executes a Flow Designer subflow to evaluate the disclosure. Use this type when the evaluation requires complex logic, external integrations, or multi-step processing.

## Before you begin

Role required: sn\_lco\_cmn.config

## Procedure

1.  Add risk factor using any of the following methods.

    -   Add risk factor from the risk assessment record
        -   Navigate to **All** &gt; **Legal and Contracts Common Utilities** &gt; **Risk Assessment**.
        -   From the Risk factors related list, select **New**.
    -   Add a risk factor record directly
        -   Navigate to **All** &gt; **Legal and Contracts Common Utilities** &gt; **Risk factor**.
        -   Select **New**.
2.  On the form, fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|A descriptive name for the risk factor.|
    |Risk assessment|The risk assessment where the risk factor will be evaluated. When you create a risk factor from the risk assessment record it will be populated with the risk assessment name.|
    |Active|Select the check box to include this factor in risk evaluations.|
    |Description|An explanation of what the condition evaluates and why it contributes to the risk score.|
    |Weight|The scoring weight assigned to this factor. Higher weights indicate greater impact on the overall risk score.|

3.  Configure evaluation type.

<table id="choicetable_xj5_tp1_33c"><thead><tr><th align="left" id="d420783e264">

Evaluation type

</th><th align="left" id="d420783e267">

Steps

</th></tr></thead><tbody><tr><td id="d420783e273">

**Subflow**

</td><td>

A Subflow reference field appears.

Select the Flow Designer subflow that executes custom evaluation logic and returns a risk score in the Subflow field.

</td></tr><tr><td id="d420783e284">

**Condition**

</td><td>

-   Right-click on the form header and select **Save**.
-   In the Risk factor conditions related list, select **New**.
-   In the **Name** field, enter descriptive name.
-   In the **Table** field, select the table on which the condition is evaluated.
-   In the **Risk factor** field, select parent risk factor. It is auto-populated when creating from the related list.
-   Select the **Active** check box to activate the condition.
-   In the **Order** field, enter the evaluation order.
-   In the **Score** field, assign a score assigned when this condition is met.
-   In the **Applies to** filter, define filter conditions using the condition builder. Example: Is it a true governance board for an organization is Advisory Board.


</td></tr><tr><td id="d420783e351">

**Skill**

</td><td>

A Skill reference field appears.

Select the AI skill that analyzes the disclosure content and returns a risk score.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The risk factor is configured and active. When the risk assessment utility evaluates a request, it processes each active risk factor based on its evaluation type: The scores from all active risk factors are aggregated to produce the overall risk score, which determines the risk level \(Low, Medium, or High\) and the corresponding approval routing.

**Parent Topic:**[Configure risk assessment](lsd-coi-config-risk-fac.md)

