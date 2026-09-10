---
title: Generate LEAP knowledge base articles
description: Generate AI-enhanced knowledge base articles from automation opportunity resolution steps to share structured, publication-ready knowledge across your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/generate-aiops-leap-knowledge-base.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-08-10"
reading_time_minutes: 3
keywords: [LEAP knowledge base, KB article generation, resolution steps, automation opportunity, KB routing, knowledge base selection]
breadcrumb: [Use, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# Generate LEAP knowledge base articles

Generate AI-enhanced knowledge base articles from automation opportunity resolution steps to share structured, publication-ready knowledge across your organization.

## Before you begin

Resolution steps must exist for the automation opportunity before generating a knowledge base article.

Role required: LEAP admin

A default knowledge base must be configured in LEAP properties before LEAP AI agent creates knowledge base articles. See [LEAP settings fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-settings-fields.md).

Each knowledge base used in LEAP must have the correct Can Contribute permissions configured. See [Knowledge base permissions for LEAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/configure-knowledge-base-user-collections.md).

## About this task

LEAP uses AI to transform resolution steps into a complete, structured knowledge base article. The generated article includes these sections:

-   Summary
-   Symptoms — inferred from incident data and resolution context
-   Resolution steps — expanded with sub-steps and code or command formatting
-   Related resources
-   Metadata — including Article Number, Product, Category, Visibility, and Valid To date

The article is created in Draft state and routed through the standard knowledge base approval workflow before publication. Each generated article maintains a link to the originating automation opportunity and is suggested when similar incidents occur.

When the LEAP AI agent automatically creates an article, it is routed to the default knowledge base and category configured in LEAP properties. When you create an article manually using the **Actions** menu, a dialog opens where you can select the knowledge base and category before the article is created.

**Note:** AI-generated content may be inaccurate. Review the generated article before submitting it for approval to confirm it reflects the correct resolution information.

## Procedure

1.  Navigate to **Workspaces** &gt; **LEAP**.

2.  On the LEAP landing page, select the automation opportunity for which you want to generate a knowledge base article.

3.  If resolution steps are unavailable in the Overview section, select **Generate resolution steps** and wait for the steps to be generated.

4.  Select **Actions** &gt; **Draft KB article**.

    A dialog opens to configure the location and category of the knowledge base where the article created should reside.

    **Tip:** You can also generate a knowledge base article by selecting the \[Omitted image "Otto-01.svg"\] Alt text: Ask Otto button to open the ServiceNow Otto panel and selecting the **draft KB article** option from the menu. Articles created this way route to the default knowledge base configured in LEAP properties.

5.  In the dialog, select a knowledge base from the **Select knowledge base** list.

    The list shows only the knowledge bases selected in the **Eligible knowledge bases** field in LEAP properties. If no eligible knowledge bases are configured, all active knowledge bases are shown.

6.  Select a category from the **Category** list.

    Categories are filtered based on the knowledge base you selected.

7.  In the **KB Meta** field, add or remove tags to improve the discoverability of the article for virtual agents and search.

    Meta tags help virtual agents find the correct knowledge base article. Tags are pre-populated based on the automation opportunity context. You can add new tags or remove existing ones as needed.

8.  Select **Draft KB article**.

    LEAP generates a complete knowledge base article and opens it in the Knowledge Center in draft state.

9.  Review the generated article, including all sections and automatically populated metadata, and make any corrections.

    Technical commands and code snippets are formatted with monospace font and include platform-specific context where applicable.

10. Submit the article through the knowledge base approval workflow.

    After approval, the article is published to the Knowledge Center. It is linked to the originating incident record and suggested when similar incidents occur.


