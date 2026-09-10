---
title: Generate a knowledge article from multiple closed cases
description: Generate a draft knowledge article from multiple closed supplier cases using ServiceNow Otto for SLO, then review and publish it to the knowledge base.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/generate-article-multiple-cases.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Use, ServiceNow Otto for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Generate a knowledge article from multiple closed cases

Generate a draft knowledge article from multiple closed supplier cases using ServiceNow Otto for SLO, then review and publish it to the knowledge base.

## Before you begin

-   The supplier cases must be in the **Closed Completed** state with no existing knowledge article linked to them.
-   Source-to-Pay Workspace must be configured with knowledge article generation enabled.

**Note:** AI-generated content may contain inaccuracies. Review and verify all generated articles before publishing.

Role required: sn\_supplier\_gen\_ai.now\_assist\_fulfiller

## About this task

Generate a knowledge article from multiple related closed supplier cases to create comprehensive documentation that address common issues. This workflow builds your knowledge repository from a set of closed cases rather than one case at a time.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Supplier Knowledge** &gt; **Create new article**.

    The **Use AI to draft article?** modal opens.

2.  Select **Draft with AI**.

3.  Select the case type from the list.

    By default **Supplier Case** is selected.

4.  In the **Search from tasks** field, enter keywords to find cases.

    Cases matching your search criteria appear in the results list.

5.  Select the cases you want to combine into a single knowledge article.

    You can select multiple cases that address similar issues or solutions.

6.  Select **Continue with selected tasks**.

    ServiceNow Otto generates article content based on the selected cases.

7.  Review and edit the generated article content.

    Verify the accuracy of all AI-generated content before publishing. The article combines information from all selected cases.

8.  Select **Submit**.

    A message appears indicating that the knowledge article is saved as a draft and linked to all selected cases.

9.  Select **View Article** to open the draft article.

10. Make any final edits to the article.

11. Select **Publish**.

    A success message appears indicating the article is published.


## Result

The published knowledge article is linked to all selected cases and available in the knowledge base.

If the article generation fails, an error message appears. Verify that knowledge article generation is configured correctly and try again. After the article generation process starts, it can't be stopped. Generation continues even if you close the modal.

