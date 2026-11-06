---
title: Configure allowed AI model providers
description: Restrict your AI systems to the model providers your organization approves, choose where their requests are processed, and decide what happens to AI systems the approved providers don't support.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/aict-configure-allowed-providers.html
release: australia
topic_type: task
last_updated: "2026-11-02"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring AI model providers, Configuring ServiceNow AI settings, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Configure allowed AI model providers

Restrict your AI systems to the model providers your organization approves, choose where their requests are processed, and decide what happens to AI systems the approved providers don't support.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward or admin

## About this task

Provider settings apply to every AI system on your instance. Preview the impact of your changes before you save, so you know which AI systems lose support and which run on fallback providers. For how provider groups, data routing, spillover, and fallback work, see [Configuring AI model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-ai-model-providers.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **ServiceNow AI**.

2.  Select the **AI model providers** tab.

3.  Review the **Impact summary** panel to see how your current selections affect your AI systems.

    To see the AI systems in a category, select the category. The **Impact summary** page lists each AI system's type, activation status, default provider, support status, and support by each provider.

4.  Select **Edit**.

5.  In the **Data routing** section, select **Regional** or **Global**.

    Only the routing options available for your instance's region appear.

6.  In the **AI model providers supported by ServiceNow** section, select the providers to allow.

    You must allow at least one provider in this section.

7.  In the **AI model providers configured by your organization** section, select the third-party providers to allow.

8.  In the **Is spillover activated?** section, set the toggle.

    This section appears only on instances in the APJ region that use regional routing with Azure OpenAI allowed. Turn it on to let Azure OpenAI process data outside your region when regional capacity is limited.

9.  In the **Is fallback activated?** section, set the toggle.

    With fallback on, active AI systems that your allowed providers don't support stay active on the provider last configured for them, and they're reported as non-compliant. With fallback off, saving doesn't deactivate those AI systems. The impact summary lists the active ones as needing deactivation, so you can deactivate them yourself.

10. Select **Preview impact**.

    The preview lists your selections and the resulting impact summary. To see the AI systems in a category, select it. Select **Close** to return to your edits.

11. Select **Save**.

    If you selected **Global** routing on an instance in the APJ region, the **Data routing confirmation** dialog box opens first. Review the change to your data processing location, and then select **Agree and proceed**.

12. In the **Save changes?** dialog box, review your selections and their impact, and then select **Save**.


## Result

The **AI model providers** tab shows your allowed providers, data routing, and fallback setting, and the **Impact summary** panel reflects your changes.

**Parent Topic:**[Configuring AI model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-ai-model-providers.md)

