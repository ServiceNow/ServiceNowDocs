---
title: Components installed with response templates
description: Several types of components are installed with activation of the Templated Responses \(com.sn\_templated\_snip\) plugin, including tables and user roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate, Response templates, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with response templates

Several types of components are installed with activation of the Templated Responses \(com.sn\_templated\_snip\) plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

Demo data is available for this feature.

## Roles installed

By default, the following HR roles contain the following response template roles.

**Note:** The Templated Responses \[com.sn\_templated\_snip\] plugin activates the sn\_templated\_snip.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only Response Template admin user by requiring a minimum number \(default is two\) of active users with this role.

<table id="table_ks1_2k3_ldb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Response templates administrator\[sn\_templated\_snip.template\_snippet\_admin\]

</td><td>

Grants access to scoped administration of the response templates feature.

</td><td>

sn\_templated\_snip.template\_snippet\_writer

</td></tr><tr><td>

Response templates writer\[sn\_templated\_snip.template\_snippet\_writer\]

</td><td>

Grants access to create, read, update, and delete \(CRUD\) response template content.

</td><td>

sn\_templated\_snip.template\_snippet\_reader

</td></tr><tr><td>

Response templates reader\[sn\_templated\_snip.template\_snippet\_reader\]

</td><td>

Grants access to read response template content.

</td><td>

None

</td></tr></tbody>
</table>You can assign these roles to the appropriate roles, groups, or users in your application.

-   To assign a role to another role, see Add a role to an existing role.
-   To assign a role to a group, see Assign a role to a group.
-   To assign a role to a user, see Assign a role to a user.

For further information on user administration and how to manage users, see User administration.

## Tables installed

<table id="table_ytw_vj3_ldb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Response Template\[sn\_templated\_snip\_note\_template\]

</td><td>

Stores response template information. Response templates are reusable messages that can be copied to case or task forms. Response templates provide quick and consistent messages to users, or display standard chat response messages to requesters in Agent Chat.

</td></tr><tr><td>

M2M Response Template to Channel\[m2m\_response\_template\_to\_channel\]

</td><td>

Maps channels to response templates.

</td></tr><tr><td>

Response Template Channel\[sn\_templated\_snip\_channel\]

</td><td>

Stores information about response template channels.

</td></tr><tr><td>

Note Template for Table\[sn\_m2m\_note\_template\_for\_table\]

</td><td>

Maps notes to response templates.

</td></tr></tbody>
</table>For further information on table administration and how to manage data, see Table administration.

**Parent Topic:**[Activate response templates](../task/activate-templated-snippets.md)

