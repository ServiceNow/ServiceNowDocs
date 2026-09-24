---
title: AI Guardian
description: AI Guardian provides the runtime protection layer for your generative AI deployments, evaluating requests and responses in real time to detect offensive content, prompt injection attacks, and sensitive topics that aren't suited for an AI response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-now-assist-guardian.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Now Assist Guardian, AI governance, generative AI safety, guardrails, prompt injection, offensive content detection, sensitive topic filters, runtime AI protection]
breadcrumb: [Establishing AI governance, Enable AI Experiences]
---

# AI Guardian

AI Guardian provides the runtime protection layer for your generative AI deployments, evaluating requests and responses in real time to detect offensive content, prompt injection attacks, and sensitive topics that aren't suited for an AI response.

## Why AI Guardian matters

Generative AI behavior is probabilistic. The same input sent to a large language model \(LLM\) can produce different outputs from one request to the next, and even well-tested skills can return content that's harmful, off-topic, or manipulated by a bad actor. Lifecycle governance can establish policies and controls before a generative AI skill goes live, but it can't catch what happens in the moment a user submits a prompt.

AI Guardian closes that gap by evaluating every request and response in real time. Offensive content is detected before it reaches a user. Prompt injection attempts that try to override LLM instructions are flagged or blocked. Conversations that drift into topics not suited for AI responses are redirected to a fallback flow. Together, these protections give your governance team the runtime evidence and enforcement they need to deploy AI with confidence.

## How AI Guardian fits into AI governance

AI governance operates at two levels, and a complete program needs both. Lifecycle governance, supported by AI Control Tower and AI Risk and Compliance, evaluates AI assets before deployment and across their full life cycle: intake, impact assessment, risk classification, control attestation, and ongoing monitoring. Runtime governance, supported by AI Guardian, evaluates each individual AI interaction as it happens.

The two layers reinforce each other. Lifecycle reviews establish which AI systems are approved to operate and what controls must be in place. AI Guardian enforces parts of those controls at runtime and produces the logs that feed back into ongoing risk monitoring. When a guardrail surfaces a pattern of incidents, that signal can drive reassessment in AI Risk and Compliance without disrupting service.

## The three guardrails

AI Guardian provides three guardrails, each with a different scope of applicability.

-   **Offensiveness detection**

    Identifies toxic, defamatory, fraudulent, or otherwise harmful content in both the input sent to an LLM and the output returned. By default, detections are logged. You can configure the guardrail to block detected content and return a standard error message instead of the generated response. Offensiveness detection applies to specific generative AI skills and agentic workflows.

-   **Prompt injection detection**

    Identifies attempts to override LLM instructions or expose restricted information through techniques such as role playing, paraphrasing, repetition, or instructions to ignore previous prompts. Prompt injection protection applies across all generative AI applications and features on your instance, and you can configure it at the instance level or for individual skills. When both are set, the more protective setting applies.

-   **Sensitive topic filters**

    Identifies subjects not suited for an AI response, such as workplace safety, employee compensation, or personal well-being. When a filter triggers, the user is redirected to a Sensitivity Detection: Fallback Virtual Agent topic that can route them to a live agent or help them open a case. Sensitive topic filters apply to Virtual Agent conversational skills and are available with HR Service Delivery and Customer Service Management.


## Logging and blocking

Offensiveness and prompt injection detections are logged by default. Logs capture the request, the conversation context, and any user feedback, and are accessible from **AI Admin Hub** &gt; **Settings** &gt; **AI Guardian**. Reviewing logs over a representative period of time gives your team a baseline for how often issues occur in your environment before you enable blocking.

When blocking is enabled and a guardrail triggers, the user sees a standard error message and the generated content isn't returned. Personally identifiable information \(PII\) is anonymized from requests before they reach the LLM, and the type of data anonymized is configurable.

## Explore further

For details about configuring guardrails, exporting logs, and setting up a Guardrail Service Provider, see [AI Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-guardian.md).

