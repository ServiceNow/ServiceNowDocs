---
title: Managing access to knowledge bases and knowledge articles
description: Determine whether certain users or categories of users can access knowledge bases and knowledge articles by controlling contribute and read access.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Managing access to knowledge bases and knowledge articles

Determine whether certain users or categories of users can access knowledge bases and knowledge articles by controlling contribute and read access.

As a knowledge administrator, manager of a knowledge base, or owner of a knowledge base, you can assign user criteria to control contribute and read access at the knowledge base level, where:

-   Read access determines the ability to view knowledge articles in a knowledge base.
-   Contribute access determines the ability to create, modify, and retire knowledge articles in a knowledge base.

As a knowledge administrator, manager of a knowledge base, or owner of a knowledge base, you can assign user criteria, or roles, or both, to control read access at the knowledge article level.

Try to use only user criteria, which were introduced in Knowledge Management v3, to control access to knowledge articles. Roles were used for this purpose in Knowledge Management v2. If no user criteria is selected for a knowledge base, all users can read and all users with roles can contribute to that knowledge base.

**Note:** By default, when contribute access isn't provided for a knowledge base, a user must meet both roles and user criteria conditions for read access. However, you can override roles set for a knowledge article and provide access through user criteria only by setting the **glide.knowman.search.apply\_role\_based\_security** system property to `false`. Because this property isn't available by default, you must add it. For more information, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

## User criteria for knowledge access

As a knowledge administrator, manager of a knowledge base, or owner of a knowledge base, you control access to knowledge bases or knowledge articles for a user through user criteria, which are described in the following table.

<table id="table_m2t_r55_2jb"><thead><tr><th>

User criteria

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Cannot Contribute

</td><td>

