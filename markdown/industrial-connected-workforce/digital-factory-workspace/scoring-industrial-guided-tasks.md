---
title: Scoring in Industrial Guided Tasks
description: Scoring enables the automatic calculation of performance scores after completing an Industrial Guided Task \(IGT\).
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Industrial Guided Tasks, Explore, Digital Factory Workspace, Industrial Connected Workforce]
---

# Scoring in Industrial Guided Tasks

Scoring enables the automatic calculation of performance scores after completing an Industrial Guided Task \(IGT\).

By using scoring, operators are provided with immediate feedback to support continuous improvement in a task execution and operating conditions. You can enable scoring for a standard using the IGT standard form. Scoring enables you to assign values to questions in task authoring and customize how results are calculated.

You can enable scoring at two points:

-   During standard creation: Scoring can be enabled directly in the IGT standard form. Once enabled, you can immediately configure scores for questions in the Task authoring interface.
-   For an existing standard: If scoring is enabled after the standard is created, you must refresh the Workspace. After refreshing, scoring options become available in Task authoring.

If scoring is enabled on the IGT standard:

-   The system calculates the total score for the IGT based on the results of the linked assessment template.
-   The Score status reflects how the total score compares to the Target score set in the standard:
    -   If the total score is equal to or greater than the target score, the task is marked as Successful.
    -   If the total score is below the target score, the task is marked as Unsuccessful.
-   If scoring is enabled but no target score is set on the standard, the score status is set to No target available. In this case, only the total score is displayed and the score status is hidden from the guided task.
-   If scoring isn’t enabled or the user doesn’t complete the scoring, the score status is set to Not scored.

## Scoring without a target score

You can enable scoring on an IGT standard without setting a target score. This is useful when you want to capture and display a total score for a task without evaluating whether the result is successful or unsuccessful.

The following table describes the scoring behavior based on whether a target score is set.

|Scenario|Behavior|
|--------|--------|
|Scoring is performed and the standard has a target score|Score status displays as Successful or Unsuccessful based on the comparison of the total score against the target score. Both the total score and the score status are displayed on the guided task.|
|Scoring is performed and the standard does not have a target score|Score status is set to No target available. The total score is displayed on the guided task. The score status field is hidden from the guided task view.|
|Scoring is not performed|Score status displays as Not scored.|

## Score normalization

Score normalization allows ICW administrators to apply advanced scoring calculations to Industrial Guided Tasks. When normalization is enabled on the assessment template category, you can use normalization strategies to adjust raw scores before they are saved to the guided task.

When normalization is enabled:

-   An ICW administrator modifies the Industrial Guided Task assessment template category to enable normalization.
-   Authors enable normalized scoring on a Guided Task Standard through the Advanced configuration view in the Smart Assessment Workspace.
-   The system saves the normalized score to the guided task instead of the raw score.

**Parent Topic:**[Exploring Industrial Guided Tasks](exploring-industrial-guided-tasks.md)

**Related topics**  


[Configure scoring and automation in Industrial Guided Tasks](../task/configure-scoring-automation-igt.md)

