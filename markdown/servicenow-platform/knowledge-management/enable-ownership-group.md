---
title: Ownership groups
description: Configure ownership groups and associate them with knowledge articles to maintain article quality, manage approvals, and for timely resolution of feedback.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Ownership groups

Configure ownership groups and associate them with knowledge articles to maintain article quality, manage approvals, and for timely resolution of feedback.

For the ease of maintenance of knowledge articles, you can assign an ownership group to a knowledge article and shift the ownership of an article from a single person to a group. An ownership group consists of a group of members and a manager who are responsible for knowledge articles. Responsibilities include: approving knowledge articles, performing AQI checks to ensuring article quality, and managing feedback tasks for knowledge articles.

When a knowledge article is assigned to an ownership group:

-   Only ownership group members have contribute access to the article even if they don't have contribute access to the knowledge base of the article. They can edit, approve, publish, and retire the knowledge article with which they are associated.
-   Users who aren't a member of the ownership group and not an author or editor can't contribute to the article even if they have **contribute** access to the knowledge base of the article.

When [Create a knowledge article from an incident in ITSM Agent Workspace](../task/create-knowledge-article.md) or [editing](../task/edit-knowledge-article.md) a knowledge article, you may need to configure the Knowledge form to add the **Ownership Group** field.

## Activation information

To enable the use of ownership groups, enable the **glide.knowman.ownership\_group.enabled** property. This property is available when the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) is activated. By default, the property is disabled.

**Note:** If you use ownership groups, try not to disable the **glide.knowman.ownership\_group.enabled** property later. If you must disable the property later, ensure that you manually reassign all knowledge articles associated with any ownership group, close all article approvals sent to ownership groups, and resolve all open feedback tasks assigned to ownership groups.

## Contribute access to published articles

If an ownership group is associated with a knowledge article, the author or reviser of the article can't contribute to the article after the article is published. You can override this behavior by enabling the **glide.knowman.ownership\_group.override** property. When the property is set to `true`, the authors or revisers of knowledge articles associated with ownership groups retain contribute access to their published articles. By default, the property is set to false.

## Approval of self-authored articles for ownership group members

With an ownership group associated with a knowledge article, ownership group members can approve self-authored articles for publication. You can override this behavior by disabling the **glide.knowman.ownership\_group.allow\_self\_approval** property. By default, the property is set to true. When the property is set to `false`, ownership group members can't approve self-authored knowledge articles.

**Related topics**  


[Manage ownership groups](../task/create-edit-ownership-group.md)

[Knowledge Management properties](../reference/r_KnowledgeProperties.md#)

