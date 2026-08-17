---
title: Enable AI Guardian for AI agents
description: Identify and block offensive messages that are sent by human agents automatically by enabling AI Guardian in AI agents. With this capability, you can help reduce your agentic workflow or test from being exposed to harmful content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-aia-na-guardian.html
release: australia
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Configure, AI Agent Studio, Enable AI experiences]
---

# Enable AI Guardian for AI agents

Identify and block offensive messages that are sent by human agents automatically by enabling AI Guardian in AI agents. With this capability, you can help reduce your agentic workflow or test from being exposed to harmful content.

## Before you begin

Role required: admin

## About this task

The AI Guardian, which is a ServiceNow AI Platform capability in the ServiceNow Otto panel, is a set of guardrails that are designed to intercept and mitigate offensive, sensitive, or security-related issues that may arise during interactions with the ServiceNow Otto application.

For example, let's say that AI Guardian detects an offensive message in the execution plan of an agentic workflow. When you try to trigger the plan or test it, AI Guardian can step in to terminate the plan or test because it detected harmful content at the first step of the execution plan.

\[Omitted image "aia-offnsv-msg-dtctn-exction-trmntn.png"\] Alt text: Offensive message is detected during the execution plan and the execution of the agentic workflow is terminated.

For more information about the different guardrails, see [AI Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-guardian.md).

## Procedure

1.  Configure Offensiveness for AI agents.

    1.  In AI Agent Studio, navigate to the **Settings** tab.

        You’re directed to the Offensiveness page.

        \[Omitted image "aia-offensiveness-page-new.png"\] Alt text: User being directed to the Offensiveness page when selecting the Settings in AI Agent Studio.

    2.  Turn on the Offensiveness setting for AI agents by using the toggle button.

        \[Omitted image "aia-offensiveness-detection-enabled.png"\] Alt text: User turning on the Offensiveness setting for AI agents.

    3.  Configure the detection impact by selecting the options icon \(\[Omitted image "options-icon.png"\] Alt text: More options icon.\) to enable the detection impact to use the following options:

        \[Omitted image "aia-offensiveness-options.png"\] Alt text: Options to enable detection impact.

        -   **Edit**: Choose the detection impact between logging or both blocking and logging.

            Enable the detection impact:

            1.  Select the **Edit** option.
            2.  On the Detection impact page, select either the **Log** or **Block and log** button based on your requirements.

                **Note:** You can switch the detection impact from **Log** to **Block and log** or from **Block and Log** to **Log** at any time.

            3.  Select **Save**.
        -   **Export**: Exports the offensiveness-based logs as a `.CSV` file. Logs can be analyzed for the types of content that are being identified so you can take other preventive measures, such as changing conversational questions.
2.  Configure Prompt Injection for AI agents.

    1.  In the AI Agent Studio, navigate to **Settings** &gt; **Prompt Injection** and select **Configure**.

        You’re directed to the AI Admin Hub page to configure the Prompt Injection.

        \[Omitted image "aia-prompt-injection-new.png"\] Alt text: Prompt Injection page in AI Agent Studio.

        **Note:** For more information about configuring the Prompt Injection, see [Configure prompt injection attack protection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/configure-prompt-injection-attack-protection.md).

        When you configure the Prompt Injection for an agentic workflow by using the required instructions, the system is designed to detect harmful content and block the conversation.


