---
title: Make a copy of a Now Assist skill
description: The 'Make a copy' feature enables you to create a copy of a Now Assist skill so that you can experiment with skill settings and configure the skill to fit your business needs.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Copy, Now Assist, skill, admin, features]
breadcrumb: [Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Make a copy of a Now Assist skill

The 'Make a copy' feature enables you to create a copy of a Now Assist skill so that you can experiment with skill settings and configure the skill to fit your business needs.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

The skills that come with the Now Assist applications have default configurations that are optimized to serve the most common use cases. If you want to change the skill settings, you can edit a skill with the Now Assist Admin console or you can create a copy of the skill. Creating a copy leaves the original skill configuration intact in case you want to use it later or want to create another copy from the original. You can activate and configure the copies of the skills by using the same guided setup as the default skills.

**Note:** The 'Make a copy' feature is not available for all Now Assist skills.

**Note:** In a default scenario, only one version of a skill can be active at a time. If you create and activate a copy of the skill, any previously activated version of the skill is deactivated.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

    If you’re already in the Now Assist Admin console, select the **Now Assist Skills** tab.

2.  In the navigation pane, select the workflow of the skill that you want to copy, such as Technology or Customer.

    Each workflow contains skills sets.

3.  Toggle between the list and grid layout for optimum view experience.

    **Note:** The skill details are presented at the forefront of the interface, enabling you to view all the details without needing to click or navigate away.

4.  Select the more options icon ![More options menu item](../../now-assist-platform/images/more-options-menu-item.png) next to **Active skill** that you want to configure, then select **Make a copy**.

5.  In the modal, select **Make a copy**

6.  You can choose to change the base input table entry as per the created copy.

    A confirmation message displays verifying the configuration changes.

7.  Select **Save** to confirm your changes and proceed to Guided Setup.


## Result

A copy of the skill is generated and you're taken to the Guided Setup.

## What to do next

Continue the steps in the guided setup to activate the skill. For more information, see [Activate a Now Assist skill](configure-a-now-assist-skill.md).

If you're making a copy of the case or incident summarization skill and would like to learn more about your options, see the [documentation for configuring record summarization](configure-case-or-incident-summarization-in-the-now-assist-admin-console.md).

-   **[Configure case or incident summarization in the Now Assist Admin console](configure-case-or-incident-summarization-in-the-now-assist-admin-console.md)**  
Configure case or incident summarization by using the guided setup in the Now Assist Admin console. You can choose the input tables and fields as well as customize the prompt output for copies of the record summarization skills.

**Parent Topic:**[Configuring Now Assist settings and features](../concept/configuring-na-landing.md)

