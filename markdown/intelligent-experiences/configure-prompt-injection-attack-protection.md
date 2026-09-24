---
title: Configure prompt injection attack protection
description: Activate or deactivate prompt injection attack detection to protect all generative AI applications and AI-generated text and conversations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/configure-prompt-injection-attack-protection.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Now Assist, prompt injection attck prevention, Generative AI, GenAI, Guardian, Admin, Detection impact]
breadcrumb: [AI Guardian, AI Admin Hub Settings, Exploring AI Admin Hub, AI Admin Hub, Generative AI skills, Enable AI Experiences]
---

# Configure prompt injection attack protection

Activate or deactivate prompt injection attack detection to protect all generative AI applications and AI-generated text and conversations.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

Prompt injection attacks are a type of cybersecurity attack where someone tries to override the initial instructions of an LLM to cause unintended behaviors. AI Guardian detect and log these prompt injection attack attempts across all generative AI applications and features. You can also configure the prompt injection detection guardrail to block the AI-generated response when an attack is detected in addition to logging it.

You can export logs for review. For more information, see [Export Now Assist Guardian logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/export-now-assist-guardian-logs.md).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  In the side panel, go to **Now Assist Guardian** &gt; **Prompt Injection**.

3.  Select the toggle to activate or deactivate prompt injection attack detection.

4.  Under **Detection impact**, select the options icon \(\[Omitted image "naa-more-options-icon.png"\] Alt text: Options icon.\) and then select **Edit** to change how detected attacks are handled.

    You can choose whether prompt injection attacks are blocked as well as logged.

    \[Omitted image "image.na-guradian-prompt-injection"\] Alt text: Prompt injection protection detection impact selection card with an option to choose the detection impact.


## Result

Prompt injection detection is configured on your instance. When enabled, you see a standard error message when an attack is detected.

**Parent Topic:**[AI Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-guardian.md)

