---
title: Article versioning
description: Use the Knowledge Management article versioning feature to create and maintain multiple versions of a knowledge article.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Article versioning

Use the Knowledge Management article versioning feature to create and maintain multiple versions of a knowledge article.

Knowledge contributors can create a new version of a knowledge article from an existing published version. This existing version can be either the latest published version or an older outdated version. All changes are stored in the new version of the article and the information in the existing article remains the same.

If you import published knowledge articles from a ServiceNow instance that does not support article versioning, you must run the Initialize Versions on Articles fix script to enable article checkout and editing.

With the article versioning feature, a knowledge user can:

-   Check out a published article and create another version.

    **Note:** Only an author \(who checks out an article for revision\), knowledge base owner, and user with knowledge\_admin role can edit an article in the draft state.

-   Select a previously published \(outdated\) version of an article and make it current.
-   Recall an article that is being reviewed or scheduled for publication.
-   Retire the latest published version of an article.

**Note:** Only an author \(who checks out an article for revision\), knowledge base owner, and user with knowledge\_admin role can edit an article in the draft state.

There are two types of article revisions: major and minor. Minor revisions include updates to an article that has not yet been published. Major revisions include updates to an article that has been published and is available to customers. To track the different revisions, the article versioning feature introduces version numbering. For more information, see [Knowledge article version numbers](knowledge-article-version-numbers.md)

With the article versioning feature, the knowledge article number also includes the version number. All references to knowledge articles use this number format. For example, KB0010003 v2.0. To access all the versions of knowledge article, navigate to **All** &gt; **Knowledge** &gt; **Articles** &gt; **All** and open article with multiple versions. In the Related list, you can access all the versions.

![multiple versions of article](../image/versioning-control.png "Versioning control")

## Activation information

The article versioning feature requires the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\) to be activated and the **glide.knowman.versioning.enabled** property to be set to true \(default value\). For more information, see [Activate the Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md) and [Article versioning properties](../reference/r_KnowledgeProperties.md#).

**Related topics**  


[Use article versioning](use-article-versioning_0.md)

[Knowledge Management FAQ](https://community.servicenow.com/community?id=community_article&sys_id=637ffc92db519490d82ffb24399619f3)

