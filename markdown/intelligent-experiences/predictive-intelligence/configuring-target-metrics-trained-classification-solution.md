---
title: Configuring target metrics for a trained classification solution
description: Set values for precision, coverage, and recall statistics for a trained machine learning solution.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create and train a classification solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Configuring target metrics for a trained classification solution

Set values for precision, coverage, and recall statistics for a trained machine learning solution.

## Setting classification metric values at the class or solution level

Predictive Intelligence provides three classification metric types: precision, coverage, and recall. You configure these metrics on the Solution Statistics tab of a trained classification solution form. While you can manually set values to these metrics at the class level, doing so can be challenging if you have a large number of classes to cover. In many cases, you may not know the best value to set until your solution is trained. This topic focuses on setting the metric values at just the solution level.

## Configuring solution metrics

When you apply a value to one metric, it changes the values of the other two. This behavior enables you to modify your metrics iteratively in real time to see which value combinations render particular results. When you apply a new value to a metric, the system recomputes it by considering its new targets.

Applying a value to a metric asks the system to train its predictions to favor the metric you set based on the highest percentage value, and at a cost to the other metrics. The system tries to meet these values but may not set them exactly as you request due to how the data you're training is distributed.

When you apply metric values at the solution level, the system automatically sets the appropriate values at the class level.

Here are the basic steps for configuring a target metric for your solution.

1.  Navigate to the Solution Statistics tab of a trained ML solution.
2.  Review the messages on the green banners of the screen which define each of the metrics so you can better understand the values you want to assign to the solution. The first two message banners address estimated solution-level metrics. The third banner addresses class-level results based on the solution values you applied.
3.  In the **Target Metric** choice list, select the metric you want to configure.
4.  In the **Target Metric Value** field, enter a numeric percentile value between 0-100.
5.  Click **Apply Values**.
6.  Result: On the Solutions Statistics tab, you can review the change in values to the **Estimated Solution Precision**, **Estimated Solution Recall**, and **Estimated Solution Coverage**. The system calculates these values based on the **Target Metric** you select and the **Target Metric Value** you enter for the solution.

Here's a sample landing page for a recently trained classification solution. As you can see, the precision metric is 44.18, recall is 41.26, and coverage is 77.23.

![This sample image shows the estimated values set for solution precision, recall and coverage metrics.](../images/metric-default-solution.png)

If you need to adjust these default values for a use case, refer to the sample configurations below. For example, based on the classification solution you're implementing, you might want to change the target metric value for precision, recall, or coverage. Keep in mind that when you change the target metric value for one metric, such as precision, it impacts the values of the recall and coverage metrics as well.

## Precision configuration example

In this example scenario, you're replacing a manual triage process for routing incident records with an ML classification solution that automatically assigns the records to the correct assignment group. For this scenario, you have a target value in mind and the system must predict correctly at least 80% of the time. So you set the precision metric value to `80` and click **Apply Values**.

![This image shows you how to set the Precision metric to 80%.](../images/metric-precision-example.png)

Here are the metric values the system applied to the solution. In this scenario, the precision value of 80.04 slightly exceeded your request for 80%, so you're likely satisfied with that value.

![This image shows you the estimated precision, recall, and coverage values the system assigned to the solution based on your Precision input value of 80%.](../images/metric-precision-example-result.png)

## Coverage configuration example

In another example scenario where you're replacing a manual triage process for routing incident records, your minimum goal is to predict at least 70% of incoming incidents in the first quarter of the year. So you set the coverage metric value to `70` and click **Apply Values**.

![How to set the Coverage metric to 70%.](../images/metric-coverage-example.png)

The metric values the system applied to the solution are shown in the following image. The coverage metric value increased from 35.99 to 55.98. However, the precision metric decreased from 80.18 to 64.97. This could be because you set the coverage metric to a relatively high value of 70, or perhaps because of how the data you're training is distributed.

![The estimated precision, recall, and coverage values the system assigned to the solution based on your Coverage input value of 70%.](../images/metric-coverage-example-result.png)

## Recall configuration example

In another scenario, classifying if an incoming email is a Phish or not can be an important use case in a security-related machine learning solution. In this situation, it's very important to identify every Phish, and it may be okay to report a non-Phish as a Phish occasionally. However, no real Phish should be classified as a non-Phish. In such situations, the recall metric must have a high value, which might lead to lower percentages for precision and coverage. So here you can set the recall metric to `95` and click **Apply Values**.

![This image shows you how to set the Recall metric to 95%.](../images/metric-recall-example.png)

Here are the metric values the system applied to the solution. The recall metric value increased from 54.87 to 61.03. However, the precision metric decreased from 60.1 to 55.44. This is likely because you set the recall metric to the high value of 95.

![The estimated precision, recall, and coverage values that the system assigned to the solution based on your Recall input value of 95%.](../images/metric-recall-example-result.png)

## Class-level results for the solution metric values you apply to your solution

The following image shows an example of the class-level results the system applied to a solution's precision, coverage, and recall statistics for 37 classes. You can keep modifying the metric values until you're fully satisfied with the results.

By Sorting \(z to a\) on the Estimated Precision column you can see which classes have the highest precision for the solution.

![The class-level results the system applied to a solution's precision, coverage, and recall statistics for 37 classes.](../images/metric-all-example-result-classes.png)

