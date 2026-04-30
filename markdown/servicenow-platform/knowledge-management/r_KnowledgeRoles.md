---
title: Knowledge Management roles
description: Certain roles are required to use Knowledge Management functionality.Users with the knowledge role can contribute to the default knowledge base and access the Knowledge application menu. The knowledge role is a fulfiller role and not a requester role. Requesters can view, comment, and give feedback to the knowledge articles. However, a requester cannot create or edit articles.Knowledge managers perform administrative functions for the knowledge bases they manage defining categories, pinning important articles, and approving changes to articles. Users selected as managers of a knowledge base receive this role automatically. Knowledge role comes as a subordinate role.Knowledge administrator can perform all the administrative tasks associated with maintaining the Knowledge Management system. User selected as a knowledge admin can make changes to all the knowledge bases except the scoped knowledge base. Knowledge role comes as a subordinate role.Knowledge coaches can perform Article Quality Index \(AQI\) surveys on articles, write, edit and review knowledge articles, and coach the team on best practices. Knowledge role comes as a subordinate role.Knowledge domain experts perform AQI surveys on articles and can write, edit and review knowledge management articles. A knowledge domain expert keeps track of the health of knowledge base. Knowledge role comes as a subordinate role.Administrators can configure knowledge workflows, set knowledge properties, and manage knowledge forms and dashboards.Knowledge group managers can add or remove members in ownership groups managed by them. They cannot change the manager assigned in their groups. The manager can only be reassigned by the knowledge administrator. Knowledge group managers are assigned feedback tasks by default. They can reassign tasks to another group member, or group members can assign a feedback task to themselves. Knowledge\_group\_member role comes as a subordinate role.Knowledge group members are part of an ownership group that can be associated to knowledge articles. They can approve knowledge articles, assign feedback tasks to themselves and work on them as well as edit any knowledge articles that their ownership group is assigned to. Knowledge role comes as a subordinate role.Knowledge-Centered Service \(KCS\) candidates understand the basics of Knowledge-Centered Service \(KCS\). Knowledge role comes as a subordinate role.Knowledge-Centered Service \(KCS\) contributors can create or validate knowledge articles in their product areas without being reviewed by a knowledge coach. They may also author and approve articles for broad audience visibility. Knowledge role comes as a subordinate role.Knowledge-Centered Service \(KCS\) publishers are authors who are well versed in KCS standards and create more external-facing articles. Knowledge role comes as a subordinate role.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Knowledge Management reference, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Knowledge Management roles

Certain roles are required to use Knowledge Management functionality.

**Note:** The user criteria determine the access to knowledge articles. For more information, see [Managing access to knowledge bases and knowledge articles](../concept/user-access-knowledge.md).

The kcs\_candidate, kcs\_contributor, and kcs\_publisher roles also include the knowledge role. For more information about these KCS-related roles, see [KCS v6 Practices Guide](https://library.serviceinnovation.org/KCS/KCS_v6/KCS_v6_Practices_Guide).

**Parent Topic:**[Knowledge Management reference](knowledge-management-reference.md)

## Knowledge \[knowledge\]

Users with the knowledge role can contribute to the default knowledge base and access the Knowledge application menu. The knowledge role is a fulfiller role and not a requester role. Requesters can view, comment, and give feedback to the knowledge articles. However, a requester cannot create or edit articles.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Knowledge manager \[knowledge\_manager\]

Knowledge managers perform administrative functions for the knowledge bases they manage defining categories, pinning important articles, and approving changes to articles. Users selected as managers of a knowledge base receive this role automatically. Knowledge role comes as a subordinate role.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Knowledge administrator \[knowledge\_admin\]

Knowledge administrator can perform all the administrative tasks associated with maintaining the Knowledge Management system. User selected as a knowledge admin can make changes to all the knowledge bases except the scoped knowledge base. Knowledge role comes as a subordinate role.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Knowledge coach \[knowledge\_coach\]

Knowledge coaches can perform Article Quality Index \(AQI\) surveys on articles, write, edit and review knowledge articles, and coach the team on best practices. Knowledge role comes as a subordinate role.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Knowledge domain expert \[knowledge\_domain\_expert\]

Knowledge domain experts perform AQI surveys on articles and can write, edit and review knowledge management articles. A knowledge domain expert keeps track of the health of knowledge base. Knowledge role comes as a subordinate role.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Administrator \[admin\]

Administrators can configure knowledge workflows, set knowledge properties, and manage knowledge forms and dashboards.

### Contains Roles

List of roles contained within the role.

-   sn\_templated\_snip.template\_snippet\_admin
-   sn\_employee.admin
-   taxonomy\_admin
-   sn\_ace.ace\_user

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Knowledge group manager \[knowledge\_group\_manager\]

Knowledge group managers can add or remove members in ownership groups managed by them. They cannot change the manager assigned in their groups. The manager can only be reassigned by the knowledge administrator. Knowledge group managers are assigned feedback tasks by default. They can reassign tasks to another group member, or group members can assign a feedback task to themselves. Knowledge\_group\_member role comes as a subordinate role.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Knowledge group member \[knowledge\_group\_member\]

Knowledge group members are part of an ownership group that can be associated to knowledge articles. They can approve knowledge articles, assign feedback tasks to themselves and work on them as well as edit any knowledge articles that their ownership group is assigned to. Knowledge role comes as a subordinate role.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## KCS candidate \[kcs\_candidate\]

Knowledge-Centered Service \(KCS\) candidates understand the basics of Knowledge-Centered Service \(KCS\). Knowledge role comes as a subordinate role.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## KCS contributor \[kcs\_contributor\]

Knowledge-Centered Service \(KCS\) contributors can create or validate knowledge articles in their product areas without being reviewed by a knowledge coach. They may also author and approve articles for broad audience visibility. Knowledge role comes as a subordinate role.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## KCS publisher \[kcs\_publisher\]

Knowledge-Centered Service \(KCS\) publishers are authors who are well versed in KCS standards and create more external-facing articles. Knowledge role comes as a subordinate role.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

