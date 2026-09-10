---
title: Generate a knowledge article from multiple cases
description: Use ServiceNow Otto to generate a single knowledge article from multiple closed cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/create-knowledge-articles-multiple-cases.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-15"
reading_time_minutes: 1
keywords: [knowledge article, multiple cases, bulk generation, AI generation, Otto, procurement]
breadcrumb: [Use ServiceNow Otto for Accounts Payable Operations \(APO\), ServiceNow Otto for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Generate a knowledge article from multiple cases

Use ServiceNow Otto to generate a single knowledge article from multiple closed cases.

## Before you begin

The cases must be in the **Closed** state.

Knowledge article generation for invoice case skill must be configured.

Role required: sn\_ap\_apm.accounts\_payable\_specialist, sn\_ap\_cm.agent, sn\_ap\_gen\_ai.nowassist\_fulfiller

## About this task

Generate a knowledge article from multiple related cases to create comprehensive documentation that addresses common issues. Use this workflow to expand your knowledge repository from a set of closed cases rather than one case at a time.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Create New Article**.

    The Use AI to draft this article modal opens.

2.  Select **Draft with AI**.

3.  Select the case type from the list.

    Available case types include invoice and inquiry case.

4.  In the **Search from tasks** field, enter keywords to find cases.

    Cases matching your search criteria appear in the results list.

5.  Select the cases you want to combine into a single knowledge article.

    You can select multiple cases that address similar issues or solutions.

6.  Select **Continue with selected tasks**.

    ServiceNow Otto generates article content based on the selected cases.

7.  To ensure accuracy, review and edit the generated article content.

    Verify the accuracy of all AI-generated content before publishing. The article combines information from all selected cases.

8.  Select **Submit**.

    A message appears confirms that the knowledge article is saved as a draft and linked to all selected cases.

9.  Select **View Article** to open the draft article.

10. Make any final edits to the article.

11. Select **Publish**.

    A success message appears indicating the article is published.


## Result

The published knowledge article is linked to all selected cases and available in the knowledge base.

If article generation fails, an error message appears. Verify that knowledge article generation is configured correctly and try again. After the article generation process starts, it can't be stopped. Generation continues even if you close the modal.

