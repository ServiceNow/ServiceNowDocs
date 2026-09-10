---
title: Generate a knowledge article from a closed supplier case
description: Generate a draft knowledge article from a closed supplier case using ServiceNow Otto for SLO, then review and publish it to the knowledge base.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/generate-article-case.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 1
breadcrumb: [Use, ServiceNow Otto for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Generate a knowledge article from a closed supplier case

Generate a draft knowledge article from a closed supplier case using ServiceNow Otto for SLO, then review and publish it to the knowledge base.

## Before you begin

-   The supplier case must be in the **Closed Completed** state with no existing knowledge article linked to it.
-   Source-to-Pay Workspace must be configured with knowledge article generation enabled.

**Note:** AI-generated content may contain inaccuracies. Review and verify all generated articles before publishing.

Role required: sn\_supplier\_gen\_ai.now\_assist\_fulfiller

## About this task

## Procedure

1.  Navigate to **Workspaces** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon.\) to view your cases.

3.  Open a closed supplier case assigned to you.

4.  Select **Create Knowledge**.

    This option appears only when the case has no associated knowledge article.

5.  In the dialog box, select **Draft with AI**.

    If additional relevant tasks exist, they appear. You can select up to five tasks to include in the knowledge article.

6.  Select the tasks to include in the knowledge article.

    1.  Select the tasks you want to include, then select **Continue with selected tasks**.

    2.  Select **Continue without more tasks** to proceed without additional tasks.

    The generated article opens in a new tab with a unique ID and is automatically linked to the supplier case.

7.  Review the article and edit as needed.

    Verify the accuracy of all AI-generated article content.

8.  Select **Save**.

9.  Select **Publish**.

    A confirmation message appears.


## Result

The published knowledge article is linked to the supplier case and added to the knowledge base.

If the article generation fails, an error message appears. Verify that knowledge article generation is configured correctly and try again. If the issue persists, contact your administrator.

