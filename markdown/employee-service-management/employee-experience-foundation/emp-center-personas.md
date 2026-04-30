---
title: Employee Center users and roles
description: Employee Center plugins include necessary roles for configuring and using the features. Learn more about the roles and the tasks they can perform.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure, Employee Center, Employee Service Management]
---

# Employee Center users and roles

Employee Center plugins include necessary roles for configuring and using the features. Learn more about the roles and the tasks they can perform.

Users and roles are configured at the platform level. For information, see [Exploring user administration](https://www.servicenow.com/docs/access?context=exploring-user-administration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

<table id="table_enp_ltx_sqb"><thead><tr><th>

Users

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Employee Center Admin\[sn\_hr\_sp.esc\_admin\]

</td><td>

A user with this role can manage and configure the Employee Center.**Note:** The sp\_admin and esc\_admin have scripting rights. These roles can create a widget and run a script to update cross-scope tables.

</td><td>

-   sn\_hr\_sp.admin
-   sp\_admin
-   esc\_admin
-   catalog\_admin
-   chat\_admin
-   live\_feed\_admin

</td></tr><tr><td>

Content Admin \(Employee Center Pro\)\[sn\_cd.content\_admin\]

</td><td>

-   Define [Content Ownership](ecpro-content-restriction.md)
-   Connect Content Publishing with a [Video hosting integrations framework](content-providers.md)

</td><td>

-   Content Manager \[sn\_cd.manager\]
-   Template Owner \[sn\_cd.content\_template\_owner\]

</td></tr><tr><td>

Content Manager \(Employee Center Pro\)\[sn\_cd.content\_manager\]

</td><td>

Create, edit and publish content in [Content Publishing](ec-publish-content.md)

</td><td>

None

</td></tr><tr><td>

Engagement Admin \(Employee Center Pro\)

 \[sn\_ce.admin\]

</td><td>

Configure reactions for [Content engagement](ec-content-engagement.md)

</td><td>

None

</td></tr><tr><td>

Template Owner \(Employee Center Pro\)\[sn\_cd.content\_template\_owner \]

</td><td>

This role allows users to create [Content templates](ec-content-templates.md) for news article content creation and publishing.

</td><td>

None

</td></tr><tr><td>

Campaign Manager \(Employee Center Pro\)\[sn\_ca.campaign\_manager\]

</td><td>

Create, edit and publish [Campaigns](ec-content-governance.md)

</td><td>

-   sn\_esign.config\_manager
-   sn\_cda.analytics\_reader
-   sn\_cd.content\_approver

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

A user criteria on the topic record for topic management level tasks, such as, handling connected content, features content, Knowledge Base

</td><td>

Not applicable

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Employee Center](setup-emp-center.md)

**Related topics**  


[Understanding Employee Center plugins](install-plugins.md)

[Setup browse experience features](setup-browse-experience.md)

[Setup search experience features](setup-search-experience.md)

[Setup task management and integration features](setup-task-mgmt.md)

[Setup continuous improvement features](setup-continuous-improvement.md)

[Setup employee communications](setup-employee-comms.md)

[Configure your Employee Center portal](configure-ec-portal.md)

[Moveworks for Employee Center](moveworks-for-employeecenter.md)

[Employee Center Pro Kiosk](deskless-kiosk-overview.md)

[Configuring Employee Center for mobile](ec-mobile-configrations.md)

[Quick start tests for Employee Center](../../../administer/atf-quick-start-tests/reference/quick-start-tests-employee-center.md)

