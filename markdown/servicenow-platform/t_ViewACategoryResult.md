---
title: View an assessment category result
description: Category results contain values that represent an evaluated record's performance in a specific metric category. Each category result record stores data from one assessment group. Category result values are calculated based on category and metric weights and from metric result values for the same category.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [View a quiz designer scorecard, View a quiz result, Quiz designer, Using Quizzes, Quizzes, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View an assessment category result

Category results contain values that represent an evaluated record's performance in a specific metric category. Each category result record stores data from one assessment group. Category result values are calculated based on category and metric weights and from metric result values for the same category.

## Before you begin

Role required: assessment\_admin or admin

## About this task

**Note:** The system does not include metric results from certain responses in category result calculations. To compensate, the system adjusts the weight of the other normalized metric result values within the same category.

## Procedure

1.  Navigate to **All** &gt; **Assessments** &gt; **Results** &gt; **Category Results**.

2.  Click the reference icon next to an assessment group number to open the category result record.

3.  View the Assessment Category Result form.

    All fields on the form are read-only.

<table id="table_odb_vcj_w4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

Name of the metric category that the category result values apply to.

</td></tr><tr><td>

Rating

</td><td>

Rating is used on scorecards and decision matrixes. Rating is updated dynamically as users complete assessments. Rating is calculated as:```
(Sum of all normalized values that share a particular assessment group, category, and assessable record) / (Number of assessment instances for the assessment group)
```

 For example: In the Assessment Category Results table example, the assessment group **ASG0000801** with category **Politeness** from group **NY DB** \(the assessable record\) has a **Rating** value **8.86**.

 On the associated Metric Results table, you can see that there are **4** instances of this group: **AINST0000801**, **AINST0000802**, **AINST0000803**, and**AINST0000804**.

 The system calculated the rating using

```
(5.14+5.14+1.43+5.71+5.14+4.29+4.29+4.29) / 4 = 8.86
```

</td></tr><tr><td>

Assessment group

</td><td>

Assessment group to which the category result is associated. The category result **Rating** and **Normalized value** are calculated from metric results in this assessment group only.

</td></tr><tr><td>

Normalized value

</td><td>

Calculated value that measures the **Rating** relative to the weights of categories used to assess the record evaluated.

 The normalized value is calculated as follows:

 Normalized value = Rating x \(Associated category weight / Sum of weights of all categories the source record has category results for in this assessment group\)

 Example: A source record has four associated category results in assessment group ASG0000907, one for each of these categories:

-   Importance Rating \(weight = 10\)
-   Product Reliability \(weight = 9\)
-   Company Alignment \(weight = 9\)
-   Compliance Score \(weight = 9\)
 If this source record's category result for Product Reliability has a Rating of 7.81, the normalized value calculation is:

 7.81 x \[9 / \(10+9+9+9\)\] = 1.9

</td></tr><tr><td>

Weight

</td><td>

Weight of the associated category. You may need to configure the form to see this field.

</td></tr><tr><td>

Source

</td><td>

Record evaluated as the assessment subject. You may need to configure the form to see this field.

</td></tr></tbody>
</table>
**Parent Topic:**[View a quiz designer scorecard](t_ViewAQuizDesignerScorecard.md)

**Related topics**  


[Assessment results](../reference/r_AssessmentResults.md)

[bundle-platadm.configure-form-layout]

[View a metric result](t_ViewAMetricResult.md)

