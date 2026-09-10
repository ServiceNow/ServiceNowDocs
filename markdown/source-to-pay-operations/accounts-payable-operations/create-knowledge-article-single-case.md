---
title: Generate a knowledge article from a case
description: Use ServiceNow Otto to generate a knowledge article from a closed case in the Source-to-Pay Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/create-knowledge-article-single-case.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-15"
reading_time_minutes: 1
keywords: [knowledge article, case management, AI generation, Otto, procurement]
breadcrumb: [Use ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Generate a knowledge article from a case

Use ServiceNow Otto to generate a knowledge article from a closed case in the Source-to-Pay Workspace.

## Before you begin

The case must be in the **Closed** state with no existing knowledge article linked to it.

Knowledge article generation for invoice case skill must be configured.

Role required: sn\_ap\_apm.accounts\_payable\_specialist, sn\_ap\_cm.agent, sn\_ap\_gen\_ai.nowassist\_fulfiller

## About this task

Generate a knowledge article from a closed case to capture solutions and build your knowledge repository. ServiceNow Otto drafts the article content based on case details, which you can review and edit before publishing.

## Procedure

1.  Navigate to **Source-to-Pay Workspace** &gt; **List view**.

2.  Open a case assigned to you in the **Closed** state.

3.  Select **Create Knowledge**.

    The **Create Knowledge** action appears only when no knowledge article is linked to the case.

    The Use AI to draft this article modal opens.

4.  Select **Draft with AI**.

    ServiceNow Otto generates the article content. If similar cases exist, a modal displays cases you can include in the article.

5.  Select up to five similar cases to include in the article, then select **Continue with selected tasks**.

    If no similar cases exist, the article is created directly without this step. Similar cases are identified by the AI Search profile titled \[KM\] Multi-task Article Generation.

    The generated article appears in a new tab with a unique ID and is linked to the case.

6.  Select **Generate Knowledge** from the ServiceNow Otto panel to create a knowledge article.

    You're prompted to enter the task number.

    The generated article appears in a new tab with a unique ID and is linked to the case.

7.  Review and edit the generated article content.

    Verify the accuracy of all AI-generated content before publishing.

8.  Select **Save**.

    The article is saved as a draft.

9.  Select **Publish**.

    A success message appears indicating the article is published.


## Result

The published knowledge article is linked to the case and available in the knowledge base.

If the article generation fails, an error message appears. Verify that knowledge article generation is configured correctly and try again. If the issue persists, contact your administrator.

