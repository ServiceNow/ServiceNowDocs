---
title: Evaluation metrics and calculations
description: Metrics against which conversations are evaluated and calculation of adjusted scores.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2025-09-03"
reading_time_minutes: 3
breadcrumb: [Evaluation dashboard References, Reference, AI Control Tower, Enable AI experiences]
---

# Evaluation metrics and calculations

Metrics against which conversations are evaluated and calculation of adjusted scores.

## Metrics

The Select metric list shows all the metrics against which each conversation is evaluated for the selected date range. You can filter the evaluation trend based on each metric. The following metrics are available:

|Metric|Description|
|------|-----------|
|Request Completion|Measures the virtual agent's ability to complete user requests by accurately identifying the user's intent and gathering all required information \(slot filling\).|
|Intent Accuracy|Shows the virtual agent's ability to comprehend user requests, resulting in relevant responses.|
|Slot Filling|Shows the virtual agent's capability to interpret user responses and extract structured answers to the required questions.|
|Smooth Flowing Conversation \(Deadlock avoidance\)|Checks if the virtual agent responds dynamically, successfully moving the conversation forward without repetition.|
|Context Retention|Shows if the virtual agent succeeds in retaining and using information provided during the conversation, including request interpretation and slot filling.|
|Truthfulness \(Hallucination Prevention\)|Shows if the virtual agent generated genuine responses grounded in conversation, excluding fabrication or memory and comprehension failures.|
|Conciseness \(Redundancy Avoidance\)|Checks the virtual agent's ability to avoid superfluous or verbose and generic responses, which doesn't contribute to the core intent of the conversation.|
|Coherence|Checks for clear logical flow, structure, and organization of the virtual agent's responses.|
|User Satisfaction|Weighted average of all the other metrics on which the conversation was evaluated.|

**Note:** All the metrics are rated on a scale of 3 or 5, and are finally scaled up to 5.

## Calculations

Calculation of deviations and Adjusted Score:

To align the auto-evaluation scores with human judgment over time, a deviation is calculated and used to produce an adjusted score on metric level.

-   Upper Deviation

    Condition: If the number of human-labeled scores that are higher than the auto-evaluated scores in the last 6 months is more than 30.

    Calculation: The top 90% of these cases are taken and the difference \(delta\) between the human score and the auto-evaluated score is averaged. This delta is the Upper Deviation.

-   Lower Deviation

    Condition: If the number of human-labeled scores that are lower than the auto-evaluated scores in the last 6 months is more than 30.

    Calculation: The top 90% of these cases are taken and the difference \(delta\) between the human score and the auto-evaluated score is averaged. This delta is the Lower Deviation.

-   Adjusted Score

    The final Adjusted Score is calculated based on the availability of the deviations.

    -   If at least 30 distinct evaluations of both upper and lower deviations are labeled for a given metric, Error band is calculated as SUM\(Avg labeling score – LLM score\)/Distinct evaluations. This error band is added to Auto-Eval score to get Adjusted Score.
    -   If neither deviation is available, then Adjusted Score = Auto-Eval Score

Calculation of Auto eval user satisfaction score, Human user satisfaction score, and Upper and Lower deviation on Evaluation level:

-   Auto eval user satisfaction score: For a given evaluation, get all the scores for each metric that are LLM generated and calculate SUM\(metric score \* metric weight\)/SUM\(metric weights\).
-   Human user satisfaction score: For a given evaluation, if at least one metric is labeled, it’s considered to calculate the human user satisfaction score. If labeled, the labeling score is used, or else LLM score is used. Calculated as SUM\(metric score \* metric weight\)/SUM\(metric weights\).
-   Gap: Gap is calculated as \(Human user satisfaction score – Auto eval satisfaction score\).
-   Upper Deviation: If the Gap is positive and there are more than 30 records, the error band is calculated at top 90% by SUM\(Positive Gap\) / Distinct evaluations. This error band is added to the Auto eval user satisfaction score.
-   Lower Deviation: If the Gap is negative and there are more than 30 records, the error band is calculated at top 90% by SUM\(Negative Gap\) / Distinct evaluations. This error band is added to the Auto eval user satisfaction score.
-   Adjusted user satisfaction score is calculated as SUM\(Gap\) / Distinct evaluations.

**Note:**

-   The evaluator provides aggregated score per chat, even if there are multiple different requests made by user.
-   Performance Analytics indicators are used to calculate the average score over time. If you run batch jobs on historical data, then by the definition of Performance Analytics indicators, these evaluations are counted on the evaluation date in aggregated scores and not counted for scores on the actual chat date.

**Parent Topic:**[Evaluation dashboard References](ai-eval-references.md)

