---
title: Define a skill determination rule
description: Create a skill determination rule to tag the German skill to incoming cases from German speakers.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tutorial: Automatically assign work to agents by skill, Configure agent assignment rules, Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Define a skill determination rule

Create a skill determination rule to tag the German skill to incoming cases from German speakers.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Skills** &gt; **Skill Determination Rules**, and then select **New**.

2.  Enter the following information in the fields listed:

    -   **Name**: `Skill determination for German cases`
    -   **Active**: `true`
    -   **Source table**: **Case \[sn\_customerservice\_case\]**
    -   **Condition**: **Opened by.language is German**

        **Note:** Search for the `Show related fields` option when defining the conditions to get the Opened by.language option.

    -   **Skills**: German
3.  Select **Submit**.


## Result

Cases that need German speakers are routed to users in Customer Service and Support who have the German skill.

