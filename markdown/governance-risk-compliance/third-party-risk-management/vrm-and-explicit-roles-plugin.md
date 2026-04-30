---
title: TPRM and the Explicit Roles plugin
description: Activating the Third-party Risk Management plugin also installs the Explicit Roles plugin. Administrators assign the snc\_internal and snc\_external roles to provide internal and external users access to the instance.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage the third-party portal, Third-party Risk Management, Governance, Risk, and Compliance]
---

# TPRM and the Explicit Roles plugin

Activating the Third-party Risk Management plugin also installs the Explicit Roles plugin. Administrators assign the snc\_internal and snc\_external roles to provide internal and external users access to the instance.

When third-party contacts are created, they are automatically assigned the snc\_external role, giving them access to resources related to the Third-party portal.

Various tables provide role-based access to record by setting the **Roles** field. If the **Roles** field is empty, all users have access to that record. For example, if the **Roles** field for a Service Catalog item has an empty **Roles** field, all users have access to that Service Catalog item.

However, when the Explicit Roles plugin is installed, the **Roles** field is updated to **snc\_internal**. Also, all users are given the snc\_internal role. Continuing with the previous example:

-   Before installing the Explicit Roles plugin, if a Service Catalog item had an empty **Roles** field, it was accessible to every user.
-   After installing the Explicit roles plugin, the **Roles** field of the Service Catalog item is updated to snc\_internal and all existing users are given the snc\_internal role, making the catalog item accessible to those users.
-   After that, all new users must be assigned the snc\_internal role, or they will not have access to that Service Catalog item.

The following table describes the changes to tables affected by the Explicit Roles plugin.

<table id="table_efk_k55_dcb"><thead><tr><th>

Table

</th><th>

Changes

</th></tr></thead><tbody><tr><td>

Access Control \[sys\_security\_acl\]

</td><td>

For all existing and newly created ACLs without a role requirement, the snc\_internal role is assigned.

</td></tr><tr><td>

Catalog item\[sc\_cat\_item\]

</td><td>

For all records where the **Roles** field is empty, the snc\_internal role is added. If the glide.sc.use\_user\_criteria property is set to false, newly created catalog items are automatically assigned the snc\_internal role. If the property is set to true, the SNC External user criteria is added to all newly created catalog items, excluding external users from viewing the record.

</td></tr><tr><td>

Page\[content\_page\]

</td><td>

For sites that have a login page, where the **Read roles** field is empty, the snc\_internal role is added. For sites that have no login page or that have automatically created content pages, the public role is added.

</td></tr><tr><td>

Navigation Menu \[sys\_app\_application\]

</td><td>

For all records where the **Roles** field is empty, the snc\_internal role is added. Newly created navigation menus with an empty **Roles** field are also automatically assigned the snc\_internal role.

</td></tr><tr><td>

Overview Help Panel \[sys\_ui\_overview\_help\_panel\]

</td><td>

For all records where the **Roles** field is empty, the snc\_internal role is added. Newly created overview panels with an empty **Roles** field are also assigned the snc\_internal role.

</td></tr><tr><td>

Portal Page \[sys\_portal\_page\]

</td><td>

For all records where the **Read** roles field is empty, the snc\_internal role is added. Newly created portal pages with an empty **Read roles** field are also automatically assigned the snc\_internal role.

</td></tr><tr><td>

Processor \[sys\_processor\]

</td><td>

For all records where the **Roles** field is empty, the snc\_internal role is added. Newly created processors with an empty **Roles** field are also automatically assigned the snc\_internal role.

</td></tr><tr><td>

Report \[sys\_report\]

</td><td>

For all records where the **Roles** field is empty, snc\_internal is added. Newly created reports that have an empty **Roles** field when sharing are also automatically assigned the snc\_internal role.

</td></tr></tbody>
</table>