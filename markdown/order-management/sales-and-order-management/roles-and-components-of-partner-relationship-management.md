---
title: Roles and components of Partner Relationship Management
description: The Partner Relationship Management application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between enterprises and channel partners.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Configure Partner Relationship Management, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
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

Enterprise Partner Admin \(sn\_prm.enterprise\_partner\_admin\)

</td><td>

A user who is an admin for the partner enterprise.

</td><td>

-   sn\_service\_org.writer
-   sn\_prm.channel\_partner\_writer
-   sn\_prm.partner\_program\_writer
-   sn\_prm.partner\_program\_rel\_writer

</td></tr><tr><td>

Enterprise Partner Relationship Manager \(sn\_prm.enterprise\_partner\_rel\_manager\)

</td><td>

Contributor who belongs to an enterprise and is responsible for managing cases associated with the partner hierarchy.

</td><td>

-   sn\_bus\_loc.location\_relationship\_manager
-   sn\_prm.partner\_data\_viewer

</td></tr><tr><td>

Enterprise Partner Agent \(sn\_prm.enterprise\_partner\_agent\)

</td><td>

Fulfiller who belongs to an enterprise and is responsible for fulfilling partner cases.

</td><td>

-   sn\_customerservice\_agent
-   sn\_prm.partner\_data\_viewer

</td></tr><tr><td>

External Partner Manager \(sn\_prm.external\_partner\_manager\)

</td><td>

Contributor who belongs to a partner entity and is responsible for reporting cases associated with their partner hierarchy on the portal.

</td><td>

-   sn\_customerservice.svc\_location\_manager\_contributor
-   sn\_prm.partner\_data\_viewer

</td></tr><tr><td>

External partner Associate \(sn\_prm.external\_partner\_associate\)

</td><td>

Contributor who belongs to a partner entity and is responsible for reporting cases associated with their partners on the portal.

</td><td>

-   sn\_customerservice.service\_organization\_contributor
-   sn\_prm.partner\_data\_viewer

</td></tr></tbody>
</table>The following table lists the granular roles installed with Partner Relationship Management.

|Role|Description|Inherited roles|
|----|-----------|---------------|
|Channel partner writer \(sn\_prm.channel\_partner\_writer\)|This role provides granular edit access to the channel partner table.|Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)|
|Partner Program Writer \(sn\_prm.partner\_program\_writer\)|This role provides granular edit access to the partner program table.|Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)|
|Partner Program Relationship Writer \(sn\_prm.partner\_program\_rel\_writer\)|This role provides granular edit access to the partner program relationship table.|Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)|
|Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)|This role provides granular read access to the channel partner, partner program, and partner program relationship tables.|NA|

**Related topics**  


[Install Partner Relationship Management](../task/install-partner-relationship-management.md)

[Data model for Partner Relationship Management](data-model-for-partner-relationship-management.md)

