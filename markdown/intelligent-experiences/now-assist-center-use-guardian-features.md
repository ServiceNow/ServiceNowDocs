---
title: Use AI Guardian features in AI Admin Center
description: Use AI Guardian features in the AI Admin Center workspace to detect offensive content, prompt injection attacks, and sensitive topics in generative AI interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-center-use-guardian-features.html
release: zurich
topic_type: task
last_updated: "2026-07-30"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Using other AI applications from AI Admin Center, Use, AI Admin Center, Enable AI experiences]
---

# Use AI Guardian features in AI Admin Center

Use AI Guardian features in the AI Admin Center workspace to detect offensive content, prompt injection attacks, and sensitive topics in generative AI interactions.

## Before you begin

The following applications must be installed before performing this task:

-   AI Admin Center

    For more information, see [Confirm installation of AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-install.md).

-   AI Admin Hub

    For more information, see [Install and configure essential AI plugins using AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/install-configure-essential-now-assist-plugins.md).


Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to use AI Guardian capabilities from AI Admin Center.

AI Guardian provides safety and governance controls for AI-generated content. It monitors AI interactions for potentially harmful, offensive, or policy-violating content.

In AI Admin Center, the integration of AI Guardian includes multi-tabbing support for working with safety and governance controls without leaving the application context.

For more information on AI Guardian, see [AI Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-guardian.md).

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** or **Workspaces** &gt; **AI Admin Center**.

2.  Select **Admin** \(\[Omitted image "icon-now-assist-center-nav-admin.png"\] Alt text: Admin icon. \) in the side navigation bar.

    The Admin tab opens showing AI Admin Hub options.

3.  Select one of the options under **AI Guardian** to configure.

    AI Guardian provides three guardrails. Each guardrail has a different scope.

<table id="choicetable_bs2_qzh_w3c"><thead><tr><th align="left" id="d220409e231">

Guardrail

</th><th align="left" id="d220409e234">

Description

</th></tr></thead><tbody><tr><td id="d220409e240">

**Prompt injection detection**

</td><td>

This guardrail attempts to override LLM instructions or expose restricted information. It applies to all generative AI applications and features.

 Select **Prompt injection** to open the Prompt injection tab.

 For more information on how to configure this guardrail, see [Configure prompt injection attack protection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configure-prompt-injection-attack-protection.md).

</td></tr><tr><td id="d220409e268">

**Offensiveness detection**

</td><td>

This guardrail detects offensive or harmful content in AI inputs and outputs. It applies to specific generative AI skills and workflows.

 Select **Offensiveness** to open the Offensiveness tab.

 For more information on how to configure this guardrail, see [Activate offensiveness protection for generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/activate-offensiveness-protection-for-generative-ai.md).

</td></tr><tr><td id="d220409e299">

**Sensitive topic filters**

</td><td>

This guardrail filters subjects not suited for AI responses, such as workplace safety or employee compensation. It applies to Virtual Agent conversational skills only \(available for HR Service Delivery and Customer Service Management\).

 Select **Sensitive Filters** to open the Filters tab.

 For more information on how to configure this guardrail, see [Configure sensitive topic filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/configure-sensitive-topic-filters.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Using other AI applications and features from AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-using-other-applications.md)

