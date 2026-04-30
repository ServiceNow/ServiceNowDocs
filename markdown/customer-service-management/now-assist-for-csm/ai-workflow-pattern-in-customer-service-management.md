---
title: AI Workflow pattern in Customer Service Management
description: In-product AI workflow patterns shows agentic workflow status, presence indicators, and AI-generated insights directly on Customer Service Management \(CSM\) record and interaction pages.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-02-06"
reading_time_minutes: 4
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# AI Workflow pattern in Customer Service Management

In-product AI workflow patterns shows agentic workflow status, presence indicators, and AI-generated insights directly on Customer Service Management \(CSM\) record and interaction pages.

The AI workflow feature is built directly into Customer Service Management \(CSM\). This feature is available on Core UI and Configurable Workspace of the case records. You can view AI activity, respond to workflow prompts, and track progress — all from the case record page. AI indicators, workflow presence, and a dedicated AI Workflow tab are available on case records and interaction pages in the contextual side panel. The feature also introduces a **Triage Cases** button that initiates agentic workflows directly from the case form.

## AI Workflow integration

AI workflow supports human‑initiated and autonomous agent‑initiated workflows. When triggered, the system displays a presence indicator showing that Now Assist is actively analyzing the record. The AI Workflow tab gives you a unified view of a workflow’s status, findings, required inputs, and history, making it easy to work with AI‑generated insights and automation. When a workflow needs input from the user, an alert appears with a **Review** button. Selecting this button takes you directly to the **AI Workflow** tab, opens the **Interactive View**, and automatically focuses on the specific plan that requires your input.

## AI Workflow UI Components

The following table describes the key user interface components that support in‑product AI workflow patterns.

|UI component|Description|
|------------|-----------|
|**Triage Cases** button|Trigger agentic workflows directly from case records using the Triage Cases button, eliminating the need to navigate to Now Assist panel. When you select the Triage Cases button on a case record, the system automatically initiates an agentic workflow for the case and email interaction record. You can monitor workflow progress by accessing the **AI Workflow** tab, where the same workflow appears with complete visibility. From this tab, you can drill into the workflow details to review individual steps or provide any required input to advance the workflow.|
|AI presence indicator|View the visual indicator showing that Now Assist is actively running an agentic workflow on the current record. Selecting the indicator displays AI activity status and shows up when **Triage Cases** button is selected.|
|**AI Workflow** tab|A dedicated tab that displays in‑progress, completed, input‑required, ready for review, failed, and cancelled workflows. You can view workflow details, AI‑generated findings, and workflow history.|
|Workflow detail experience|Provides a step‑by‑step view of workflow execution. You can see each step in the workflow as it happens. You can check the workflow’s status at any time. You can easily tell when the system needs information from you. You can also read the main findings and insights the AI has prepared. When you’re ready, you can choose to continue to the next step, skip extra details, or let the workflow finish on its own. For example, if a workflow requires input like "Do you want deeper insights?", responding with No moves the workflow directly to complete state.|
|AI record indicators|Alerts and system‑generated indicators showing AI‑assisted record creation, findings, and transparency details directly on the case record.|
|Input request panel|Displays workflow ‑requested inputs such as text, Boolean, single‑select, multi‑select, or drop down values that enable you to influence workflow progression.|
|Workflow history|Shows completed actions, AI findings, supervision information, and any user responses supplied during workflow execution.|

## Feature behavior

The AI workflow tab provides a single view of all AI workflows related to a record. It shows workflow status, step‑by‑step details, and any required inputs, which you can enter directly in the tab. Workflows can also be canceled when needed.

By default, this feature is turned off in the base system. To enable it, admin must set the system property com.glide.agentic\_processes\_view.enabled. Once the system property is enabled by an admin, the **Triage Cases** button \(UI Action\) and the **AI Workflow** tab is set to visible. If you prefer to hide this option, you can disable it in AI Agent Studio. To disable the **Triage Cases** button:

1.  Open AI Agent Studio.
2.  Select the **Triage Cases** agentic workflow.
3.  Navigate to **Select Channel and Status**.
4.  Scroll down to the **UI Actions** section.
5.  Toggle the **Display** option to turn the button on or off.

This allows admin to control whether the **Triage Cases** button appears in the agent interface. All workflows must be initiated by a human agent.

![Add triggers page showing Triage Cases UI actions with display toggles and configuration options.](../image/ai-workflow-triage-cases.png "Triage Cases guided flow")

The **AI Workflow** tab is visible on following pages in CSM Configurable Workspace:

-   CSM default record page
-   CSM frontline case page
-   CSM interaction record page
-   Email interaction record page
-   Voice interaction record page
-   Centered chat record page

The **AI Workflow** tab is visible on following pages in Core UI:

-   Case view
-   Email interaction view

**Note:** The in-product trigger **Triage Cases** button is only enabled for case records and email type interactions.

