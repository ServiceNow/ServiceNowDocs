---
title: Migrate Social Q&amp;A data to Communities
description: If you want to migrate existing Social Q&amp;A content to Communities, you can use a script to migrate the data.
locale: en-US
release: yokohama
product: Communities
classification: communities
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure a community, Communities, Customer Service Management]
---

# Migrate Social Q&amp;A data to Communities

If you want to migrate existing Social Q&amp;A content to Communities, you can use a script to migrate the data.

## Before you begin

Role required: sn\_communities.admin

The Customer Communities plugin \(com.sn\_customer\_communities\) must be activated.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Search for the script Migrate Social QA to Community and open it.

3.  To enable the script, select the **Active** check box and click **Update**.

    The script is deactivated by default.

4.  Click **Run Fix Script**.

    The **Run Fix Script** popup appears.

5.  Click **Proceed in Background**.

    Always use this option for long-running scripts, or if you do not know the expected execution time.

6.  Check the status of the fix script and review the results from the Show Progress Workers related list.


## What to do next

Verify the following information.

-   A new forum is created for every knowledge base that has Social Q&amp;A content.
-   All questions, answers, comments, helpful votes, and upvotes are migrated.
-   All view counts, answer counts, and comment counts are migrated.
-   The accepted solution to a question in Social Q&amp;A is **Marked as Correct Answer** in Communities.
-   Social Q&amp;A is deactivated for every knowledge base that contained Social Q&amp;A data. Social Q&amp;A content is no longer visible for these knowledge bases.

**Parent Topic:**[Configure a community](configure-communities.md)

