---
title: Generate LEAP knowledge base articles
description: Generate AI-enhanced knowledge base articles from automation opportunity resolution steps to share structured, publication-ready knowledge across your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/generate-aiops-leap-knowledge-base.html
release: zurich
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 1
keywords: [LEAP knowledge base, KB article generation, resolution steps, automation opportunity]
breadcrumb: [Using LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Generate LEAP knowledge base articles

Generate AI-enhanced knowledge base articles from automation opportunity resolution steps to share structured, publication-ready knowledge across your organization.

## Before you begin

Resolution steps must exist for the automation opportunity before you can generate a knowledge base article.

Role required: admin

## About this task

LEAP uses AI to transform resolution steps into a complete, structured knowledge base article. The generated article includes the following sections:

-   Summary
-   Symptoms — inferred from incident data and resolution context
-   Resolution steps — expanded with sub-steps and code or command formatting
-   Related resources
-   Metadata — including Article Number, Product, Category, Visibility, and Valid To date

The article is created in draft state and routed through the standard knowledge base approval workflow before publication. Each generated article maintains a link to the originating automation opportunity and is suggested when similar incidents occur.

**Note:** AI-generated content may be inaccurate. Review the generated article before submitting it for approval to confirm it reflects the correct resolution information.

## Procedure

1.  Navigate to **Workspaces** &gt; **LEAP**.

2.  On the LEAP landing page, select the automation opportunity for which you want to generate a knowledge base article.

3.  If resolution steps are unavailable in the Overview section, select **Generate resolution steps** and wait for the steps to be generated.

4.  Select **Actions** &gt; **Create KB**.

    LEAP generates a complete knowledge base article from the resolution steps. The article opens in the Knowledge Center in draft state.

    **Tip:** You can also generate a knowledge base article by selecting the \[Omitted image "explore-button.png"\] Alt text: Generate LEAP knowledge base button \[Omitted image "explore-button.png"\] Alt text: to open the Now Assist panel and selecting the knowledge base option from the workflow menu.

5.  Review the generated article, including all sections and auto-populated metadata, and make any corrections.

    Technical commands and code snippets are formatted with monospace font and include platform-specific context where applicable.

6.  Submit the article through the knowledge base approval workflow.

    The article moves through the approval workflow and is published to the Knowledge Center. It is linked to the originating incident record and suggested when similar incidents occur.


