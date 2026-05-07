---
title: Configure security controls
description: Set up Now Assist Guardian guardrails and data privacy controls to protect your AI agent interactions before testing begins.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 2
breadcrumb: [Create and secure an AI agent in Now Assist, Agentic AI security and governance]
---

# Configure security controls

Set up Now Assist Guardian guardrails and data privacy controls to protect your AI agent interactions before testing begins.

Runtime security controls protect your users and your data during AI agent interactions. Configure these before testing so that your test runs generate meaningful Guardian log data and so that any issues are caught before you go live.

## Configure Now Assist Guardian

Now Assist Guardian monitors prompts sent to large language models and their responses. It operates independently of your ACL and user identity configuration from Phase 3 — it is a runtime layer, not an access layer.

Complete the following Guardian configuration steps:

1.  Review the Guardian overview to understand what it detects and how logging and blocking work. See .
2.  Configure your Guardrail service provider. See .
3.  Activate offensiveness protection to log and optionally block offensive content in AI-generated responses. See .
4.  Configure prompt injection attack protection to detect and optionally block prompt injection attempts. See .
5.  If your agent uses Virtual Agent, configure sensitive topic filters to redirect users when subject matter is detected that should be handled by a human agent or HR case. See .
6.  Enable Guardian specifically for AI agents to protect your agentic workflows from harmful content in human-agent messages. See [Enable Now Assist Guardian for AI agents](https://www.servicenow.com/docs/access?context=enable-aia-na-guardian&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Configure Guardian to log before enabling blocking. Reviewing logs from your test runs will help you understand what your agent's interactions look like before deciding whether to block content.

## Configure data privacy controls

Before your agent goes into testing, verify that personally identifiable information \(PII\) is handled appropriately. Complete the following steps if you have not already done so:

1.  Assign a data steward if one is not already assigned. The data steward is responsible for data sharing decisions for Now Assist on your instance. See [Assign the data steward role](https://www.servicenow.com/docs/access?context=assign-data-steward-role&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
2.  Configure privacy policies to control how PII is de-identified before it reaches the large language model. See [Configuring Data Privacy for Now Assist](configure-now-assist-data-privacy.md).
3.  Review your data sharing preferences and opt out if your organization policy requires it. See [Opt out of data sharing for Now Assist](https://www.servicenow.com/docs/access?context=opt-out-of-data-sharing-for-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Next step

When Guardian is configured and data privacy controls are in place, proceed to [Test and validate](naai-tutorial-test-validate.md).

**Parent Topic:**[Create and secure an AI agent in Now Assist](naai-tutorial-overview.md)

