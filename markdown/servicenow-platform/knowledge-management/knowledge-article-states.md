---
title: Knowledge article states
description: Knowledge article versions can be in one of several states as it progresses through the creation cycle.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge article states

Knowledge article versions can be in one of several states as it progresses through the creation cycle.

**Note:** You need to activate the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) and set the **glide.knowman.versioning.enabled** system property to `true`. For more information, [Activate the Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md) and [Article versioning properties](../reference/r_KnowledgeProperties.md#).

<table id="table_trn_kgl_yy"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The article is in the process of being created.**Note:** A versioned knowledge article in the **Draft** state can be modified only by the author or reviser with the contribute access to the knowledge base, owner of a knowledge base, users with the admin and knowledge\_admin role, and ownership group members, if ownership group is added to the article.

</td></tr><tr><td>

Review

</td><td>

The draft version of the article is sent to reviewers to approve or reject.

</td></tr><tr><td>

Scheduled for publish

</td><td>

The draft version of a knowledge article is scheduled for publishing on a future date.

</td></tr><tr><td>

Published

</td><td>

The article is approved and published. When the state of an article changes to **Published**, the state of any previous published versions of that article changes to **Outdated**.**Note:** After a knowledge article with an ownership group is approved, only the owner of a knowledge base and ownership group members have contribute access to the article.

</td></tr><tr><td>

Pending retirement

</td><td>

The published article is selected for retirement, pending approval.

</td></tr><tr><td>

Retired

</td><td>

The published article is retired. Retired knowledge articles cannot be searched for by external users or customers. To reuse a retired article, create a new article with the same content, which is published once approved.

</td></tr><tr><td>

Outdated

</td><td>

A more recent version of the article has been published. End users can read published articles as well as the outdated versions.

</td></tr></tbody>
</table>**Related topics**  


[Knowledge access controls](user-access-knowledge.md)

