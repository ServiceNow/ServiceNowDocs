---
title: Configuring AI model providers
description: Limit your AI systems to the model providers your organization approves, control where AI requests are processed, and see how each change affects the AI systems on your instance before you save it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-configuring-ai-model-providers.html
release: australia
topic_type: concept
last_updated: "2026-11-02"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring ServiceNow AI settings, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configuring AI model providers

Limit your AI systems to the model providers your organization approves, control where AI requests are processed, and see how each change affects the AI systems on your instance before you save it.

## Provider groups

AI model providers fall into two groups, and you choose the allowed providers in each one.

-   **Providers supported by ServiceNow**

    Providers that ServiceNow or its OEM partners support, such as Now LLM Service, AWS Claude, Azure OpenAI, and Google Gemini. At least one provider in this group must be allowed. The data routing choice applies to this group. On instances entitled to it, the long-term stable \(LTS\) version of Now LLM Service also appears in this group.

-   **Providers configured by your organization**

    Third-party providers that your organization connects with its own provider keys, such as Custom LLM Provider, OpenAI, Perplexity, and IBM Watson. An Otto admin adds new providers to this group from AI Skill Kit.


Some ServiceNow skills and agents use third-party provider APIs that can route data to datacenters outside your region. For the list of affected APIs and the skills and agents that use them, see the [Third-party APIs used in Advanced AI &amp; Data Products \[KB2596322\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2596322) article in the Now Support Knowledge Base.

## Data routing

Data routing determines which datacenters process large language model \(LLM\) and small language model \(SLM\) requests for the providers supported by ServiceNow.

-   **Regional**

    Requests are routed to the most suitable datacenter in your region. Some governments require regional routing.

-   **Global**

    Requests are routed to the most suitable datacenter anywhere, with no geographic limitation. Your data processing location changes to a global datacenter, while your instance stays in its original location.


The routing options available depend on your instance's region, so some instances offer regional routing only.

## Spillover

Regional deployments of Azure OpenAI have limited capacity, which can rate-limit requests and slow performance. Spillover lets Azure OpenAI process data in a datacenter outside your region when it needs to. The option is offered only on instances in the APJ region that use regional routing with Azure OpenAI allowed. Selecting global routing turns spillover on.

## Fallback

When you narrow the allowed providers, some active AI systems might depend on a provider that's no longer allowed. Fallback keeps those AI systems active by using the provider you last configured for them, or the one originally configured. Fallback is on by default.

AI systems that run on a fallback provider are non-compliant, because the fallback provider isn't one of your allowed providers. Without fallback, saving your changes doesn't deactivate the unsupported AI systems for you. The impact summary flags the active ones as needing deactivation, and you deactivate them yourself.

## Impact summary

The impact summary shows how your provider choices affect the AI systems on your instance, which include skills, agentic workflows, and AI agents. It counts the total AI systems and the AI systems supported by your allowed providers. The remaining categories depend on whether fallback is on:

-   With fallback on, it counts the AI systems running on fallback providers.
-   With fallback off, it counts the active AI systems that need to be deactivated and the inactive AI systems that can't be activated, because no allowed provider supports them.

You can preview the impact of your changes before you save them. From any category, you can open a detailed list of the AI systems in it, showing each system's type, activation status, default provider, support status, and whether each provider supports it.

## Model Preview Program

The Model Preview Program gives your organization early access to AI models that aren't generally available yet, such as models labeled preview, beta, or experimental. You can explore new capabilities, test use cases, and prepare for adoption before general availability.

The program is a global setting, so data routing preferences don't affect it. It's offered only on eligible instances. Eligibility is set at the instance level, based on the instance's geographic and regulatory classification at provisioning time, and currently covers US commercial instances only. On-premises, in-country, and regulated-market instances aren't eligible.

After you accept the program terms and enroll, eligible preview models become available to AI applications such as AI Skill Kit and AI Agent Studio. Your allowed providers and fallback setting still apply to preview models. Enrollment can't be turned off from the instance. For the procedure, see [Enroll in the Model Preview Program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configure-model-preview-program.md).

-   **[Configure allowed AI model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configure-allowed-providers.md)**  
Restrict your AI systems to the model providers your organization approves, choose where their requests are processed, and decide what happens to AI systems the approved providers don't support.
-   **[Enroll in the Model Preview Program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configure-model-preview-program.md)**  
Give your organization early access to AI models before they're generally available by accepting the Model Preview Program terms on an eligible instance.

**Parent Topic:**[Configuring ServiceNow AI settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-servicenow-ai-settings.md)

