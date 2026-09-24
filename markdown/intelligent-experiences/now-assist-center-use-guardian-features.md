---
title: Use AI Guardian features in AI Admin Center
description: Use AI Guardian features in the AI Admin Center workspace to detect offensive content, prompt injection attacks, and sensitive topics in generative AI interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-center-use-guardian-features.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Using other AI applications from AI Admin Center, Setting up AI capabilities and configurations, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Use AI Guardian features in AI Admin Center

Use AI Guardian features in the AI Admin Center workspace to detect offensive content, prompt injection attacks, and sensitive topics in generative AI interactions.

## Before you begin

The following applications must be installed before performing this task:

-   AI Admin Center

    For more information, see [Confirm installation of AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-install.md).

-   AI Admin Hub

    For more information, see [Install and configure essential AI plugins using AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-configure-essential-now-assist-plugins.md).


Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to use AI Guardian capabilities from AI Admin Center.

AI Guardian provides safety and governance controls for AI-generated content. It monitors AI interactions for potentially harmful, offensive, or policy-violating content.

In AI Admin Center, the integration of AI Guardian includes multi-tabbing support for working with safety and governance controls without leaving the application context.

For more information on AI Guardian, see .

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** or **Workspaces** &gt; **AI Admin Center**.

2.  Select **Admin** \(\[Omitted image "icon-now-assist-center-nav-admin.png"\] Alt text: Admin icon. \) in the side navigation bar.

    The Admin tab opens showing AI Admin Hub options.

3.  Select one of the options under **AI Guardian** to configure.

    AI Guardian provides three guardrails. Each guardrail has a different scope.

<table id="choicetable_bs2_qzh_w3c"><thead><tr><th align="left" id="d278769e223">

Guardrail

</th><th align="left" id="d278769e226">

Description

</th></tr></thead><tbody><tr><td id="d278769e232">

**Prompt injection detection**

</td><td>

This guardrail attempts to override LLM instructions or expose restricted information. It applies to all generative AI applications and features.

 Select **Prompt injection** to open the Prompt injection tab.

 For more information on how to configure this guardrail, see .

</td></tr><tr><td id="d278769e256">

**Offensiveness detection**

</td><td>

This guardrail detects offensive or harmful content in AI inputs and outputs. It applies to specific generative AI skills and workflows.

 Select **Offensiveness** to open the Offensiveness tab.

 For more information on how to configure this guardrail, see .

</td></tr><tr><td id="d278769e280">

**Sensitive topic filters**

</td><td>

This guardrail filters subjects not suited for AI responses, such as workplace safety or employee compensation. It applies to Virtual Agent conversational skills only \(available for HR Service Delivery and Customer Service Management\).

 Select **Sensitive Filters** to open the Filters tab.

 For more information on how to configure this guardrail, see .

</td></tr></tbody>
</table>
