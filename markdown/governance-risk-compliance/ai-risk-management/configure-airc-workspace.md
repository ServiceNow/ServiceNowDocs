---
title: Configure AI Risk and Compliance Workspace
description: Configure the AI Risk and Compliance Workspace using UI Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/configure-airc-workspace.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Configure AI Risk and Compliance Workspace

Configure the AI Risk and Compliance Workspace using UI Builder.

## Before you begin

Role required: admin, ui\_builder\_admin

## About this task

ServiceNow offers prebuilt Configurable Workspace experiences to target specific users. These prebuilt workspaces can be updated and modified in UI Builder instead of creating an experience from scratch. For a list of prebuilt workspaces ServiceNow offers, see [List of workspaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/list-of-workspaces.md). To update an existing Configurable Workspace experience, see [Open a Configurable Workspace experience in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/open-your-configurable-workspace-experience-in-ui-builder.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  To edit the configuration of the workspace, set the **Application scope** to **AI Risk and Compliance Management**.

3.  Select **Page collections**.

4.  Select **AI risk and compliance home page tabs**.

5.  In the **Pages and variants** section, select the page that you want to edit.

    The following pages are available in the AI Risk and Compliance page collection:

    -   **Risk &amp; compliance**: Displays regulatory risk classification charts, compliance posture by authority document and policy, and compliance scores for AI systems, models, and datasets.
    -   **Operations**: Displays AI systems by life cycle state and department, and assessment tracking panels for risk and AI assessments.
    -   **AI cases**: Displays AI case and inquiry status charts and lists. This page is scoped to the AI Case Management application.
    **Note:** Changes made in a page collection apply to all experiences that use that page collection.

6.  In the UI Builder editor, modify the page components as needed.

    Common modifications include updating component visibility, adjusting data resource filters on list or chart components, and editing section headings.

7.  Select **Save**.


## Result

Your changes reflect in the AI Risk and Compliance Workspace under the corresponding pages.

## What to do next

To create new workspace experiences or pages from scratch, see [Create a Configurable Workspace experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/create-configurable-workspace-experience-uib.md) and [Create a Configurable Workspace page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/create-configurable-workspace-page-uib.md). For full UI Builder documentation, see [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder-overview.md).

**Related topics**  


[Set up AI Risk and Compliance properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configure-airc-properties.md)

[https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configuring-ai-risk-and-compliance.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/configuring-ai-risk-and-compliance.md)

