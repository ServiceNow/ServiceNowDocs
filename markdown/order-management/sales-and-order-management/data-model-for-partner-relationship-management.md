---
title: Data model for Partner Relationship Management
description: The Partner Relationship Management data model provides a framework to map the relationship between channel partners and programs.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Data model for Partner Relationship Management

The Partner Relationship Management data model provides a framework to map the relationship between channel partners and programs.

Add data in the Channel Partner \[sn\_prm\_channel\_partner\] and Partner Program \[sn\_prm\_partner\_program\] tables and create a relationship between the two tables in the Partner Program relationship \[sn\_prm\_partner\_program sn\_prm\_partner\_program\_relationship\] table.

<table id="table_rfz_1fw_1fc"><thead><tr><th>

Task

</th><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Configure Channel Partner table](../task/configure-channel-partner-table.md)

</td><td>

-   Enterprise admin \(sn\_prm.enterprise\_partner\_admin\)
-   Channel partner writer \(sn\_prm.channel\_partner\_writer\)

</td><td>

Manage information related to channel partners.

</td></tr><tr><td>

[Configure Partner Program table](../task/configure-partner-program-table.md)

</td><td>

-   Enterprise admin \(sn\_prm.enterprise\_partner\_admin\)
-   Partner program writer \(sn\_prm.partner\_program\_writer\)

</td><td>

Enable channel partners to participate in structured programs to build customer relationships.

</td></tr><tr><td>

[Configure Partner Program Relationship table](../task/configure-partner-program-relationship-table.md)

</td><td>

-   Enterprise admin \(sn\_prm.enterprise\_partner\_admin\)
-   Partner program relationship writer \(sn\_prm.partner\_program\_rel\_writer\)

</td><td>

Establish a relationship between channel partners and partner programs.

</td></tr><tr><td>

[Configure Program Segment Mapping](../task/configure-program-segment-mapping.md)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

[Configure Program Segment Criteria](../task/configure-program-segment-criteria.md)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

[Configure Program Criteria](../task/configure-program-criteria.md)

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>-   **[Configure Channel Partner table](../task/configure-channel-partner-table.md)**  
With the Partner Relationship Management application, you can use the channel partner \[sn\_prm\_channel\_partner\] table to manage and store information related to channel partners.
-   **[Configure Partner Program table](../task/configure-partner-program-table.md)**  
With the Partner Relationship Management application, enable channel partners to participate in structured initiatives designed to drive revenue, enhance market reach, and build customer relationships by using the Partner Program \[sn\_prm\_partner\_program\] table.
-   **[Configure Partner Program Relationship table](../task/configure-partner-program-relationship-table.md)**  
With the Partner Relationship Management application, you can establish a relationship between channel partners and partner programs.
-   **[Configure Program Segment Mapping](../task/configure-program-segment-mapping.md)**  
Establish a mapping between a program and a segment on the program segment mapping \(sn\_prm\_program\_segment\_mapping\) table to determine which segment belongs to which partner program.
-   **[Configure Program Segment Criteria](../task/configure-program-segment-criteria.md)**  
Create records in the program segment criteria \(sn\_prm\_program\_segment\_criteria\) table based on different records on the entity criteria \(sn\_req\_criteria\_customer\_condition\) table and segments.
-   **[Configure Program Criteria](../task/configure-program-criteria.md)**  
Establish a mapping between the partner program \(sn\_prm\_partner\_program\_relationship\) table and the entity criteria \(sn\_req\_criteria\_customer\_condition\) table.

**Parent Topic:**[Configure Partner Relationship Management](configure-partner-relationship-management.md)

**Related topics**  


[Install Partner Relationship Management](../task/install-partner-relationship-management.md)

[Roles and components of Partner Relationship Management](roles-and-components-of-partner-relationship-management.md)

