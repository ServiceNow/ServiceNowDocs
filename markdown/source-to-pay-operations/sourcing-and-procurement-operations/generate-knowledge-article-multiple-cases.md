---
title: Generate a knowledge article from multiple procurement cases
description: Use ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) to generate a single knowledge article from multiple closed procurement cases in the Source-to-Pay Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/generate-knowledge-article-multiple-cases.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Generate a knowledge article, Use ServiceNow Otto for SPO, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Generate a knowledge article from multiple procurement cases

Use ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) to generate a single knowledge article from multiple closed procurement cases in the Source-to-Pay Workspace.

## Before you begin

-   One or more procurement cases assigned to you in **Closed Completed** state.
-   Source-to-Pay Workspace configured with knowledge article generation enabled.

**Note:** ServiceNow Otto generates knowledge article drafts using AI. Review and verify all content for accuracy before publishing.

Role required: sn\_spend\_gen\_ai.now\_assist\_fulfiller

## About this task

Generate a knowledge article from multiple related procurement cases to create comprehensive documentation that addresses common issues. This workflow builds your knowledge repository from a set of closed cases rather than one case at a time.

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Knowledge** &gt; **Create new article**.

2.  In the dialog box, select **Draft with AI**.

3.  Select a closed procurement case from the list.

4.  In the **Search from tasks** field, enter keywords to find cases.

    Cases matching your search criteria appear in the results list.

5.  Select the closed procurement cases to combine into a single knowledge article.

    Select cases that address similar issues or resolutions.

6.  Select **Continue with selected tasks**.

7.  Review the article and edit as needed.

8.  Select **Submit**.

    A message appears indicating that the knowledge article is saved as a draft and linked to all selected cases.

9.  Select **View Article** to open the draft article.

10. Make any final edits to the article.

11. Select **Publish**.

    A confirmation message appears. The article is published and available in the knowledge base.


## Result

The published knowledge article is linked to all selected cases and available in the knowledge base.

If article generation fails:

-   Verify that knowledge article generation is configured in your ServiceNow instance.
-   Confirm the procurement case is in **Closed Completed** state.
-   Try again.

If the issue persist, contact your administrator.

**Parent Topic:**[Generate a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/spo-generate-knowledge-article.md)

