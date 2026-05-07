---
title: Configure prompt injection attack protection
description: Activate or deactivate prompt injection attack detection to protect all generative AI applications and AI-generated text and conversations on your instance from malicious inputs and unintended model behaviors.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, prompt injection attck prevention, Generative AI, GenAI, Guardian, Admin, Detection impact]
breadcrumb: [Now Assist Guardian, Agentic AI security and governance]
---

# Configure prompt injection attack protection

Activate or deactivate prompt injection attack detection to protect all generative AI applications and AI-generated text and conversations on your instance from malicious inputs and unintended model behaviors.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

Prompt injection attacks are a type of cybersecurity attack where someone tries to override the initial instructions of an LLM to cause unintended behaviors. Now Assist Guardian detects prompt injection attempts before they reach the model and either logs them or blocks the response, depending on your configuration. You can also configure the prompt injection detection guardrail to block the AI-generated response when an attack is detected in addition to logging it.

You can export logs for review. For more information, see [Export Now Assist Guardian logs](export-now-assist-guardian-logs.md).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  In the side panel, go to **Now Assist Guardian** &gt; **Prompt Injection**.

3.  Select the **Prompt Injection** toggle to activate prompt injection detection.

    ![Prompt Injection guardrail settings with the "Log the output" action and "Low" severity level selected.](../image/na-guardian-prompt-injection.png)

4.  In the **Choose an action when prompt injection is detected** section, select one of the following options to handle the detected attacks:

    -   To log the request and conversation while keeping the model response visible to the user, select **Log the output**.
    -   To block the model response and log the request and conversation, select **Block the response and log the output**.
5.  In the **Select the attack severity level to check for prompt injection** section, select a severity level to check for prompt injection.

    -   To flag even the slightest hints of injection or manipulation attempts, select **Low**.
    -   To flag clear or moderate prompt injection attempts, select **Medium**.
    -   To flag only high certainty prompt injection attempts, select **High**.
6.  Select **Save**.


## Result

Prompt injection detection is configured on your instance for all generative AI workflows. Now Assist Guardian detects prompt injection attempts based on the severity level you selected and responds according to the action you configured.

**Parent Topic:**[Now Assist Guardian](../../now-assist-platform/concept/now-assist-guardian.md)

