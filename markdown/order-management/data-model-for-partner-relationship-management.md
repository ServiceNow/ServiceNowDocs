---
title: Data model for Partner Relationship Management
description: The Partner Relationship Management data model provides a framework to map the relationship between channel partners and programs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/data-model-for-partner-relationship-management.html
release: australia
topic_type: concept
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
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



</td><td>

-   Enterprise admin \(sn\_prm.enterprise\_partner\_admin\)
-   Channel partner writer \(sn\_prm.channel\_partner\_writer\)

</td><td>

Manage information related to channel partners.

</td></tr><tr><td>



</td><td>

-   Enterprise admin \(sn\_prm.enterprise\_partner\_admin\)
-   Partner program writer \(sn\_prm.partner\_program\_writer\)

</td><td>

Enable channel partners to participate in structured programs to build customer relationships.

</td></tr><tr><td>



</td><td>

-   Enterprise admin \(sn\_prm.enterprise\_partner\_admin\)
-   Partner program relationship writer \(sn\_prm.partner\_program\_rel\_writer\)

</td><td>

Establish a relationship between channel partners and partner programs.

</td></tr></tbody>
</table>**Parent Topic:**[Configure Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/configure-partner-relationship-management.md)

**Related topics**  


[Install Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/install-partner-relationship-management.md)

[Roles and components of Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/roles-and-components-of-partner-relationship-management.md)

