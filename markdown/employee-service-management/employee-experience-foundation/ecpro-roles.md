---
title: Employee Center Pro roles
description: Employee Center Pro plugins include necessary roles for configuring and using the features. Learn more about the roles and the tasks they can perform.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Admin configurations, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Employee Center Pro roles

Employee Center Pro plugins include necessary roles for configuring and using the features. Learn more about the roles and the tasks they can perform.

Users and roles are configured at the platform level. For information, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Employee Center

<table id="table_prz_3kf_wcc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Employee Center Admin\[sn\_hr\_sp.esc\_admin\]

</td><td>

A user with this role can manage and configure the Employee Center.**Note:** The sp\_admin and esc\_admin have scripting rights. These roles can create a widget and run a script to update cross-scope tables.

</td><td>

-   catalog\_admin
-   chat\_admin
-   live\_feed\_admin
-   sn\_employee.admin
-   sn\_ex\_emp\_fd.portal\_stats\_manager
-   sn\_hr\_sp.admin
-   sp\_admin

</td></tr><tr><td>

Taxonomy Admin \[taxonomy\_admin\]

</td><td>

A user with this role can update and modify any created taxonomy in the taxonomy and topic table names.

</td><td>

user\_criteria\_admin

</td></tr><tr><td>

Taxonomy Manager

</td><td>

A user criteria on the taxonomy record. A user assigned as a taxonomy manager can manage topics and connected content, but they cannot manage the taxonomy record.

</td><td>

Not applicable

</td></tr><tr><td>

Taxonomy Contributor

</td><td>

A user criteria on the taxonomy record. A user assigned as a taxonomy contributor can associate content to the topics.

</td><td>

Not applicable

</td></tr><tr><td>

Topic Manager

</td><td>

A user criteria on the topic record to decentralize topic management. Users assigned as Topic managers can create, move, or clone topics within or between taxonomies, depending on the rights assigned to them.

</td><td>

Not applicable

</td></tr><tr><td>

Topic Contributor

</td><td>

A user criteria on the topic record for topic management level tasks, such as handling connected content, features content, Knowledge Base

</td><td>

Not applicable

</td></tr></tbody>
</table>## Employee Profile

For more information, see [Employee profile](employee-profile-portal.md)

<table id="table_zs3_3n1_xcc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Employee profile admin\[sn\_employee.admin\]

</td><td>

Configures employee profile

</td><td>

-   image\_admin
-   ml\_admin

</td></tr></tbody>
</table>## Content Analytics

For more information, see [Content Analytics](ecpro-content-automation-analytics.md)

<table id="table_c1c_qjk_rcc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Content analytics admin\[sn\_cda.analytics\_admin\]

</td><td>

Configures tracking profiles and customizes dashboards

</td><td>

-   sn\_cdap.admin
-   user\_admin
-   sn\_cda.analytics\_reader

</td></tr><tr><td>

Content analytics reader\[sn\_cda.analytics\_reader\]

</td><td>

Can view and interact with dashboards

</td><td>

pa\_viewer

</td></tr></tbody>
</table>## Content engagement

For more information, see [Content engagement](ec-content-engagement.md)

<table id="table_s55_2kk_rcc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Content engagement admin\[sn\_ce.admin\]

</td><td>

Configures reaction icons for news articles[Content engagement](ec-content-engagement.md)

</td><td>

sn\_ce.moderator

</td></tr><tr><td>

Content engagement moderator\[sn\_ce.moderator\]

</td><td>

Can remove reported comments from news articles

</td><td>

None

</td></tr></tbody>
</table>## Content Experiences

For more information, see [Creating campaigns](ecpro-campaigns.md)

<table id="table_wjk_xkk_rcc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Campaign admin\[sn\_ca.campaign\_admin\]

</td><td>

Can access, modify, or delete any campaign

</td><td>

-   sn\_ca\_pa.admin
-   sn\_ca.campaign\_manager

</td></tr><tr><td>

Campaign manager\[sn\_ca.campaign\_manager\]

</td><td>

Creates content, assembles content into campaigns, and reviews performance metrics for published content

</td><td>

-   pa.viewer
-   sn\_ca.content\_manager
-   sn\_ca.campaign\_approver

</td></tr><tr><td>

Campaign approver\[sn\_ca.campaign\_approver\]

</td><td>

Reviews and approves campaigns

</td><td>

sn\_cd.content\_approver

</td></tr></tbody>
</table>## Content Governance

For more information, see [Managing content requests](ec-content-governance.md)

<table id="table_l4p_wlk_rcc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Governance admin\[sn\_cg.governance\_admin\]

</td><td>

Can access, assign, or modify any content request

</td><td>

sn\_cg.governance\_manager

</td></tr><tr><td>

Governance manager\[sn\_cg.governance\_manager\]

</td><td>

Can access open content requests and modify the status

</td><td>

None

</td></tr></tbody>
</table>## Content Publishing

For more information, see [Creating employee communications](ec-publish-content.md)

<table id="table_awp_fwk_rcc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Content Admin\[sn\_cd.content\_admin\]

</td><td>

-   Define [Content Ownership](ecpro-content-restriction.md)
-   Connect Content Publishing with a [Video hosting integrations framework](content-providers.md)

</td><td>

-   Content Manager \[sn\_cd.manager\]
-   Template Owner \[sn\_cd.content\_template\_owner\]
-   sn\_cg.governance\_admin
-   sn\_cg.content\_request\_user
-   sn\_cg.content\_request\_item\_user
-   sn\_cd.content\_category\_owner
-   sn\_cda.analytics\_admin
-   sn\_ex\_emp\_fd.portal\_stats\_manager

</td></tr><tr><td>

Content Manager\[sn\_cd.content\_manager\]

</td><td>

Create, edit and publish content in [Content Publishing](ec-publish-content.md)

</td><td>

-   localization\_requestor
-   sn\_cg.governance\_manager
-   sn\_cg.content\_request\_user
-   sn\_cg.content\_request\_item\_user
-   sn\_esign.config\_manager
-   sn\_cd.content\_approver
-   sn\_cda.analytics\_reader

</td></tr><tr><td>

Content approver\[content\_approver\]

</td><td>

Reviews and approves content

</td><td>

approver\_user

</td></tr><tr><td>

Content category owner\[sn\_cd.content\_category\_owner\]

</td><td>

Create, edit, and delete content categories

</td><td>

None

</td></tr><tr><td>

Template Owner\[sn\_cd.content\_template\_owner \]

</td><td>

This role allows users to create [Content templates](ec-content-templates.md) for news article content creation and publishing.

</td><td>

sn\_cd.content\_manager

</td></tr></tbody>
</table>