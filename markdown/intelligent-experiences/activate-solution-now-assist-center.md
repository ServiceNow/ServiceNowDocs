---
title: View and activate actionable use cases in AI Admin Center \(Next Experience UI\)
description: View the top actions you can take right away to adopt AI capabilities on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/activate-solution-now-assist-center.html
release: brazil
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Activating actionable use cases, Setting up AI capabilities and configurations, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# View and activate actionable use cases in AI Admin Center\(Next Experience UI\)

View the top actions you can take right away to adopt AI capabilities on your instance.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

ServiceNow Otto panel must be enabled to activate the use cases. Actionable use cases work with the ServiceNow Otto panel to guide you through the setup in a chat conversation. For more information, see [Enable the ServiceNow Otto panel \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-enable-now-assist-panel.md).

Required plugins must be installed. For more information, see [Install and configure essential AI plugins using AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-configure-essential-now-assist-plugins.md).

**Note:** If a card displays a Model provider not approved warning, the model provider for that skill has not been approved in AI Guardian. Resolve this issue before attempting setup for the use case.

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to activate an actionable use case.

The actionable use cases section on the home page displays solution cards tailored to your instance. Each card represents a base-system AI solution you can activate with guided assistance from the ServiceNow Otto panel. The system determines which cards to display based on your license entitlements, installed products, instance version compatibility, and current AI enablement state.

If there are no actionable use cases, the section doesn't appear.

**Note:** This topic describes the AI Admin Center feature based on the Next Experience UI. If you're using the Lux user experience for AI Admin Center, see the Lux UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **AI Admin Center \(Legacy\)**.

    The AI Admin Center opens to the home page.

2.  Review the actionable use case cards displayed in the first section of the home page.

    Each card shows the use case name and a brief description of the AI solution.

    \[Omitted image "now-assist-center-home-adoption-tasks-2.png"\] Alt text: Actionable use cases in Now Assist Center.

3.  Select **Activate** on the card to begin.

    A conversation will open in the ServiceNow Otto panel.

    In the ServiceNow Otto panel, you can use natural language to have your AI companion implement the use case.

    **Note:** To remove a card permanently without activating it, select **Dismiss** on the card.

    **Warning:** Dismissed cards don't reappear in future sessions.

4.  In the ServiceNow Otto panel, review the information provided about the solution.

5.  When the panel asks you to confirm, respond to proceed with the activation.

6.  Follow any additional prompts in the panel to complete the setup.


## Result

The AI solution is activated. A confirmation message appears at the top of the workspace.

After it is activated, the card disappears and the new solution appears under the Recently activated AI section of the home page.

## What to do next

To monitor the performance of the activated solution, review the Recently activated AI section on the home page. For more information, see [Monitor your recently activated AI solution in AI Admin Center \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/monitor-now-assist-performance-now-assist-center.md).

**Parent Topic:**[Activating actionable use cases from AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-actionable-use-cases.md)

**Related topics**  


[Install and configure essential AI plugins using AI Admin Center]()

[View and activate your top actions in AI Admin Center \(Lux UI\)]()

