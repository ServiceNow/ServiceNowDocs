---
title: Generate a knowledge article from a closed procurement case
description: Generate a draft knowledge article from a closed procurement case using ServiceNow Otto for Sourcing and Procurement Operations \(SPO\), then review and publish it to the knowledge base.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/generate-knowledge-article-procurement-case.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 1
breadcrumb: [Generate a knowledge article, Use ServiceNow Otto for SPO, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Generate a knowledge article from a closed procurement case

Generate a draft knowledge article from a closed procurement case using ServiceNow Otto for Sourcing and Procurement Operations \(SPO\), then review and publish it to the knowledge base.

## Before you begin

-   A procurement case assigned to you in **Closed Completed** state.
-   Source-to-Pay Workspace configured with knowledge article generation enabled.

**Note:** ServiceNow Otto generates knowledge article drafts using AI. Review and verify all content for accuracy before publishing.

Role required: sn\_spend\_gen\_ai.now\_assist\_fulfiller

## Procedure

1.  Navigate to **Workspaces** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon.\) to view your cases.

3.  Open a closed procurement case.

4.  Select **Create Knowledge**.

    This option appears only when the case has no associated knowledge article.

5.  In the dialog box, select **Draft with AI**.

    If additional relevant tasks exist, they appear. You can select up to five tasks to include in the knowledge article.

6.  Select the tasks to include in the knowledge article.

    1.  Select the tasks you want to include, then select **Continue with selected tasks**.

    2.  Select **Continue without more tasks** to proceed without additional tasks.

    The generated article opens in a new tab with a unique ID and is automatically linked to the case.

7.  Review the article and edit as needed.

    Verify the accuracy of all AI-generated article content.

8.  Select **Save**.

9.  Select **Publish**.

    A confirmation message appears. The article is published and available in the knowledge base.


## Result

Your knowledge article is published, linked to the case, and discoverable in the knowledge base.

If article generation fails:

-   Verify that knowledge article generation is configured in your ServiceNow instance.
-   Confirm the procurement case is in **Closed Completed** state.
-   Try again.

If the issue persist, contact your administrator.

**Parent Topic:**[Generate a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/spo-generate-knowledge-article.md)

