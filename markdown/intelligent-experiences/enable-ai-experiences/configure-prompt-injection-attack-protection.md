---
title: Configure prompt injection attack protection
description: Activate or deactivate prompt injection attack protection for AI-generated text and conversations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/intelligent-experiences/enable-ai-experiences/configure-prompt-injection-attack-protection.html
release: xanadu
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2024-11-22"
reading_time_minutes: 1
keywords: [Now Assist, prompt injection attck prevention, Generative AI, GenAI, Guardian, Admin, Detection impact]
breadcrumb: [Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Configure prompt injection attack protection

Activate or deactivate prompt injection attack protection for AI-generated text and conversations.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

Prompt injection attacks are a type of cybersecurity attack where someone tries to override the initial instructions of an LLM to cause unintended behaviors. Now Assist Guardian can detect and log these attack attempts, and you can choose whether you want to block the AI-generated response after the attack has been attempted.

See [Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/now-assist-guardian.md) for more information.

Logs can be exported for review. For instructions on how to do so, see [Export Now Assist Guardian logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/export-now-assist-guardian-logs.md).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  In the side panel, go to **Now Assist Guardian** &gt; **Prompt Injection**.

3.  Select the toggle to change the active status of prompt injection attack protection.

    Prompt injection attack protection is enabled by default, which means Now Assist Guardian logs attempts unless you turn it off.

4.  Under **Detection impact**, select the options icon \(\[Omitted image "naa-more-options-icon.png"\] Alt text: More options icon in the Now Assist Admin console\) and then choose **Edit** to change the detection impact.

    You can choose whether prompt injection attacks are blocked as well as logged.

    \[Omitted image "na-guardian-prompt-injection-detection-impact.png"\] Alt text: Prompt injection protection detection impact selection card with "log only" selected


## Result

You have configured whether prompt injection attack protection is enabled on your instance and determined what you want Now Assist Guardian to do in case of an attempt.

**Parent Topic:**[Configuring Now Assist settings and features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/configuring-na-landing.md)

