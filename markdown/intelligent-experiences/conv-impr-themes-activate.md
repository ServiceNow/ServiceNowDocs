---
title: Activating Conversation Improvement Themes
description: Activate the Conversation Improvement Themes application to analyze conversation quality.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Conversation Improvement Themes, Enable AI experiences]
---

# Activating Conversation Improvement Themes

Activate the Conversation Improvement Themes application to analyze conversation quality.

## Before you begin

Role required: admin

Conversation evaluations have to be enabled in AI Control Tower. For more information, see .

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin Console** &gt; **Now Assist Skills**.

2.  Within the Platform category, select the feature **Conversation Evaluator** and verify that all the skills shipped with the Conversation Evaluator application are activated.

3.  After that, activate the skills shipped with this application.

    -   Theme Extraction
    -   Themes Update Definition
    -   Themes Primary Request Tagging
4.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    Apply the filter: `Application = Conversation Improvement themes`. Activate all scheduled jobs.

    -   Create thematic executions
    -   Evaluations for themes \[Daily job\]
    -   Evaluations for themes \[Historic job\]
    -   Themes - Create Daily Primary Request Executions
    -   Update Theme Effective and Ineffective Scores
5.  For access to the application, assign the following roles to the users:

    -   sn\_na\_thematic.theme\_admin
    -   sn\_na\_conv\_eval.eval\_admin
    **Note:**

    Only users who have access to the roles mentioned previously can access the data on the Conversation Improvements dashboard and the tables. But they won't be able to see live agent invocations.

    User must have the following roles to access all the data on the themes dashboard:

    -   sn\_na\_thematic.theme\_admin
    -   sn\_na\_conv\_eval.eval\_admin
    -   Interaction\_admin

