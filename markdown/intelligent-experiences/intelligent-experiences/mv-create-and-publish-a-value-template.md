---
title: Create and publish a value template
description: A value template defines the formula used to calculate productivity gains for mapped AI systems. After you publish a template, the value job runs automatically and populates the Value dashboard.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-08-12"
reading_time_minutes: 3
keywords: [create value template, publish value template, AI Control Tower]
---

# Create and publish a value template

A value template defines the formula used to calculate productivity gains for mapped AI systems. After you publish a template, the value job runs automatically and populates the Value dashboard.

## Before you begin

Role required: sn\_ai\_governance\_ai\_steward

## About this task

Create a value template when you want to measure the productivity value of one or more AI systems. You define the metric once, map the AI systems that the metric applies to, test the calculation, and then publish the template.

The template flow includes three stages: Formula, Mapping, and Test \(optional\). All fields remain editable until you publish the template.

Productivity is calculated as: Usage × Time × Quality. Where Usage is how often an asset is used, Time is how much time it saves per use, and Quality is the share of outputs that are accepted.

A template saved as a draft is listed in the Draft state and does not calculate value until you publish it.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home**.

2.  Navigate to **Settings** &gt; **Rules and Templates** &gt; **Templates** &gt; **All templates**.

3.  Select **Create template**.

4.  Enter a name, a department, and a description for the template.

    The template detail fields are described in the following table.

    |Field|Description|
    |-----|-----------|
    |**Template name**|Enter a unique name for the template. This field is required.|
    |**Value template category**|Select the category, such as **Productivity**. The Productivity category measures total productivity gain in terms of time saved.|
    |**Department**|Select the department that the template applies to.|
    |**Description**|Enter a description of the template.|

5.  In the **Persona** field, select the persona that the AI system supports, such as **Agent**.

6.  In the **Usage** field, select the indicators that measure execution, such as agent execution, use case execution, skill execution, worker execution, or third-party system execution.

7.  Set the time value type.

    Select an indicator to derive time saved from usage, or select a constant to apply a fixed baseline that you define.

8.  From the **Quality type** list select an option.

    When you select the quality score, the value defaults to 50 percent. You can overwrite the default value.

    **Note:**

    Productivity = Usage × Time × Quality. Productivity is calculated by multiplying how often an asset is used, how much time it saves per use, and the share of outputs that are accepted.

    The calculation builder fields are described in the following table.

    |Field|Description|
    |-----|-----------|
    |**Persona**|Select the persona that the metric applies to. This field is required.|
    |**Usage**|Select the usage metric for the calculation. This field is required.|
    |**Time value type**|Select how the time value is provided, such as constant or an indicator.|
    |**Time constant \(in minutes\)**|Enter the time saved per use, in minutes. This field is required when the time value type is constant.|
    |**Quality type**|Select how the quality \(acceptance\) value is provided, such as constant or an indicator.|
    |**Quality constant \(in %\)**|Enter the share of outputs that are accepted, as a percentage. This field is required when the quality type is **Constant**.|

    To include additional metrics in the calculation, select **Add metrics**.

9.  Select **Save as draft**.

10. Select **Next** to map the AI systems that the metric applies to.

11. Select an AI system type, such as **Generative AI** or **Agentic AI**, and then select the AI systems to map.

12. Select **Map AI systems**.

    You can select more than one AI system. Your selections are saved automatically.

13. Select **Next**.

14. Select the AI systems to test, and then select **Validate and calculate**.

    You can select up to 10 AI systems at a time. The value job runs and shows the numbers under current productivity or new productivity, depending on whether the AI system already has a template.

15. Select **Publish template**.

    If a selected AI system already has a published template, a message states that the existing mapping is retired when you publish. Confirm the override to continue.


## Result

The template is published and mapped to the selected AI systems. The value job calculates the productivity gains for the previous day and shows them on the Value dashboard.

The template is listed on the **Templates** tab. A template saved with **Save as draft** is listed in the Draft state and does not calculate value until you publish it.