Cannot contribute \(that is can't create, modify, or retire\) knowledge articles within a knowledge base. The Cannot Contribute user criteria is available only for knowledge bases.

</td></tr><tr><td>

Can Contribute

</td><td>

Can contribute \(that is can view, create, modify, or retire\) knowledge articles within a knowledge base. The Can Contribute user criteria is available only for knowledge bases.

</td></tr><tr><td>

Cannot Read

</td><td>

At the knowledge base level, cannot view knowledge articles within a knowledge base.

 At the knowledge article level, cannot view a knowledge article.

</td></tr><tr><td>

Can Read

</td><td>

At the knowledge base level, can view knowledge articles within a knowledge base.

 At the knowledge article level, can view a knowledge article.

</td></tr></tbody>
</table>The access to knowledge base and its articles are defined based on the user criteria status for a user as described in the following table.

|Status|Access|
|------|------|
|The user matches both Can Contribute and Cannot Contribute at the knowledge base level|The user is denied contribute access to the knowledge base and its articles.|
|The user matches both Can Read and Cannot Read at the knowledge base level|The user is denied read access to the knowledge base and its articles.|
|The user matches Can Read at the knowledge base level and Cannot Read at the knowledge article level|The user is denied read access to the knowledge article.|
|The user matches Cannot Read and Can Read at the knowledge article level|The user is denied read access to the knowledge article.|

## Users with special knowledge privileges

Users with special knowledge privileges aren't evaluated based on user criteria and have knowledge bases and knowledge articles access as described in the following table.

<table id="table_a51_jlv_4jb"><thead><tr><th>

User

</th><th>

Access

</th></tr></thead><tbody><tr><td>

Knowledge administrator

</td><td>

-   Contribute to and read all knowledge bases and their articles.
-   Modify the definition of all knowledge bases and assign user criteria to them.

 **Note:** This access doesn't apply to scoped knowledge bases. For more information, see [Scoped knowledge bases](scoped-knowledge-base-administration.md).

</td></tr><tr><td>

Owner of a knowledge base

</td><td>

-   Contribute to and read that knowledge base.
-   Modify the definition of that knowledge base and assign user criteria to it.

</td></tr><tr><td>

Manager of a knowledge base

</td><td>

-   Contribute to and read that knowledge base.
-   Modify the definition of that knowledge base and assign user criteria to it.

 **Note:** If the article versioning feature is enabled, the manager of a knowledge base can’t modify knowledge articles of other authors that are in the **Draft** state. For more information, see [Article versioning](article-versioning.md).

</td></tr><tr><td>

Members of an ownership group associated with a knowledge article

</td><td>

Read, modify, approve, and retire that knowledge article \(see [Ownership groups](enable-ownership-group.md)\).

</td></tr></tbody>
</table>## Explicit roles and user criteria

Explicit roles \(snc\_external and snc\_internal\) are added to your instance when your administrator installs a plugin, such as the Customer Service plugin \(com.sn\_customerservice\), that also activates the Explicit Roles plugin \(com.glide.explicit\_roles\). If you create a knowledge base with the Explicit Roles plugin \(com.glide.explicit\_roles\) activated, the application automatically adds the following predefined user criteria at the knowledge base level:

-   **Users with 'snc\_internal' role** – Added to the Can Read user criteria enabling only users with the snc\_internal role have read access to the knowledge base.
-   **Users with snc\_internal' and another role** – Added to the Can Contribute user criteria enabling only users with the snc\_internal role and at least one additional role have contribute access to the knowledge base.

When you upgrade to product versions \(from Rome onwards\) that offer the Explicit Roles plugin \(com.glide.explicit\_roles\), the predefined user criteria **Users with 'snc\_internal' role** and **Users with 'snc\_internal' and another role** aren't automatically added to any existing knowledge bases created prior to the activation of the Explicit Roles plugin. To add these predefined user criteria to an existing knowledge base, run the Fix unsecured knowledge bases fix script. For more information about explicit roles and fix scripts, see [Explicit Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/explicit-roles.md) and [Fix scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_FixScripts.md).

## Determining contribute access to a knowledge base and its articles using user criteria

The flowchart in this section illustrates the user criteria checks that determine contribute access at the knowledge base and article levels.

**Note:** In order for an unauthenticated user to view knowledge articles within the knowledge base, ensure that the audience for the Knowledge Management Service Portal pages is set to public; that is, the page can be accessed without the need for authentication. For more information, see [Create and edit a page using the Service Portal Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/t_ConfigureAPage.md).

![Flowchart showing how contribute access to a knowledge base and its article using user criteria is evaluated](../image/contribute_access.png "Contribute access to a knowledge base and its article flowchart")

When either Cannot Contribute isn’t set or a user doesn’t match Cannot Contribute and additionally Can Contribute is not set, the **glide.knowman.block\_access\_with\_no\_user\_criteria** property value is further evaluated to determine contribute access, as explained in the following table.

<table id="table_z2b_hrp_qjb"><thead><tr><th>

Property value

</th><th>

Result

</th></tr></thead><tbody><tr><td>

true

</td><td>

No user has contribute access to the knowledge base except [users with special knowledge privileges](user-access-knowledge.md#section_uvc_rqf_sjb).

</td></tr><tr><td>

false

</td><td>

All users, including unauthenticated users, with at least one role can contribute to the knowledge base. If the Explicit Roles plugin \(com.glide.explicit\_roles\) is activated, users who have at least one role other than snc\_internal can contribute to the knowledge base.

 To check knowledge bases accessible to unauthenticated users, use the User Criteria Diagnostics feature. For more information, see [Configure access to knowledge bases for unauthenticated users](../task/configure-unauthenticated-user.md).

</td></tr></tbody>
</table>When a user has contribute access to a knowledge base, the **glide.knowman.apply\_article\_read\_criteria** property is evaluated to determine contribute access to an article in the knowledge base, as explained in the following table.

|Property value|Result|
|--------------|------|
|true|Article-level read access overrides the default contribute permission granted by contribute access at the knowledge base level.|
|false|Contribute access at the knowledge base level takes precedence over article-level user criteria and the user has contribute access to every article in the knowledge base.|

## Determining read access to articles in a knowledge base using user criteria

The following flowchart illustrates the user criteria checks that determine read access to a knowledge article.

![Flowchart showing how read access to a knowledge article using user criteria is evaluated.](../image/read_access.png "Read access to a knowledge article flowchart")

When either Cannot Read isn’t set or a user doesn’t match Cannot Read and additionally Can Read is not set, the **glide.knowman.block\_access\_with\_no\_user\_criteria** property value is further evaluated to determine read access, as explained in the following table.

<table id="table_gmk_z5s_tjb"><thead><tr><th>

Property value

</th><th>

Result

</th></tr></thead><tbody><tr><td>

true

</td><td>

No user has read access except [users with special knowledge privileges](user-access-knowledge.md#section_uvc_rqf_sjb) and users who have contribute access to the knowledge base.

</td></tr><tr><td>

false

</td><td>

All users, including unauthenticated users, have read access to the knowledge base and the article-level user criteria are further evaluated.To check knowledge bases accessible to unauthenticated users, use the User Criteria Diagnostics feature. For more information, see [Configure access to knowledge bases for unauthenticated users](../task/configure-unauthenticated-user.md).

</td></tr></tbody>
</table>When a user has contribute access to a knowledge base, the **glide.knowman.apply\_article\_read\_criteria** property is evaluated to determine read access to an article in the knowledge base, as explained in the following table.

|Property value|Result|
|--------------|------|
|true|Article-level read access overrides the default read permission granted by contribute access at the knowledge base level.|
|false|Contribute access at the knowledge base level takes precedence over article-level user criteria and the user has read access to every article in the knowledge base.|

**Important:** After you add user criteria, you can use the user criteria diagnostics feature to verify the access that users have to a knowledge base or a knowledge article. For more information, see [User criteria diagnostics for Knowledge Management](diagnose-knowledge-user-criteria.md).

-   **[Create user criteria for controlling access to knowledge bases and articles](../task/create-user-criteria-record-in-knowledge-management.md)**  
Control access to knowledge bases and articles by creating user criteria.
-   **[Control access at the knowledge base level through user criteria](../task/t_SelectUserCriteria.md)**  
You specify user criteria for a knowledge base to control which users are granted access to read and contribute knowledge articles to that knowledge base.
-   **[Control access at the knowledge article level through user criteria](../task/t_SelectUCArticle.md)**  
You specify user criteria for a knowledge article to control which users are granted read access to the knowledge article.

**Parent Topic:**[Configuring Knowledge Management](configuring-knowledge-management.md)

**Related topics**  


[Knowledge Management properties](../reference/r_KnowledgeProperties.md#)

[Configuration tasks for knowledge managers](c_KnowledgeManager.md)

[Knowledge Management FAQ](https://community.servicenow.com/community?id=community_article&sys_id=637ffc92db519490d82ffb24399619f3)

[Create user criteria for controlling access to knowledge bases and articles](../task/create-user-criteria-record-in-knowledge-management.md)

