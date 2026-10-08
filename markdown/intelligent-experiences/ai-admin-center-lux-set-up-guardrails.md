---
title: Set up AI guardrails in AI Admin Center \(Lux UI\)
description: Use AI guardrails to detect offensive content, prompt injection attacks, and sensitive topics in generative AI interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-lux-set-up-guardrails.html
release: australia
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Using other AI applications from AI Admin Center, Setting up AI capabilities and configurations, AI Admin Center, Enable AI experiences]
---

# Set up AI guardrails in AI Admin Center \(Lux UI\)

Use AI guardrails to detect offensive content, prompt injection attacks, and sensitive topics in generative AI interactions.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to set up AI guardrails in AI Admin Center.

AI guardrails provide safety and governance controls for AI-generated content. They monitor AI interactions for potentially harmful, offensive, or policy-violating content.

For more information on AI Guardian, see .

**Note:** This topic describes the AI Admin Center feature based on the Lux user interface \(UI\). If you're using the Next Experience UI for AI Admin Center, see the Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **Settings** \(\[Omitted image "icon-aiac-lux-nav-settings.png"\] Alt text: Settings icon.\) in the side navigation panel.

    The Settings page opens.

3.  Select one of the options under **AI Guardian** to configure.

    AI Guardian provides three guardrails. Each guardrail has a different scope.

<table id="choicetable_lux_guard"><thead><tr><th align="left" id="d178726e235">

Guardrail

</th><th align="left" id="d178726e238">

Description

</th></tr></thead><tbody><tr><td id="d178726e244">

**Prompt injection detection**

</td><td>

This guardrail detects attempts to override LLM instructions or expose restricted information. It applies to all generative AI applications and features.

 Select **Prompt injection** to open the Prompt injection page.

 For more information on how to configure this guardrail, see .

</td></tr><tr><td id="d178726e268">

**Offensiveness detection**

</td><td>

This guardrail detects offensive or harmful content in AI inputs and outputs. It applies to specific generative AI skills and workflows.

 Select **Offensiveness** to open the Offensiveness page.

 For more information on how to configure this guardrail, see .

</td></tr><tr><td id="d178726e292">

**Sensitive topic filters**

</td><td>

This guardrail filters subjects not suited for AI responses, such as workplace safety or employee compensation. It applies to Virtual Agent conversational skills only \(available for HR Service Delivery and Customer Service Management\).

 Select **Sensitive Filters** to open the Filters page.

 For more information on how to configure this guardrail, see .

</td></tr></tbody>
</table>
