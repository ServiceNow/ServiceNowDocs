---
title: Globalization Terminology Agent
description: Generate a glossary of terms based on your English-language Knowledge Base articles. Use the glossary of terms to enhance language governance, quality, and consistency across the platform. Available from version 4.0 of Localization Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-workspace/lw-terminology-agent.html
release: brazil
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Language Asset Management, Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Globalization Terminology Agent

Generate a glossary of terms based on your English-language Knowledge Base articles. Use the glossary of terms to enhance language governance, quality, and consistency across the platform. Available from version 4.0 of Localization Workspace.

## Overview of the Globalization Terminology Agent

The Globalization Terminology Agent uses the generate glossary skill to analyze your Knowledge Base content and create a suggested English glossary. The generate glossary skill identifies and extracts key terms, generates definitions for the terms, and enables you to edit or remove terms before approval.

After approval your glossary is published to the list of glossaries in the Language Asset Management section of Localization Workspace.

The generate glossary skill is located in the [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platform-now-assist-landing.md). It can also be accessed from [AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit-landing.md).

## Benefits of the Globalization Terminology Agent

The Globalization Terminology Agent offers these benefits.

-   Save time and manual effort during glossary creation.
-   Review, edit, and approve the terms and their definitions before publishing.
-   Update the glossary in Language Asset Management after creation, including adding translations into non-English languages.
-   Export the glossary to share with stakeholders.

## Prerequisites and conditions

The following prerequisites and conditions apply.

-   Only KB articles labeled as English in the Knowledge Base are included in the search. For information see [Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/knowledge-center.md).
-   Accessing and working with glossaries in Language Asset Management requires the Terminology Manager role \(sn\_lw.terminology\_manager\) with the Localization user role \(sn\_lw.user\).
-   The generate glossary skill must be activated in [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platform-now-assist-landing.md). After the skill is activated, the **Create Glossary** button becomes visible in Language Asset Management.

## Other considerations

The maximum word count for scanning defaults to 25,000. The count of words does not map exactly to the number of tokens used. The wizard provides the option to limit retrieved articles by date range, minimum view count, and whether authored by the current user.

## Activating the generate glossary skill

\[Omitted image "lw-terminology-agent-aiadminhub.png"\] Alt text: The navigation to the AI Admin Hub. The category Other is highlighted because the Generate Glossary skill is found there.

The generate glossary skill is included from version 4.0 of Localization Workspace, but it must be activated. The general procedure for activation of this skill is as follows.

1.  Navigate to AI Admin Hub &gt; Skills.
2.  In the navigation panel of the AI Skills tab, select the category **Other**.
3.  Select the **Available** tab and locate the **Generate Glossary** skill name.
4.  Select **Activate skill** to turn on this skill.

For further information see [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platform-now-assist-landing.md) and [Activate an AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-a-now-assist-skill.md). Some configurations can be made to the skill in [AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit-landing.md).

-   **[Create a glossary using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-create-glossary-using-ai.md)**  
In Language Asset Management, generate a glossary containing terms extracted from Knowledge Base articles. The Globalization Terminology Agent uses an AI skill to scan your article content and create a list of suggested terms and definitions.

**Parent Topic:**[Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-language-asset-management.md)

