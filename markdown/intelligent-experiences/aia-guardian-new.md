---
title: Enable Now Assist Guardian in AI Agent Studio
description: Identify and block offensive messages that are sent by human agents automatically by enabling AI Guardian in AI agents. With this capability, you can help reduce your agentic workflow or test from being exposed to harmful content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aia-guardian-new.html
release: australia
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [AI Agent Studio settings, Configure AI Agent Studio, AI Agent Studio, Enable AI experiences]
---

# Enable Now Assist Guardian in AI Agent Studio

Identify and block offensive messages that are sent by human agents automatically by enabling AI Guardian in AI agents. With this capability, you can help reduce your agentic workflow or test from being exposed to harmful content.

## Before you begin

Role required: admin

## About this task

The AI Guardian, which is a ServiceNow AI Platform capability in the Now Assist panel, is a set of guardrails that are designed to intercept and mitigate offensive, sensitive, or security-related issues that may arise during interactions with the Now Assist application.

For example, let's say that AI Guardian detects an offensive message in the execution plan of an agentic workflow. When you try to trigger the plan or test it, AI Guardian can step in to terminate the plan or test because it detected harmful content at the first step of the execution plan.

For more information about the different guardrails, see [Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-guardian.md).

## Procedure

1.  Configure Offensiveness for AI agents.

    1.  Navigate to **AI Agent Studio** &gt; **Settings****Settings**.

    2.  In the AI Guardian section, turn on the **Offensiveness detection** toggle to monitor and block offensive content in AI responses.

2.  Configure Prompt Injection for AI agents.

    1.  Navigate to **AI Agent Studio** &gt; **Settings****Settings**.

    2.  Select **Configure** against **Prompt Injection protection**.

        You’re directed to the AI Admin Hub on your instance to configure the Prompt Injection.

        **Note:** For more information about configuring the Prompt Injection, see [Configure prompt injection attack protection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/configure-prompt-injection-attack-protection.md).

        When you configure the Prompt Injection for an agentic workflow by using the required instructions, the system is designed to detect the harmful content and block the conversation.


