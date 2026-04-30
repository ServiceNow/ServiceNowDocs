---
title: Create a custom Merit Review scoring framework for a Grant Program in the Reviewer Service Portal
description: Start scoring grant proposals based on your agency's preferences by creating a custom scoring framework.Add attributes within your scoring framework.Add attributes within your scoring framework.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 3
breadcrumb: [Configure the Merit Review Scoring Framework and Rubric, Set up a grant program, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Create a custom Merit Review scoring framework for a Grant Program in the Reviewer Service Portal

Start scoring grant proposals based on your agency's preferences by creating a custom scoring framework.

## About this task

Scoring frameworks provide a structured method to evaluate and prioritize initiatives, projects, and demands based on predefined criteria. This allows merit reviewers to score applications based on the consistent criteria.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Scoring Frameworks**.

2.  Select **New**.

3.  Enter a name of your scoring framework in the **Name** field.

4.  Enter the details of your scoring framework in the **Description** field.

5.  Select the checkbox next to **Active** to make the framework available for use with the Reviewer service portal.

6.  Select **Submit**.


## What to do next

[Create a merit review scoring framework attribute](psds-config-gmp-create-scoring-framework.md#)

**Parent Topic:**[Configure the Merit Review Scoring Framework for a Grant Program in the Reviewer Service Portal](psds-config-gmp-scoring-framework.md)

## Create merit review scoring framework attributes for a Grant Program in the Reviewer Service Portal

Add attributes within your scoring framework.

### About this task

The following attribute types can be added to a scoring framework:

-   Choice: For attributes with predefined values \(such as high, medium, or low\)
-   Decimal: For attributes with number ranges and min/max values
-   Integer: For attributes with number ranges and min/max values
-   String: For the weighted calculation of all attributes

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Scoring Frameworks**.

2.  From the Scoring Frameworks list, select a framework for which you want to add the Scoring Framework Attributes.

3.  Select **New**, from the Scoring Framework Attributes related list.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Name that defines the scoring Framework.|
    |Type|Type of the label, such as integer, choice, star, and so on.|
    |Description|Details of the Scoring Framework.|

    **Tip:** If you want to add a choice type scoring attribute, you must have selected Decimal or Integer in the **Type** field, and Choice in the **Display type** field.

    To add a choice-list attribute:

    1.  In the Choices related list, select **New**.

5.  Select **Submit**.

6.  Repeat this procedure until all Scoring Framework Attributes have been added.

    **Note:** Every scoring framework can only have one final score. Select the checkbox for the final score attribute for only one attribute.


### What to do next

[Create a final score attribute for the merit review scoring framework](psds-config-gmp-create-scoring-framework.md#)

## Create a final score attribute for the merit review scoring framework

Add attributes within your scoring framework.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Scoring Frameworks**.

2.  From the Scoring Frameworks list, select a framework for which you want to add the final score attribute.

3.  Select **New**, from the Scoring Framework Attributes related list.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Name that defines your Scoring Framework's final score. **Enter Final Score**.|
    |Type|Type of the label, such as choice, decimal, integer, or string.|
    |Description|Details of the Scoring Framework attribute.|

5.  Select the **Final score** option to mark this attribute as the final score attribute of your Scoring Framework.

6.  Select the **Active** option to mark this attribute available for use with your Scoring Framework.

7.  Select the **Calculated Value** tab and add a formula to derive the value of the final score attribute

    This formula should be based only on the scoring attributes of your scoring framework.

8.  Select **Update**.


### What to do next

[Configure a merit review scoring rubric for a grants proposal](psds-config-gmp-create-rubric.md)

