---
title: Assign user role
description: You can assign roles to control user access to specific features, capabilities, and data in the Telecommunications Network Inventory application. These assigned roles enable or prevent access to specific forms and processes by users with the specified roles only.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/telecom-inventory-roles.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Telecommunications Network Inventory]
---

# Assign user role

You can assign roles to control user access to specific features, capabilities, and data in the Telecommunications Network Inventory application. These assigned roles enable or prevent access to specific forms and processes by users with the specified roles only.

You assign roles to users and groups by using the ServiceNow AI Platform user administration feature.

-   To assign a role to a user, see Assign a role to a user.
-   To assign a role to a group, see Assign a role to a group.

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
</table>Starting with the Telecommunications Network Inventory \(v12.1\) June 2026 release, the following standard ServiceNow platform roles no longer have read access to specific TNI tables. This change was made to confirm that subscription consumption accurately reflects only the products a customer has purchased.

If your users are assigned any of the roles listed below, they will no longer be able to read or query the affected tables. You can explicitly grant access by assigning the appropriate TNI-specific roles to those users.

**Affected tables and roles**

<table id="table_k2k_2fh_mjc"><tbody><tr><td>

**Table**

</td><td>

**Role removed**

</td><td>

**ACL type removed**

</td></tr><tr><td>

tni\_entity

</td><td>

asset

</td><td>

Read, Report view

</td></tr><tr><td>

tni\_entity

</td><td>

sn\_cmdb\_user

</td><td>

Read, Report view

</td></tr><tr><td>

tni\_entity

</td><td>

cmdb\_read

</td><td>

Read

</td></tr><tr><td>

tni\_entity

</td><td>

itil

</td><td>

Read, Report view

</td></tr><tr><td>

sn\_ni\_core\_licensing\_resource\_count

</td><td>

usage\_admin

</td><td>

Read, Report view

</td></tr></tbody>
</table>**Note:** The tni\_entity table is owned by TNI Core and is populated when a configuration item \(CI\) is created via TNI. The sn\_ni\_core\_licensing\_resource\_count table is owned by TNI Core and stores licensing resource count data.

**Parent Topic:**[Configuring Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/configuring-telecom-network-inventory.md)

