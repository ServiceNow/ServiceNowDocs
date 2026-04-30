---
title: Configuring evaluations
description: Configure conversation evaluations by disabling evaluations, adjusting execution logic and thresholds, and tuning scoring weights.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 1
breadcrumb: [Evaluation tab, AI Control Tower Home, AI Control Tower dashboard, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Configuring evaluations

Configure conversation evaluations by disabling evaluations, adjusting execution logic and thresholds, and tuning scoring weights.

## Disable evaluations

**Prerequisites**

Update must be created.

Disable evaluations:

1.  Navigate to **Process Automation** &gt; **Flow Designer** and select **Flows**.
2.  Select the Execute Evaluation flow.
3.  Select **Deactivate**.

## Change the evaluation execution conditions

Change the evaluation execution conditions:

1.  Navigate to **System Definition** &gt; **Script Includes**.
2.  Search for and select the script Include `evalExecuteCondition`.
3.  In the **Script** field, modify the executeEvaluation method.
    -   Input: The method receives the conversation reference record as a parameter.
    -   To restrict by user profile, use the initiatedUser variable \(contains the user’s sys\_id\).
4.  Use GlideRecord queries or other logic as needed to implement custom execution conditions.
5.  Save and test in a non-production environment before promoting.

## Set the daily limit on evaluations

Set a maximum daily limit on evaluations:

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties** \(sys\_properties.list\).
2.  Search for and select the property **sn\_na\_conv\_eval.maxEvaluateCount**.
3.  Set the **Value** field to the desired integer value to limit the maximum number of evaluations created per day.

## Configure the minimum records for error bands

Set the minimum number of records required to calculate the error band for upper and lower deviation:

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties** \(sys\_properties.list\).
2.  Search for and select the property **sn\_na\_conv\_eval.errorBandMinRecords**.
3.  Set the **Value** field to the desired integer value to define the minimum number of records required before upper and lower error bands are calculated.

## Adjust skill weights for the composite score

Set the weights for each evaluation metric for chat evaluation, which are used to compute total and composite scores on evaluation records:

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties** \(sys\_properties.list\).
2.  Search for and select the property **sn\_na\_conv\_eval.evalWeights**.
3.  Update only the value components for each skill.

    The composite score is calculated as Sum\(Skill Score × Skill Weight\) / Sum\(Skill Weights\).


