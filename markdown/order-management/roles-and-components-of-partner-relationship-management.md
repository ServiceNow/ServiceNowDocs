---
title: Roles and components of Partner Relationship Management
description: The Partner Relationship Management application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between enterprises and channel partners.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Roles and components of Partner Relationship Management

The Partner Relationship Management application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between enterprises and channel partners.

The PRM plugin \(com.snc.partner\_relationship\_management\) comes with a set of functional and granular roles, each with varying levels of access to raise and address queries.

The PRM application provides access and permissions to users part of both the enterprise and the channel partner ecosystem.

## Functional and granular roles

Functional roles help provide authorized related parties access to enterprise and channel partner members. A granular model helps to protect data by granting the required level of access to the relevant enterprise or channel partner entities. With this functionality, each role is associated with a set of privileges or responsibilities that determine users’ access to certain information.

You can set granular policies that authorize individuals to do their jobs efficiently and effectively, which helps to improve the customer experience.

## Roles and descriptions

Functional roles are a set of granular roles that are required to perform a function that requires access to multiple entities. The following table lists the functional roles for Partner Relationship Management.

<table id="table_xpn_vcw_1fc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Enterprise Partner admin \(sn\_prm.enterprise\_partner\_admin\)

</td><td>

A user who is an admin for the partner enterprise.

</td><td>

-   sn\_service\_org.writer
-   sn\_prm.channel\_partner\_writer
-   sn\_prm.partner\_program\_writer
-   sn\_prm.partner\_program\_rel\_writer
-   sn\_customerservice.csm\_workspace\_user
-   sn\_seg.segment\_mgmt\_admin

</td></tr><tr><td>

Enterprise Partner Relationship Manager \(sn\_prm.enterprise\_partner\_rel\_manager\)

</td><td>

Contributor who belongs to an enterprise and is responsible for managing cases associated with the partner hierarchy.

</td><td>

-   sn\_bus\_loc.location\_relationship\_manager
-   sn\_prm.partner\_data\_viewer
-   sn\_customerservice.csm\_workspace\_user

</td></tr><tr><td>

Enterprise Partner Agent \(sn\_prm.enterprise\_partner\_agent\)

</td><td>

Fulfiller who belongs to an enterprise and is responsible for fulfilling partner cases.

</td><td>

-   sn\_customerservice\_agent
-   sn\_prm.partner\_data\_viewer

</td></tr><tr><td>

Partner Manager \(sn\_prm.external\_partner\_manager\)

</td><td>

Contributor who belongs to a partner entity and is responsible for reporting cases associated with their partner hierarchy on the portal.

</td><td>

-   sn\_customerservice.svc\_location\_manager\_contributor
-   sn\_prm.partner\_data\_viewer
-   sn\_prm\_dr.partner\_deal\_reg\_manager

</td></tr><tr><td>

Partner Associate \(sn\_prm.external\_partner\_associate\)

</td><td>

Contributor who belongs to a partner entity and is responsible for reporting cases associated with their partners on the portal.

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_prm.partner\_data\_viewer

</td></tr></tbody>
</table>The following table lists the granular roles installed with Partner Relationship Management.

<table id="table_zfq_wdw_1fc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Inherited roles

</th></tr></thead><tbody><tr><td>

Channel partner writer \(sn\_prm.channel\_partner\_writer\)

</td><td>

This role provides granular edit access to the channel partner table.

</td><td>

Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)

</td></tr><tr><td>

Partner Program Writer \(sn\_prm.partner\_program\_writer\)

</td><td>

This role provides granular edit access to the partner program table.

</td><td>

Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)

</td></tr><tr><td>

Partner Program Relationship Writer \(sn\_prm.partner\_program\_rel\_writer\)

</td><td>

This role provides granular edit access to the partner program relationship table.

</td><td>

Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)

</td></tr><tr><td>

Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)

</td><td>

This role provides granular read access to the channel partner, partner program, and partner program relationship tables.

</td><td>

NA

</td></tr><tr><td>

Experience \(sn\_prm.partner\_ui\)

</td><td>

This role provides granular access to organization staff to ensure a consistent experience across all user interfaces.**Note:** The Experience role needs to be manually inherited into other roles to view the Partner Relationship Management modules on ServiceNow platform, CSM Configurable Workspace, and the Partner portal.

</td><td>

NA

</td></tr><tr><td>

Program Segment Writer \(sn\_prm.program\_segment writer\)

</td><td>

This role provides users with the create, read, and update access to the Program segment mapping \(sn\_prm\_program\_segment\_mapping\) table.

</td><td>

-   Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)
-   Segment Data Viewer \(sn\_Seg.segment\_mgmt\_data\_viewer\)

</td></tr></tbody>
</table>## System properties

Navigate to **All** &gt; **Partner Relationship Management** &gt; **Properties**. The Enterprise Partner admin \(sn\_prm.enterprise\_partner\_admin\) has the read and write access to the following properties.

-   glide.ui.sn\_prm\_partner\_program\_activity.fields
-   glide.service\_portal.resize\_text.partner.enable\_rem\_conversion
-   glide.ui.sn\_prm\_partner\_program\_relationship\_activity.fields
-   glide.ui.sn\_prm\_channel\_partner\_activity.fields

-   **[Add responsibilities to PRM roles](../task/add-responsibilities-to-prm-roles.md)**  
A responsibility describes a role or function that supports a user. Use responsibility definitions to create relationships between any two partner entities.

**Parent Topic:**[Configure Partner Relationship Management](configure-partner-relationship-management.md)

**Related topics**  


[Install Partner Relationship Management](../task/install-partner-relationship-management.md)

[Data model for Partner Relationship Management](data-model-for-partner-relationship-management.md)

