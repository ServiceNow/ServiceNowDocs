---
title: Troubleshoot a Now Assist skill
description: Run diagnostics for a skill on the Now Assist Admin console and get information about the status of your skill configuration.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Now Assist, skill, troubleshoot, diagnostic, nsa\_admin, Generative AI, GenAI]
breadcrumb: [Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Troubleshoot a Now Assist skill

Run diagnostics for a skill on the Now Assist Admin console and get information about the status of your skill configuration.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

Certain skills have diagnostic scripts that you can run from the Now Assist Admin console. These diagnostic scripts check for successful skill execution and setup of the underlying [capability definitions](../../generative-ai-controller/reference/reference-for-generative-ai-controller.md). If you've made a copy of a skill, you will not be able to run diagnostics on the skill copy.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features**.

    If you’re already in the Now Assist Admin console, select the **Now Assist Features** tab.

2.  In the navigation pane, select the workflow of the skill that you want to troubleshoot, such as **Technology** or **Customer**.

3.  On the feature card that contains the skill you want to troubleshoot, select **View details**.

4.  In the All available skills or Active skills section, select the more options icon ![More options icon.](../image/naa-more-options-icon.png) next to the skill that you want to make a copy of and select **Run diagnostics**.

5.  After the diagnostics are complete, review the results of each test.

    ![Modal with diagnostic results indicating an error "Error in executing capability Record Summarization"](../image/naac-troubleshooting-modal.png)


## What to do next

If you have identified any problems with your skill configuration, you can [edit the skill](edit-a-now-assist-skill.md) from the Now Assist Admin console.

If editing the skill does not solve the issue, you can [contact ServiceNow Support](http://www.servicenow.com/support/contact-support.html) for additional help.

**Parent Topic:**[Configuring Now Assist settings and features](../concept/configuring-na-landing.md)

