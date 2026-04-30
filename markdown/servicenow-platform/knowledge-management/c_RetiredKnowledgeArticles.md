---
title: Retire a knowledge article
description: Initiate the retirement workflow to retire a knowledge article. Knowledge base owners and managers can view articles after they are retired but cannot search for retired articles on the Knowledge homepage and portal.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Creating and maintaining articles, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Retire a knowledge article

Initiate the retirement workflow to retire a knowledge article. Knowledge base owners and managers can view articles after they are retired but cannot search for retired articles on the Knowledge homepage and portal.

A knowledge article has an associated retirement workflow, similar to the publishing workflow. This allows administrators to configure these workflows, defining an approval and review process for retiring knowledge if appropriate.

When editing an article, click **Retire** to launch the retirement workflow associated with that article. Only knowledge administrator, knowledge manager, and the latest publisher of the versioned knowledge article \(not available for kcs\_candidate or kcs\_contributor\) can retire a knowledge article. For more information, see [Retire a versioned article](../task/retire-versioned-article.md). If the article requires approval prior to retirement, the article goes to a pending approval state, and the workflow either finishes upon approval or cancels if rejected by a required approver. The article number associated with the retired article is not available for reuse. For information on the status of a knowledge article see [Knowledge article states](knowledge-article-states.md).

**Note:**

-   Only administrators and knowledge administrators can view the retired knowledge articles. To reuse a retired article, administrators and knowledge administrators can republish the article. For more information, see [Republish a retired article](../task/republish-retired-article.md).
-   An article and its translations have a parent-child relationship. Retiring a parent article does not automatically retire all its translated child articles.

Beginning with the San Diego release, you can provide a replacement article while retiring a knowledge article. When the retired article is accessed, the user will automatically be redirected to the replacement article with a display message `The article KBxxx is retired and has been replaced with the knowledge article KBxxx`. If no replacement article is available, the page displays the message `Knowledge record not found`. The retire with replacement feature is not supported on classic workspace. By default, the **glide.knowman.enable\_article\_replacement\_on\_retire** system property is set to `true` for new users, to provide a replacement article for a retired article. Existing and upgraded users must enable this property \(set it to true manually\), to able to view and use the feature.

**Note:**

-   Article with replacement returns a 301 code.
-   Article without any replacement returns a 404 code.
-   The retire action on classic workspace will just retire the article and not provide a replacement irrespective of the setting of **glide.knowman.enable\_article\_replacement\_on\_retire**.

## Instant retire and Approval retire workflows

![Instant retire knowledge article workflow](../image/Instant-retire-knowledge-article-workflow.png) ![Approval retire knowledge article workflow](../image/Approval-retire-knowledge-article-workflow.png)

