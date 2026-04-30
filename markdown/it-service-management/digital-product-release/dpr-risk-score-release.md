---
title: Risk score for a release
description: Risk scores help release coordinators and product managers identify potential issues early and take corrective action. The risk score is calculated for the current in-progress phase and is recalculated each time you view the Release overview dashboard.The risk score of timeline-oriented releases combines overdue task scores and policy failure scores, weighted by their respective importance. The weight or priority to overdue tasks and policy failure determines their urgency or impact on a release. The score ranges from 0 to 100.The risk score for stage-oriented releases evaluates the likelihood of delays or issues in the current phase based on task completion, policy compliance, progress thresholds, and readiness date proximity. The score ranges from 0 to 100.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2026-02-25"
reading_time_minutes: 5
keywords: [Risk score calculation for a release, Risk score formula for a release, Risk score for a release, Risk score for a timeline-oriented release, Risk score for a stage-oriented release, risk score timeline release, timeline-oriented risk score, release risk calculation, risk score stage release, stage-oriented risk score, release risk calculation, risk score readiness]
breadcrumb: [Reference, Digital Product Release, IT Service Management]
---

# Risk score for a release

Risk scores help release coordinators and product managers identify potential issues early and take corrective action. The risk score is calculated for the current in-progress phase and is recalculated each time you view the Release overview dashboard.

Risk score is calculated differently for timeline-oriented releases and stage-oriented releases.

**Parent Topic:**[Digital Product Release reference](dpr-reference.md)

## Risk score for timeline-oriented releases

The risk score of timeline-oriented releases combines overdue task scores and policy failure scores, weighted by their respective importance. The weight or priority to overdue tasks and policy failure determines their urgency or impact on a release. The score ranges from 0 to 100.

Risk scores help release coordinators and product managers identify potential issues early and take corrective action. The risk score is calculated for the current in-progress phase. The score isn’t calculated for completed or cancelled releases.

### Risk factors for timeline-oriented releases

The risk score for a timeline-oriented release is based on the following factors.

-   **Overdue tasks**

    The overdue task score is categorized based on the percentage of overdue tasks.

    More overdue tasks contribute to a higher risk score.

-   **Policy failure**

    The policy failure score is determined by the percentage of failed policies.

    Non-compliant policies increase the risk score.


### Risk score calculation

Given `overdue_weight + policy_failure_weight = 1`, the risk score of a release is calculated according to the following formula:

`Risk score = Round((Overdue task score * overdue_weight + Policy failure score * policy_failure_weight) * (Number of days elapsed in release / Total number of days in release))`

Where each metric is calculated as follows:

-   **Overdue task score:**

    -   If &lt;10% of tasks are overdue, the overdue task score is 0.
    -   If 10-40% of tasks are overdue, the overdue task score is 1.
    -   If &gt;40% of tasks are overdue, the overdue task score is 2.
    If a task has no end date, the phase's end date is used as the task's due date.

-   **Policy failure score:**
    -   If &lt;10% of policies fail, the policy failure score is 0.
    -   If 10-40% of policies fail, the policy failure score is 1.
    -   If &gt;40% of policies fail, the policy failure score is 2.

Based on the calculated risk score, the release is categorized into one of the following risk levels:

-   Low, if the value is 0 or 1
-   Medium, if the value is 2
-   High, if the value is 3
-   High, if the value is 4

This categorization can help you determine the risks involved with the release, thus enabling you to take measures to reduce these risks in a timely manner.

**Related topics**  


[Release Overview dashboard](dpr-release-overview-dashboard.md)

[Managing stage-oriented releases](dpr-working-stage-release.md)

## Risk score for stage-oriented releases

The risk score for stage-oriented releases evaluates the likelihood of delays or issues in the current phase based on task completion, policy compliance, progress thresholds, and readiness date proximity. The score ranges from 0 to 100.

Risk scores help release coordinators and product managers identify potential issues early and take corrective action. The risk score is calculated for the current in-progress phase. The score isn’t calculated for completed or cancelled releases.

### Risk factors for stage-oriented releases

The risk score for a stage-oriented release is based on four factors. Each factor produces a value from 0 through 1, which is then multiplied by its assigned weight.

-   **Work risk**

    The ratio of incomplete tasks to total tasks in the current phase. A task is considered closed when its state is Closed Complete or Closed Incomplete. If the phase has zero or one task, the work risk is 0.

    Work risk = 1 - \(closed tasks / total tasks\)

    A lower completion ratio contributes to a higher risk score.

-   **Policy risk**

    The ratio of non-compliant policies to total completed policy executions in the current phase. Only policies with a completed execution status are counted. If no policies have been executed, the policy risk is 0.

    Policy risk = \(non-compliant policies / total completed policies\)

    Non-compliant policies increase the risk score.

-   **Stage progress risk**

    Measures whether task completion has reached a minimum progress threshold. The default threshold is 20%. If the closed task ratio meets or exceeds the threshold, the stage progress risk is 0.

    Stage progress risk = max\(0, 1 - \(closed task ratio / 0.2\)\)

-   **Time pressure risk**

    Measures the proximity to the release readiness date. This factor is only included when a readiness date is defined on the release target. Risk increases as the readiness date approaches, using a 14-day threshold. If the readiness date has passed, the time pressure risk is 1.

    Time pressure risk = 1 - \(days remaining / 14\)


### Risk score calculation

The risk score formula uses different weights depending on whether a readiness date is defined on the release target.

-   **With a readiness date:**

    `Risk score = Round(((0.3 × Work risk) + (0.4 × Policy risk) + (0.1 × Stage progress risk) + (0.2 × Time pressure risk)) × 100)`

-   **Without a readiness date:**

    `Risk score = Round(((0.5 × Work risk) + (0.4 × Policy risk) + (0.1 × Stage progress risk)) × 100)`

    When no readiness date is defined, the work risk weight increases from 30% to 50% to compensate for the absence of time pressure.


The following table summarizes the weight assigned to each factor.

|Factor|With readiness date|Without readiness date|
|------|-------------------|----------------------|
|Work risk|30%|50%|
|Policy risk|40%|40%|
|Stage progress risk|10%|10%|
|Time pressure risk|20%|Not applicable|

The final score is capped from 0 through 100. A score of 0 indicates no identified risk. A score of 100 indicates the highest risk level.

### When the risk score is zero

The risk score returns 0 in the following cases:

-   The release is in the Completed or Cancelled state.
-   No phase is currently in progress.
-   The current phase has no tasks and no completed policy executions.

**Related topics**  


[Release Overview dashboard](dpr-release-overview-dashboard.md)

[Managing stage-oriented releases](dpr-working-stage-release.md)

