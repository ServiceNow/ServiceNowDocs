---
title: Activate an actionable use case in AI Admin Center
description: Activate an AI solution from an actionable use case card on the AI Admin Center home page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/activate-solution-now-assist-center.html
release: zurich
topic_type: task
last_updated: "2026-07-30"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Activating actionable use cases, Use, AI Admin Center, Enable AI experiences]
---

# Activate an actionable use case in AI Admin Center

Activate an AI solution from an actionable use case card on the AI Admin Center home page.

## Before you begin

ServiceNow Otto panel must be enabled to activate the use cases. Actionable use cases work with the ServiceNow Otto panel to guide you through the setup in a chat conversation. For more information, see [Enable the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-enable-now-assist-panel.md).

Required plugins must be installed. For more information, see [Install and configure essential AI plugins using AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/install-configure-essential-now-assist-plugins.md).

**Note:** If a card displays a Model provider not approved warning, the model provider for that skill has not been approved in AI Guardian. Resolve this issue before attempting setup for the use case.

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to activate an actionable use case.

The actionable use cases section on the home page displays solution cards tailored to your instance. Each card represents a base-system AI solution you can activate with guided assistance from the ServiceNow Otto panel. The system determines which cards to display based on your license entitlements, installed products, instance version compatibility, and current AI enablement state.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** or **Workspaces** &gt; **AI Admin Center**.

2.  Review the actionable use case cards displayed in the first section of the home page.

    Each card shows the use case name and a brief description of the AI solution.

    \[Omitted image "now-assist-center-home-adoption-tasks-2.png"\] Alt text: Actionable use cases in Now Assist Center.

3.  Select **Activate** on the card to begin.

    A conversation will open in the ServiceNow Otto panel.

    In the ServiceNow Otto panel, you can use natural language to have your AI companion implement the use case.

    **Note:** To remove a card permanently without activating it, select **Dismiss** on the card. Dismissed cards don't reappear in future sessions.

4.  In the ServiceNow Otto panel, review the information provided about the solution.

5.  When the panel asks you to confirm, respond to proceed with the activation.

6.  Follow any additional prompts in the panel to complete the setup.


## Result

The AI solution is activated. A confirmation message appears at the top of the workspace.

After it is activated, the card disappears and the new solution appears under the Recently activated AI section of the home page.

## What to do next

To monitor the performance of the activated solution, review the Recently activated AI section on the home page. For more information, see [Monitor your recently activated AI solution in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/monitor-now-assist-performance-now-assist-center.md).

**Parent Topic:**[Activating actionable use cases from AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-actionable-use-cases.md)

**Related topics**  


[Install and configure essential AI plugins using AI Admin Center]()

