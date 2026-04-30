---
title: Migrate Social Q&amp;A data to Communities
description: If you want to migrate existing Social Q&amp;A content to Communities, you can use a script to migrate the data.
locale: en-US
release: zurich
product: Communities
classification: communities
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring communities, Communities, Customer Service Management]
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

**Parent Topic:**[Configuring communities](../reference/configure-communities.md)

**Related topics**  


[Community content types](../concept/c_communities-content-types.md)

[Community feedback types](../concept/feedback-types.md)

[Community access types](../concept/access-types.md)

[Platform Analytics Solutions for Communities](../../../use/dashboards/application-content-packs/communities-content-pack.md)

[View community logs](view-community-logs.md)

[View community feedback and bookmarks tables](view-feedback-bookmark-tables.md)

[Create a case from a discussion](../concept/case-management-integration.md)

[Enable knowledge harvesting](../concept/communities-km-integration-configure.md)

[Activate Communities plugins](activate-communities.md)

[Community setup guide for admins](../reference/r_setup-communities-admin.md)

[Configure community content types](enable-content-types-for-community.md)

[Configure video sources for a community](../../customer-service-management/task/create-video-configuration.md)

[Configure community forums](configure-forums-topics.md)

[Forum and user permissions management](../concept/communities-permissions.md)

[Configure the community profile](configure-community-profile.md)

[Create community Terms and Conditions](create-terms-conditions.md)

[Enable users to self-register to a community](../concept/configure-registration.md)

[Moderate a community](moderate-communities.md)

[Administer gamification](../concept/communities-gamification-administer.md)

[Community Service Portal](../concept/community-service-portal.md)

