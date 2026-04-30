---
title: Add skills to a course with skill sensing
description: Add skills to a course manually using the Large Language Model \(LLM\) skills recommendations based on the title and description of the course.
locale: en-US
release: yokohama
product: Learning Core
classification: learning-core
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 2
breadcrumb: [Skill sensing for learning content, Using My Learning, Learning, Talent Development, Employee Service Management]
---

# Add skills to a course with skill sensing

Add skills to a course manually using the Large Language Model \(LLM\) skills recommendations based on the title and description of the course.

## Before you begin

Role required: Learning admin

Plugin requirement: Now Assist for HR Service Delivery \(HRSD\) plugin \(sn\_hr\_gen\_ai\), Learning core plugin \(sn\_learning\_core\), and Skills foundation plugin \(sn\_skills\_int\).

**Note:** Manual skill recommendation works for Internal courses, external courses, exams and assessments. The recommendations don't work for Paths and collections.

## Procedure

1.  Navigate to **All** &gt; **Learning** &gt; **Content** &gt; **Internal content/External content**.

2.  Select a course for which you want to add skills.

3.  Select **Add skills**.

4.  Select **Get recommendations**.

    -   The skills recommended are populated from the Review skills recommendation table based on the title and description of the course.
    -   The existing skills that are tagged to a course are not recommended again.
    -   The **Get recommendations** option is displayed only when you are adding skills to a course for the first time. From the next time onwards, the **Refresh recommendations** option is displayed.
5.  In the Recommended skills list, select **Add** to add the skill, and **Discard** to reject the skill.

    -   Skills once discarded are not recommended again unless manually deleted from the Recommended skills list.
    -   The discarded skills are in the Review skills recommendation table in the Rejected state. You can manually restore the skills status from this table.
6.  In the Selected skills list, you can see the skills that are added also change the level type of a skill.

7.  In the Search for a skill field, type in a skill name and add it to the selected skills list.

    You cannot add the skills that are already in the Selected skills list.

8.  Select **Add skill\(s\)** to confirm the selection.

    Only after you select the Add skills\(s\) option, the changes are saved.


## Result

-   The added skills are linked to the course and displayed in its Associated skills list. They are also stored in the Course item skills table \(sn\_lc\_course\_item\_m2m\_cmn\_skill\) and removed from the Review skills recommendation table.
-   Discarded skills move to the Review skills recommendation table with a Rejected status. You can later change their status to Pending or Accepted.

**Parent Topic:**[Skill sensing for learning content](../concept/skill-sensing-for-learning-content.md)

