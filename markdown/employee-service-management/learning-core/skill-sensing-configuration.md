---
title: Configuration for bulk skill sensing
description: Define conditions to create a sub set of learning courses on which you can run the scheduled job enabling you to accept multiple recommended skills.
locale: en-US
release: yokohama
product: Learning Core
classification: learning-core
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 2
breadcrumb: [Skill sensing for learning content, Using My Learning, Learning, Talent Development, Employee Service Management]
---

# Configuration for bulk skill sensing

Define conditions to create a sub set of learning courses on which you can run the scheduled job enabling you to accept multiple recommended skills.

## Before you begin

Role required: Learning admin

Plugin requirement: Now Assist for HR Service Delivery \(HRSD\) plugin \(sn\_hr\_gen\_ai\), Learning core plugin \(sn\_learning\_core\), and Skills foundation plugin \(sn\_skills\_int\).

## Procedure

1.  Navigate to **All** &gt; **Learning** &gt; **Learning Skill Recommendations** &gt; **Skill Sensing Configuration**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_q1t_5xv_chc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table from which the courses are extracted.

</td></tr><tr><td>

Condition

</td><td>

Use the **Add Filter Condition** option to refine the learning courses for the condition types that are set. All the learning courses that meet this condition receive skill recommendations.**Note:**

-   The trigger conditions are based on Learning Course items \(internal courses, external courses, and exams\).
-   If there are no records matching the condition, you cannot generate the recommended skills.


</td></tr><tr><td>

Exclude courses below minimum skills count

</td><td>

Filter the learning courses that already have a specific number \(Minimum skills count\) of skills tagged. For example, if the Minimum skill count is three, the courses that have three skills or above are not considered.

</td></tr><tr><td>

Exclude courses that already have recommended skills

</td><td>

Omits the learning courses that already have skills recommended by Large Language Model \(LLM\).

</td></tr><tr><td>

Include active courses with recent learner activity

</td><td>

Include learning courses that have any recent activity like a course being assigned, started, in-progress.

 Note: Apart from the filter conditions, the above three fields can be used to further filter the courses.

</td></tr><tr><td>

Active

</td><td>

Make the configuration active.**Note:** Only one skill sensing configuration must be active at a given point.

</td></tr><tr><td>

Description

</td><td>

A description for the configuration.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Select **Generate recommended Skills** to generate skills recommendations.

    **Note:** If you don't have the Now Assist for HR Service Delivery \(HRSD\) plugin \(sn\_hr\_gen\_ai\) installed, the **Generate recommended Skills** option is not displayed.

6.  Select **Proceed** to create the records in the Review skills recommendation table.

    **Note:** If the system property sn\_lc.auto\_accept\_llm\_recommendations is set to True, all the recommended skills are automatically accepted and added to the Course item skills table \(sn\_lc\_course\_item\_m2m\_cmn\_skill\). The skills will also be linked to the respective learning courses based on the table mapping. By default, this property is set to False.

    .


**Parent Topic:**[Skill sensing for learning content](../concept/skill-sensing-for-learning-content.md)

