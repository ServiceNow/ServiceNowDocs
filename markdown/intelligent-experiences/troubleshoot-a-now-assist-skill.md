---
title: Troubleshoot an AI skill
description: Run diagnostics for a skill on AI Admin Hub and get information about the status of your skill configuration with AI Troubleshooting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/troubleshoot-a-now-assist-skill.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, skill, troubleshoot, diagnostic, nsa\_admin, Generative AI, GenAI]
breadcrumb: [AI Admin Hub reference, AI Admin Hub, Enable AI experiences]
---

# Troubleshoot an AI skill

Run diagnostics for a skill on AI Admin Hub and get information about the status of your skill configuration with AI Troubleshooting.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

Certain skills have diagnostic scripts that you can run from the AI Admin Hub. These diagnostic scripts check for successful skill execution and setup of the underlying [capability definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/generative-ai-controller/reference-for-generative-ai-controller.md). If you've created a copy of a skill, you will not be able to run diagnostics on the skill copy.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

    If you’re already in the AI Admin Hub, select the **AI Skills** tab.

2.  In the navigation pane, select the workflow of the skill that you want to troubleshoot, such as **Technology** or **Customer**.

3.  On the feature card that contains the skill you want to troubleshoot, select **View details**.

4.  In the All available skills or Active skills section, select the more options icon \[Omitted image "naa-more-options-icon.png"\] Alt text: More options icon. next to the skill that you want to make a copy of and select **Run diagnostics**.

    **Run diagnostics** option is not applicable for skills where this option is not available or applicable.

5.  After the diagnostics are complete, review the results of each test.

    \[Omitted image "naac-troubleshooting-modal.png"\] Alt text: Modal with diagnostic results indicating an error "Error in executing capability Record Summarization"


## What to do next

If you have identified any problems with your skill configuration, you can [edit the skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/edit-a-now-assist-skill.md) from the AI Admin Hub console.

If editing the skill does not solve the issue, you can [contact ServiceNow Support](http://www.servicenow.com/support/contact-support.html) for additional help.

**Parent Topic:**[AI Admin Hub reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-reference-landing.md)

