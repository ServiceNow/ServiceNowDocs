---
title: Enable Now Assist Guardian for AI agents
description: Identify and block offensive messages that are sent by human agents automatically by enabling Now Assist Guardian in AI agents. With this capability, you can help reduce your agentic workflow or test from being exposed to harmful content.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist AI agents, Enable AI experiences]
---

# Enable Now Assist Guardian for AI agents

Identify and block offensive messages that are sent by human agents automatically by enabling Now Assist Guardian in AI agents. With this capability, you can help reduce your agentic workflow or test from being exposed to harmful content.

## Before you begin

Role required: admin

## About this task

The Now Assist Guardian, which is a ServiceNow AI Platform capability in the Now Assist panel, is a set of guardrails that are designed to intercept and mitigate offensive, sensitive, or security-related issues that may arise during interactions with the Now Assist application.

For example, let's say that Now Assist Guardian detects an offensive message in the execution plan of an agentic workflow. When you try to trigger the plan or test it, Now Assist Guardian can step in to terminate the plan or test because it detected harmful content at the first step of the execution plan.

![Offensive message is detected during the execution plan and the execution of the agentic workflow is terminated.](../image/aia-offnsv-msg-dtctn-exction-trmntn.png)

For more information about the different guardrails, see Now Assist Guardian.

## Procedure

1.  Configure Offensiveness for AI agents.

    1.  In AI Agent Studio, navigate to the **Settings** tab.

        You’re directed to the Offensiveness page.

        ![User being directed to the Offensiveness page when selecting the Settings in AI Agent Studio.](../image/aia-offensiveness-page-new.png)

    2.  Turn on the Offensiveness setting for AI agents by using the toggle button.

        ![User turning on the Offensiveness setting for AI agents.](../image/aia-offensiveness-detection-enabled.png)

    3.  Configure the detection impact by selecting the options icon \(![More options icon.](../image/options-icon.png)\) to enable the detection impact to use the following options:

        ![Options to enable detection impact.](../image/aia-offensiveness-options.png)

        -   **Edit**: Choose the detection impact between logging or both blocking and logging.

            Enable the detection impact:

            1.  Select the **Edit** option.
            2.  On the Detection impact page, select either the **Log** or **Block and log** button based on your requirements.

                **Note:** You can switch the detection impact from **Log** to **Block and log** or from **Block and Log** to **Log** at any time.

            3.  Select **Save**.
        -   **Export**: Exports the offensiveness-based logs as a `.CSV` file. Logs can be analyzed for the types of content that are being identified so you can take other preventive measures, such as changing conversational questions.
2.  Configure Prompt Injection for AI agents.

    1.  In the AI Agent Studio, navigate to **Settings** &gt; **Prompt Injection** and select **Configure**.

        You’re directed to the Now Assist Admin page to configure the Prompt Injection.

        ![Prompt Injection page in AI Agent Studio.](../image/aia-prompt-injection-new.png)

        **Note:** For more information about configuring the Prompt Injection, see .

        When you configure the Prompt Injection for an agentic workflow by using the required instructions, the system is designed to detect harmful content and block the conversation.


