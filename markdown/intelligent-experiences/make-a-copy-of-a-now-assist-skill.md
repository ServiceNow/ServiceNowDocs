---
title: Make a copy of an AI skill
description: Create a copy of an AI skill using the Make a copy function in AI Admin Hub. With a copy of the skill, you can experiment with skill settings and tailor the skill to fit your business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/make-a-copy-of-a-now-assist-skill.html
release: australia
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 2
keywords: [Copy, Now Assist, skill, admin, features]
breadcrumb: [Using AI Admin Hub, AI Admin Hub, Enable AI experiences]
---

# Make a copy of an AI skill

Create a copy of an AI skill using the **Make a copy** function in AI Admin Hub. With a copy of the skill, you can experiment with skill settings and tailor the skill to fit your business needs.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

The skills that come with the generative AI applications have default configurations that are optimized to serve the most common use cases. To change the skill settings you can edit a skill in AI Admin Hub, or you can create a copy of the skill. Creating a copy leaves the original skill configuration intact in case you want to use it later or want to create another copy from the original. You can activate and configure copies of skills using the same guided setup as the default skills.

**Note:**

-   The **Make a copy** function is not available for all AI skills.
-   In a default scenario, only one version of a skill can be active at a time. When you create and activate a copy of a skill, any previously activated version of the skill is deactivated.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

    If you’re already in AI Admin Hub, select the **AI Skills** tab.

2.  In the navigation pane, select the workflow of the skill that you want to copy, such as Technology or Customer.

3.  On the card that contains the default skill you want to copy, select the more options icon \[Omitted image "naa-more-options-icon.png"\] Alt text: More options icon. then select **Make a copy**.

4.  As an alternative to the previous step, select **View details**, then on the details tab select **Make a copy** from the More actions drop-down list at **Edit configuration**.

5.  In the modal window, select **Make a copy** to confirm.


## Result

A copy of the skill is generated and you're taken to the guided setup.

## What to do next

Continue the steps in the guided setup to activate the skill. For more information, see [Activate a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/configure-a-now-assist-skill.md).

If you're making a copy of the case or incident summarization skill and would like to learn more about your options, see the [documentation for configuring record summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/configure-case-or-incident-summarization-in-the-now-assist-admin-console.md).

-   **[Configure case or incident summarization in the AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/configure-case-or-incident-summarization-in-the-now-assist-admin-console.md)**  
Configure case or incident summarization by using the guided setup in the AI Admin Hub console. You can choose the input tables and fields and customize the prompt output for copies of the record summarization skills.

**Parent Topic:**[Using AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/using-now-assist-admin_0.md)

