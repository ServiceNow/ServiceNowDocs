---
title: Assigning user roles for Telecommunications Network Inventory
description: You can assign roles to control user access to specific features, capabilities, and data in the Telecommunications Network Inventory application. These assigned roles enable or prevent access to specific forms and processes by users with the specified roles only.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Assigning user roles for Telecommunications Network Inventory

You can assign roles to control user access to specific features, capabilities, and data in the Telecommunications Network Inventory application. These assigned roles enable or prevent access to specific forms and processes by users with the specified roles only.

You assign roles to users and groups by using the ServiceNow AI Platform user administration feature.

-   To assign a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   To assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

The Telecommunications Network Inventory provides the following roles:

<table id="table_wsf_2d2_htb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inventory Admin \[sn\_ni\_core.inventory\_template\_admin\]

</td><td>

Role that enables a user with create, read, update, and delete access to all Telecommunications Network Inventory application-related functions.

</td></tr><tr><td>

Inventory Catalog Manager \[sn\_ni\_core.telco\_inventory\_catalog\_manager\]

</td><td>

Role that enables a user with create, read, edit, and delete access to the metadata for all network inventory entities. This role also enables the user to associate the metadata of the different entities.

</td></tr><tr><td>

Inventory Template Manager \[sn\_ni\_core.inventory\_template\_manager\]

</td><td>

Role that enables a user with create, read, edit, and delete access to the network inventory templates for the new or existing entities. Also, this role enables the user to perform a Create, Read, Update, Delete \(CRUD\) operation on the default template.

</td></tr><tr><td>

Inventory Agent \[sn\_ni\_core.inventory\_agent\]

</td><td>

Role that enables a user with the following permissions:-   Read access to all inventory models, capacity metrics, and pack tables.
-   Write, update, and delete access to the inventory tables.
-   Read and write access to the template, change request and change task table.

**Note:** To modify the model and model relationships tables, a user assigned with the Inventory Agent role must also have either the Asset or Inventory User roles.

</td></tr><tr><td>

Inventory Number Manager \[sn\_inv\_num\_mgmt.inventory\_number\_manager\]

</td><td>

Role that enables a user with the following permissions:-   Read access to all telephone number tables.
-   Write, update, and delete access to the telephone number tables.

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Telecommunications Network Inventory](configuring-telecom-network-inventory.md)

