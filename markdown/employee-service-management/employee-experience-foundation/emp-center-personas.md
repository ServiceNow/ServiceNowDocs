---
title: Employee Center roles
description: Employee Center plugins include necessary roles for configuring and using the features. Learn more about the roles and the tasks they can perform.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Admin configurations, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Employee Center roles

Employee Center plugins include necessary roles for configuring and using the features. Learn more about the roles and the tasks they can perform.

Users and roles are configured at the platform level. For information, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignARoleToAUser.md).

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
</table>