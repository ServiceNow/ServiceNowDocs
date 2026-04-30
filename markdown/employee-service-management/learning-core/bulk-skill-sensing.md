---
title: Add or discard multiple skills with skill sensing
description: Review and approve the Large Language Model \(LLM\) recommended skills before tagging​ them to the learning courses.
locale: en-US
release: zurich
product: Learning Core
classification: learning-core
topic_type: task
last_updated: "2025-11-05"
reading_time_minutes: 1
breadcrumb: [Skill sensing for learning content, Use, Learning, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Add or discard multiple skills with skill sensing

Review and approve the Large Language Model \(LLM\) recommended skills before tagging​ them to the learning courses.

## Before you begin

Role required: Learning admin

Plugin requirement: Now Assist for HR Service Delivery \(HRSD\) plugin \(sn\_hr\_gen\_ai\), Learning core plugin \(sn\_learning\_core\), and Skills foundation plugin \(sn\_skills\_int\).

## Procedure

1.  Navigate to **All** &gt; **Learning** &gt; **Learning Skill Recommendations** &gt; **Review Skill Recommendations**.

    -   All recommended skills from learning courses are shown, including those in Pending and Rejected states, listed in the order they were imported.
    -   The Source column shows where the skills originated: LLM for AI-generated skills and NULL for skills created manually.
2.  Select the skills that you want to accept.

3.  Select the **Actions on selected rows** drop-down.

    -   Select **Accept skills** to approve the skills.
    -   Select **Reject skills** to decline the skills.
    **Note:** Skills in the Pending state are deleted six months after their creation, while skills in the Rejected state are deleted nine months after the created date.

4.  Select **Proceed** to accept the selected skills.

    The selected skills are added to the Course item skills table \(sn\_lc\_course\_item\_m2m\_cmn\_skill\) and linked to the relevant learning courses. They are then removed from the Course Item Recommended Skills list.


