---
title: Migrate Social Q&amp;A data to Communities
description: If you want to migrate existing Social Q&amp;A content to Communities, you can use a script to migrate the data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/communities/migrate-socialqa.html
release: australia
product: Communities
classification: communities
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring communities, Communities, Customer Service Management]
---

# Migrate Social Q&amp;A data to Communities

If you want to migrate existing Social Q&amp;A content to Communities, you can use a script to migrate the data.

## Before you begin

Role required: script\_fix\_Admin

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

**Parent Topic:**[Configuring communities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/configure-communities.md)

**Related topics**  


[Community content types]()

[Community feedback types]()

[Community access types]()

[Platform Analytics Solutions for Communities]()

[View community logs]()

[View community feedback and bookmarks tables]()

[Create a case from a discussion]()

[Enable knowledge harvesting]()

[Activate Communities plugins]()

[Community setup guide for admins]()

[Configure community content types]()

[Configure video sources for a community]()

[Configure community forums]()

[Forum and user permissions management]()

[Configure the community profile]()

[Create community Terms and Conditions]()

[Enable users to self-register to a community]()

[Moderate a community]()

[Administer gamification]()

[Community Service Portal]()

