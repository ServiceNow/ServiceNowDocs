---
title: Retire a knowledge article
description: Initiate the retirement workflow to retire a knowledge article. Knowledge base owners and managers can view articles after they are retired but cannot search for retired articles on the Knowledge homepage and portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/knowledge-management/c\_RetiredKnowledgeArticles.html
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Retire a knowledge article

Initiate the retirement workflow to retire a knowledge article. Knowledge base owners and managers can view articles after they are retired but cannot search for retired articles on the Knowledge homepage and portal.

A knowledge article has an associated retirement workflow, similar to the publishing workflow. This allows administrators to configure these workflows, defining an approval and review process for retiring knowledge if appropriate.

When editing an article, select **Retire**. This launches the retirement workflow associated with that article. Only knowledge administrator, knowledge manager, and the latest publisher of the versioned knowledge article \(not available for kcs\_candidate or kcs\_contributor\) can retire a knowledge article. For more information, see [Retire a versioned article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/retire-versioned-article.md). If the article requires approval prior to retirement, the article goes to a pending approval state, and the workflow either finishes when approved or cancels if rejected by an approver. The article number associated with the retired article is not available for reuse. For information on the status of a knowledge article see [Knowledge article states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/knowledge-article-states.md).

**Note:**

-   Only administrators and knowledge administrators can view the retired knowledge articles. To reuse a retired article, administrators and knowledge administrators can republish the article. For more information, see [Republish a retired article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/republish-retired-article.md).
-   An article and its translations have a parent-child relationship. Retiring a parent article does not automatically retire all its translated child articles.

You can provide a replacement article while retiring a knowledge article. When the retired article is accessed, the user is automatically redirected to the replacement article with the display message `The article KBxxx is retired and has been replaced with the knowledge article KBxxx`. If no replacement article is available, the page displays the message `Knowledge record not found`. The retire with replacement feature is not supported on classic workspace. By default, the **glide.knowman.enable\_article\_replacement\_on\_retire** system property is set to `true` for new users, to provide a replacement article for a retired article. Set the property to true manually so existing and upgraded users can view and use the feature.

**Note:**

-   Article with replacement returns a 301 code.
-   Article without any replacement returns a 404 code.
-   The retire action on classic workspace will just retire the article and not provide a replacement irrespective of the setting of **glide.knowman.enable\_article\_replacement\_on\_retire**.

## Instant retire and Approval retire workflows

\[Omitted image "Instant-retire-knowledge-article-workflow.png"\] Alt text: Instant retire knowledge article workflow \[Omitted image "Approval-retire-knowledge-article-workflow.png"\] Alt text: Approval retire knowledge article workflow

## Delete a knowledge article

Users with the admin role can delete a published knowledge article. On an article record, select **Delete**. If the **Delete** button isn't displayed, select the more actions icon \(\[Omitted image "more.png"\] Alt text: More actions icon\), and then select **Delete**.

