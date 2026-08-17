---
title: Configure ServiceNow AI settings
description: Control how AI features operate on your instance by configuring data sharing preferences, asset approval requirements, and allowed AI model providers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-configure-servicenow-ai-settings.html
release: zurich
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, AI Control Tower, Enable AI experiences]
---

# Configure ServiceNow AI settings

Control how AI features operate on your instance by configuring data sharing preferences, asset approval requirements, and allowed AI model providers.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

ServiceNow AI settings apply across your instance and affect all Now Assist features, not just AI Control Tower. Review each setting with your organization's data governance and AI governance policies before making changes.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **ServiceNow AI**.

2.  On the **Data controls** tab, review and adjust your data sharing and overflow processing preferences.

    1.  To stop sharing instance data with ServiceNow for AI model improvement, select **Opt out** on the **Data Sharing** card.

        Data sharing is active by default. When active, ServiceNow uses anonymized instance data to improve AI model accuracy. Opting out does not affect your instance's access to AI features. For more information, see the FAQs and opt-out documentation linked on the card.

    2.  To prevent Now Assist traffic from bursting to Microsoft Azure datacenters during high-traffic periods, select **Opt in** on the **Data overflow processing** card to keep all traffic within ServiceNow datacenters.

        Data overflow processing is inactive by default, meaning bursting to Azure is allowed. Opting in keeps all Now Assist traffic within ServiceNow datacenters but may result in processing delays or capacity errors during high-traffic periods.

3.  On the **Builder controls** tab, configure approval requirements and automated playbook behavior for AI assets.

    1.  In the **AI steward approval for AI assets** section, activate approval requirements for each asset type that should require AI steward sign-off before deployment.

        You can activate approval independently for AI systems, MCP servers, and AI models. When active for an asset type, an AI steward must approve the asset before it can be deployed. Select **Actions** on the asset type row to activate or deactivate the requirement.

    2.  In the **Automated requests** section, verify that **Automatically trigger playbooks** is set to **Active** if you want approval playbooks to run automatically when a new AI asset is added.

        When inactive, asset managers can still initiate approval playbooks manually from the asset record. Activate or deactivate using **Actions** on the row.

4.  On the **AI model providers** tab, configure which AI model providers are allowed on your instance and set fallback behavior.

    1.  Review the **Impact summary** panel to see how your current provider selection affects the AI systems on your instance.

        The Impact summary panel shows the total number of AI systems on your instance, how many are supported by your allowed providers, and how many are running on fallback providers instead. Select an area in the chart or a count to open the full Impact summary page, where you can review the list of affected AI systems for that category, including each system's type, activation status, default provider, and per-provider support status.

    2.  Select **Edit** to open the provider configuration.

    3.  In the **AI model providers supported by ServiceNow** section, select the providers you want to allow.

        Supported providers include Now LLM Service, AWS Claude, Azure OpenAI, and Google Gemini. These providers are supported by ServiceNow or ServiceNow OEM partners. The data routing setting \(Regional or Global\) applies to this provider group.

        **Note:** Some ServiceNow skills and agents use third-party provider APIs that may route data to datacenters outside your region. For a list of affected APIs and skills, see the [Third-party APIs used in Advanced AI &amp; Data Products \[KB2596322\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2596322) article.

    4.  In the **AI model providers configured by your organization** section, select any third-party providers your organization has configured with its own API keys.

        Third-party providers include Custom LLM Provider, OpenAI, Perplexity, IBM Watson, and others. If your organization uses a provider that is not listed, an admin can add it using provider keys from AI Skill Kit.

    5.  In the **Is fallback activated?** section, decide whether AI systems whose providers aren't in the allowed list should remain active using their previously configured provider.

    6.  Select **Save**.


**Parent Topic:**[Configuring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring.md)

