---
title: Activating actionable use cases from AI Admin Center
description: Actionable use cases are quick-start scenarios that help you rapidly adopt AI capabilities on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-center-actionable-use-cases.html
release: zurich
topic_type: concept
last_updated: "2026-07-30"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Use, AI Admin Center, Enable AI experiences]
---

# Activating actionable use cases from AI Admin Center

Actionable use cases are quick-start scenarios that help you rapidly adopt AI capabilities on your instance.

## Overview of actionable use cases

Actionable use cases are represented as cards in the first section of the home page. Each card shows a supported and ready-to-activate AI solution for your instance, such as activating an AI skill for ITSM or configuring a safety setting through AI Guardian.

Actionable use cases use generative AI to tailor the solution and guide setup. The system analyzes your instance profile, organizational context, license entitlements, installed products, and current AI enablement state to determine which use case cards to display and in which order. Only cards for products that you're entitled to use appear on the home page.

\[Omitted image "now-assist-center-home-adoption-tasks-2.png"\] Alt text: Actionable use cases on the AI Admin Center home page.

## Types of actionable use cases

The following are some examples of actionable use cases that may appear on your home page:

-   Let’s get you set up \(install essential AI plugins\)
-   Case summarization for CSM
-   Chat summarization for CSM
-   KB generation for CSM
-   Resolution notes generation for CSM
-   Chat summarization for ITSM
-   Incident summarization for ITSM
-   KB generation for ITSM
-   Resolution notes generation for ITSM

## How actionable use cases work

When you navigate to AI Admin Center, the home page displays the use cases most relevant to you. For each card:

-   Select **Activate** to start a guided setup conversation in the ServiceNow Otto panel. The panel describes the solution, confirms the current state, and asks you to confirm before making any change.

    **Important:** ServiceNow Otto panel must be enabled to activate the use cases. Actionable use cases work with the ServiceNow Otto panel to guide you through the setup in a chat conversation. For more information, see [Enable the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-enable-now-assist-panel.md).

-   Select **Dismiss** to permanently remove a card.

    **Warning:** Dismissed cards don't reappear in future sessions.


After you successfully activate a solution, the card disappears from the home page and a confirmation message appears at the top of the workspace. The activated solution appears in the Recently activated AI section of the home page, where you can monitor its performance.

-   **[Install and configure essential AI plugins using AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/install-configure-essential-now-assist-plugins.md)**  
Install the plugins required to enable AI solutions on your instance before activating use cases.
-   **[Activate an actionable use case in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/activate-solution-now-assist-center.md)**  
Activate an AI solution from an actionable use case card on the AI Admin Center home page.

**Parent Topic:**[Using AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/using-now-assist-center.md)

**Related topics**  


[Using the conversational experience in AI Admin Center]()

[Using AI readiness assessments in AI Admin Center]()

[Using AI Agent Advisor in AI Admin Center]()

[Using the asset inventory in AI Admin Center]()

[Using other AI applications and features from AI Admin Center]()

