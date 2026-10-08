---
title: Use AI Guardian features in AI Admin Center \(Next Experience UI\)
description: Use AI Guardian features in the AI Admin Center workspace to detect offensive content, prompt injection attacks, and sensitive topics in generative AI interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-center-use-guardian-features.html
release: australia
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Using other AI applications from AI Admin Center, Setting up AI capabilities and configurations, AI Admin Center, Enable AI experiences]
---

# Use AI Guardian features in AI Admin Center\(Next Experience UI\)

Use AI Guardian features in the AI Admin Center workspace to detect offensive content, prompt injection attacks, and sensitive topics in generative AI interactions.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

The following applications must be installed before performing this task:

-   AI Admin Center

    For more information, see [Confirm installation of AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-install.md).

-   AI Admin Hub

    For more information, see [Install and configure essential AI plugins using AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/install-configure-essential-now-assist-plugins.md).


Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to use AI Guardian capabilities from AI Admin Center.

AI Guardian provides safety and governance controls for AI-generated content. It monitors AI interactions for potentially harmful, offensive, or policy-violating content.

In AI Admin Center, the integration of AI Guardian includes multi-tabbing support for working with safety and governance controls without leaving the application context.

For more information on AI Guardian, see .

**Note:** This topic describes the AI Admin Center feature based on the Next Experience UI. If you're using the Lux user experience for AI Admin Center, see the Lux UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **AI Admin Center \(Legacy\)**.

2.  Select **Admin** \(\[Omitted image "icon-now-assist-center-nav-admin.png"\] Alt text: Admin icon. \) in the side navigation bar.

    The Admin tab opens showing AI Admin Hub options.

3.  Select one of the options under **AI Guardian** to configure.

    AI Guardian provides three guardrails. Each guardrail has a different scope.

<table id="choicetable_bs2_qzh_w3c"><thead><tr><th align="left" id="d357690e296">

Guardrail

</th><th align="left" id="d357690e299">

Description

</th></tr></thead><tbody><tr><td id="d357690e305">

**Prompt injection detection**

</td><td>

This guardrail attempts to override LLM instructions or expose restricted information. It applies to all generative AI applications and features.

 Select **Prompt injection** to open the Prompt injection tab.

 For more information on how to configure this guardrail, see [Configure prompt injection attack protection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/configure-prompt-injection-attack-protection.md).

</td></tr><tr><td id="d357690e330">

**Offensiveness detection**

</td><td>

This guardrail detects offensive or harmful content in AI inputs and outputs. It applies to specific generative AI skills and workflows.

 Select **Offensiveness** to open the Offensiveness tab.

 For more information on how to configure this guardrail, see [Activate offensiveness protection for generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/activate-offensiveness-protection-for-generative-ai.md).

</td></tr><tr><td id="d357690e355">

**Sensitive topic filters**

</td><td>

This guardrail filters subjects not suited for AI responses, such as workplace safety or employee compensation. It applies to Virtual Agent conversational skills only \(available for HR Service Delivery and Customer Service Management\).

 Select **Sensitive Filters** to open the Filters tab.

 For more information on how to configure this guardrail, see [Configure sensitive topic filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/configure-sensitive-topic-filters.md).

</td></tr></tbody>
</table>
