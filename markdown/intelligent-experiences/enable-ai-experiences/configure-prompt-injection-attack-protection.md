---
title: Configure prompt injection attack protection
description: Activate or deactivate prompt injection attack detection settings to protect all generative AI interactions on your instance from malicious inputs and unintended model behaviors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/configure-prompt-injection-attack-protection.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, prompt injection attck prevention, Generative AI, GenAI, Guardian, Admin, Detection impact]
breadcrumb: [Now Assist Guardian, Now Assist Admin Settings, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Configure prompt injection attack protection

Activate or deactivate prompt injection attack detection settings to protect all generative AI interactions on your instance from malicious inputs and unintended model behaviors.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

Now Assist Guardian detects and logs prompt injection attempts across all generative AI applications and features on your instance. You can configure Now Assist Guardian to block the AI-generated response when an attack is detected.

Prompt injection detection is enabled by default for all Now Assist skills, except Platform and custom skills, which can be configured manually. The default action is block and log, with a medium severity threshold. When a skill has its own setting, Now Assist Guardian automatically applies the more protective of the two settings, the skill-level setting or the instance-level setting.

You can export logs for review. For more information, see [Export Now Assist Guardian logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/export-now-assist-guardian-logs.md).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  In the side panel, go to **Now Assist Guardian** &gt; **Prompt Injection**.

3.  Select the **Enable at instance level** toggle to activate prompt injection detection at the instance, if it is not already enabled.

    \[Omitted image "na-guardian-prompt-injection.png"\] Alt text: Prompt Injection guardrail settings at instance level with the "Log the output" action and "Medium" severity level selected.

4.  In the **Choose an action when prompt injection is detected** section, select one of the following options to handle the detected attacks:

    -   To log the request and conversation while keeping the model response visible to the user, select **Log the output**.
    -   To block the model response and log the request and conversation, select **Block the response and log the output**.
5.  In the **Select the attack severity level to check for prompt injection** section, select a severity level to check for prompt injection.

    -   To flag even the slightest hints of injection or manipulation attempts, select **Low**.
    -   To flag clear or moderate prompt injection attempts, select **Medium**.
    -   To flag only high certainty prompt injection attempts, select **High**.
6.  In the **Product-specific configuration for skills** section, select the skill you want to configure.

    The Prompt injection for the selected skill page opens.

    1.  In the **Choose an action when prompt injection is detected** section, select the detection mode for the skill:

        -   To log the request and conversation while keeping the model response visible to the user, select **Log the output**.
        -   To block the model response and log the request and conversation, select **Block the response and log the output**.
        **Note:** This option is only available when the instance-level action is set to Log the output.

    2.  In the **Select the attack severity level to check for prompt injection** section, select a severity level, **Low**, **Medium**, or **High**.

    The skill uses the configured detection mode, or the global setting if it is stricter.

7.  Select **Save**.


## Result

Prompt injection detection is configured on your instance for all generative AI workflows. Now Assist Guardian detects prompt injection attempts based on the severity level you selected and responds according to the action you configured. When a skill has its own setting, the more protective setting applies automatically.

**Parent Topic:**[Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/now-assist-guardian.md)

