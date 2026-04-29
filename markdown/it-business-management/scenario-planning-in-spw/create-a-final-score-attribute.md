---
title: Create a final score attribute
description: Learn how to create an attribute to calculate the final score of your Scoring Framework.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Custom scoring frameworks in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Create a final score attribute

Learn how to create an attribute to calculate the final score of your Scoring Framework.

## Before you begin

Role required: sn\_align\_core\_apw\_admin

## About this task

Create an attribute to calculate the final score of a Scoring Framework.

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Scoring Frameworks**.

2.  From the Scoring Frameworks list, select a framework for which you want to add the final score attribute.

3.  Select **New**, from the Scoring Framework Attributes related list.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Name that defines your Scoring Framework's final score.|
    |Type|Type of the label, such as choice, decimal, integer, or string.|
    |Description|Details of the Scoring Framework attribute.|

5.  Select the **Final score** option to mark this attribute as the final score attribute of your Scoring Framework.

6.  Select the **Calculated Value** tab and add a formula to derive the value of the final score attribute

    This formula should be based only on the scoring attributes of your scoring framework. In the this example, the ICE custom framework has the formula:

    ```
    ICE score = Impact * Confidence * Ease
    ```

    ![Final score formula of the ICE custom framework.](../images/ice-example.png)

7.  Select **Update**.


**Parent Topic:**[Custom scoring frameworks in Strategic Planning](../concept/custom-scoring-frameworks-in-strategic-planning.md)

