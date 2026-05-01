---
title: Roles and components of Deal Registration Management
description: The Deal Registration Management application \(com.snc.deal\_registration\_management\) uses roles to provide access to information, identify internal and external users, and maintain data security.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 3
breadcrumb: [Deal Registration, Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Roles and components of Deal Registration Management

The Deal Registration Management application \(com.snc.deal\_registration\_management\) uses roles to provide access to information, identify internal and external users, and maintain data security.

The Deal Registration Management application \(com.snc.deal\_registration\_management\) comes with a set of functional roles, each with varying levels of access to deals and their line items.

## Functional and granular roles

Functional roles help provide authorized partners to maintain data and records in the deal registration table. A granular model helps to protect data by granting the required level of access to the relevant enterprise or channel partner entities. With this functionality, each role is associated with a set of privileges that determine users’ access to certain information.

You can assign granular policies that authorize individuals to do their jobs efficiently and effectively, which helps to improve customer experience.

## Roles and descriptions

Functional roles are a set of granular roles that are required to perform a function that requires access to multiple entities. The following table lists the functional roles for Deal Registration Management.

<table id="table_fz3_ffk_3hc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Deal registration admin \(sn\_prm\_dr.deal\_reg\_admin\)

</td><td>

This user can configure the deal registration data model and can create and edit all deal registrations across multiple partner types.

</td><td>

-   Deal registration type writer \(sn\_prm\_dr.deal\_reg\_type\_writer\)
-   Deal registration writer \(sn\_prm\_dr.deal\_reg\_writer\)

</td></tr><tr><td>

B2B deal registration initiator \(sn\_prm\_dr.partner\_b2b\_deal\_reg\_initiator\)

</td><td>

This user can create, view, and track deal registrations for all B2B customers with their associated channel partners.

</td><td>

Partner data viewer \(sn\_prm.partner\_data\_viewer\)

</td></tr><tr><td>

B2C deal registration initiator \(sn\_prm\_dr.partner\_b2c\_deal\_reg\_initiator\)

</td><td>

This user can create, view, and track deal registrations for all B2C customers with their associated channel partners.

</td><td>

Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)

</td></tr><tr><td>

Deal registration initiator \(sn\_prm\_dr.partner\_deal\_reg\_initiator\)

</td><td>

This user can create and view deal registrations for both B2B and B2C customers for their associated channel partners.

</td><td>

-   B2B deal registration initiator \(sn\_prm\_dr.partner\_b2b\_deal\_reg\_initiator\)
-   B2C deal registration initiator \(sn\_prm\_dr.partner\_b2c\_deal\_reg\_initiator\)

</td></tr><tr><td>

Deal registration manager \(sn\_prm\_dr.partner\_deal\_reg\_manager\)

</td><td>

This user can create and view deal registrations for all the partners across their associated partner hierarchy.

</td><td>

Deal registration initiator \(sn\_prm\_dr.partner\_deal\_reg\_initiator\)

</td></tr><tr><td>

Enterprise deal registration relationship contributor \(sn\_prm\_dr.enterprise\_deal\_reg\_rel\_contributor\)

</td><td>

This user can create, edit, and approve deal registrations for associated channel partners.

</td><td>

Partner data viewer \(sn\_prm.partner\_data\_viewer\)

</td></tr><tr><td>

Enterprise deal registration relationship manager \(sn\_prm\_dr.enterprise\_deal\_reg\_rel\_manager\)

</td><td>

This user can create, edit, and approve deal registrations for channel partners within their assigned hierarchy.

</td><td>

Enterprise deal registration relationship contributor \(sn\_prm\_dr.enterprise\_deal\_reg\_rel\_contributor\)

</td></tr><tr><td>

B2B deal registration agent \(sn\_prm\_dr.enterprise\_b2b\_deal\_reg\_agent\)

</td><td>

This user can create, qualify, approve, and convert B2B deals into opportunities.A B2B deal registration agent can manage the full life cycle for B2B deal registrations.

To learn more about converting deals to opportunities, see [Update deal registration record](../task/update-deal-registration-record.md)

</td><td>

Partner data viewer \(sn\_prm.partner\_data\_viewer\)

</td></tr><tr><td>

B2C deal registration agent \(sn\_prm\_dr.enterprise\_b2c\_deal\_reg\_agent\)

</td><td>

This user can create, qualify, approve, and convert B2C deals into opportunities.A B2C deal registration agent can manage the full life cycle for B2C deal registrations.

To learn more about converting deals to opportunities, see [Update deal registration record](../task/update-deal-registration-record.md)

</td><td>

Partner Data Viewer \(sn\_prm.partner\_data\_viewer\)

</td></tr><tr><td>

Deal registration agent \(sn\_prm\_dr.enterprise\_deal\_reg\_agent\)

</td><td>

This user can create, qualify, approve, and convert any deal registration into an opportunity. A deal registration agent can manage the full life cycle of submitted deal registrations, both B2B and B2C.

To learn more about converting deals to opportunities, see [Update deal registration record](../task/update-deal-registration-record.md)

</td><td>

-   B2B deal registration agent \(sn\_prm\_dr.enterprise\_b2b\_deal\_reg\_agent\)
-   B2C deal registration agent \(sn\_prm\_dr.enterprise\_b2c\_deal\_reg\_agent\)

</td></tr></tbody>
</table>The following table lists the set of granular roles associated with deal registration.

<table id="table_hhj_jfk_3hc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Deal registration data viewer \(sn\_prm\_dr.deal\_reg\_data\_viewer\)

</td><td>

This granular role provides users read access to all deal registrations.

</td><td>

Partner data viewer \(sn\_prm.partner\_data\_viewer\)

</td></tr><tr><td>

Deal registration type writer \(sn\_prm\_dr.deal\_reg\_type\_writer\)

</td><td>

This granular role provides users to create, write, and edit all deal registration types.With this granular role, users can also create mapping records in the partner program and deal registration type tables.

</td><td>

Deal registration data viewer \(sn\_prm\_dr.deal\_reg\_data\_viewer\)

</td></tr><tr><td>

Deal registration writer \(sn\_prm\_dr.deal\_reg\_writer\)

</td><td>

This granular role provides users create, write, and edit access to all deal registrations.

</td><td>

Deal registration data viewer \(sn\_prm\_dr.deal\_reg\_data\_viewer\)

</td></tr><tr><td>

Experience \(sn\_prm\_dr.deal\_reg\_ui\)

</td><td>

This role provides granular access to organization staff to provide a consistent experience across all user interfaces.

</td><td>

NA

</td></tr><tr><td>

Approver \(sn\_prm\_dr.deal\_reg\_approver\)

</td><td>

This granular role provides read access to users for the deal registration to which they are added as an approver.

</td><td>

Partner data viewer \(sn\_prm.partner\_data\_viewer\)

</td></tr></tbody>
</table>**Parent Topic:**[Deal Registration](deal-registration-management.md)

