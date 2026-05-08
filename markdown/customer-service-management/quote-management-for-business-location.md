---
title: Quote management for business organization
description: Integrate Service Model Foundation with Quote Management for business organizations to streamline operations and optimize the end-to-end life cycle for quote management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Integration with Sales Customer Relationship Management, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Quote management for business organization

Integrate Service Model Foundation with Quote Management for business organizations to streamline operations and optimize the end-to-end life cycle for quote management.

## Overview of quote management for business organization

Quote Management for business organizations enables sales agents and business organization staff to efficiently create and manage the end-to-end life cycle of quotes on behalf of customers.

Use the Quote Management Business Organization plugin \(com.snc.business\_organization\_qm\) to perform the following actions.

-   Create quotes for customers through channel partners
-   Modify and manage quotes for the business organization
-   Track seller and buyer details of the quote

## Data model

The Quote Management application is integrated with the product offering catalog to help sales agents build quotes easily and conveniently.

The Quote Management Customer Order Related Party table contains the following fields.

<table id="table_dkv_4h5_vfc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Type

</th></tr></thead><tbody><tr><td>

Customer quote

</td><td>

Customer quote that the related party can access.

</td><td>

Reference

</td></tr><tr><td>

Type

</td><td>

Type of related party.

</td><td>

Reference

</td></tr><tr><td>

Responsibility

</td><td>

Responsibility associated with the related party.**Note:** The default responsibility is set to **default\_responsibility**.

</td><td>

Reference

</td></tr><tr><td>

Channel partner

</td><td>

Channel partner whose members can access the quote when added as a related party.

</td><td>

Reference

</td></tr><tr><td>

Class

</td><td>

Class of the record.

</td><td>

sys\_class\_name

</td></tr><tr><td>

Domain

</td><td>

Domain of the related party record.

</td><td>

Domain ID

</td></tr><tr><td>

Active

</td><td>

State of the record, whether active or inactive.

</td><td>

Boolean

</td></tr></tbody>
</table>**Related topics**  


[Roles and responsibilities](personas-roles-and-tables-post-integration.md)

[Activate Quote Management for Business Locations](../task/activate-quote-management-for-business-locations.md)

