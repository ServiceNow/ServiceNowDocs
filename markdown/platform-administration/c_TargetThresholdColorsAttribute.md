---
title: Target threshold colors attribute
description: If the target\_field attribute is configured, a second attribute called target\_threshold\_colors enables an administrator to define additional parameters.Add an optional attribute \(target\_field\) to a percent complete field to compare the actual completion percentage of a task or project with a target percentage in a different decimal field that specifies where the task should be at this point.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Percent complete field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Target threshold colors attribute

If the **target\_field** attribute is configured, a second attribute called **target\_threshold\_colors** enables an administrator to define additional parameters.

The parameters are:

-   Different thresholds at which the colored bar should change color
-   A specific color for each threshold

The format of this attribute's value is **number1:color1;number2:color2** and so on. Use this attribute to apply warning colors to completion percentages that are lower than target percentages. These values are defined as the percentage of target accomplished. For example, a value of **0:red;50:yellow;90:green** displays a red bar if the progress to target percentage is between 0-49. If the percent of target is between 50 and 89, the color is yellow. Percent of target 90 and above displays in green. Completion percentages that exceed target percentages also display in green. Order the color attributes from the smallest percentage to the largest.

If you do not specify a target\_field, then a target of 100 is used, allowing you to use the color thresholds with a single field value.

```
target_field=percent_complete_target,target_threshold_colors=0:tomato;50:khaki;90:lightgreen
```

The following table lists examples of percent of target calculation using the colors defined above.

|Target percent|Percent field value|Percent of target calculation|Color|
|--------------|-------------------|-----------------------------|-----|
|100|40|40%|tomato|
|65|59|90.7%|lightgreen|
|15|10|66.7%|khaki|

## Add a target field attribute

Add an optional attribute \(**target\_field**\) to a percent complete field to compare the actual completion percentage of a task or project with a target percentage in a different decimal field that specifies where the task should be at this point.

### Before you begin

Role required: personalize\_dictionary

### About this task

If a target field is not specified, the target of 100 is assumed.

### Procedure

1.  Right-click the **% Complete** field in a form.

2.  Select **Configure Dictionary** from the pop-up menu.

3.  In the Dictionary Entry form, add the following attribute:

    **target\_field=percent\_complete\_target**

4.  Update the dictionary record.

    In the list, a gray bar appears behind the colored bar to indicate the target value. The gray target bar appears only if you defined a target field.

    ![Percent complete](../image/PercentComplete4.png)


