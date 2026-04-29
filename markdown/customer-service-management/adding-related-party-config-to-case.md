---
title: Create related party configurations
description: Related party configurations define the title of a relationship between an entity and an organization or user. These configurations also enable linking related party types with responsibility definitions to grant access as needed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring customer access management, User management, Set up your environment, Configure, Customer Service Management]
---

# Create related party configurations

Related party configurations define the title of a relationship between an entity and an organization or user. These configurations also enable linking related party types with responsibility definitions to grant access as needed.

## Before you begin

Role required: One of the following roles:

-   sn\_crm\_customer\_access\_management\_admin
-   sn\_crm\_foundation\_admin
-   admin

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Related Party Configuration**.

2.  To create a related party configuration, select **New**.

3.  On the form, fill in the fields.

<table id="table_esz_qdw_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Related party configuration type.

</td></tr><tr><td>

Applies To

</td><td>

Table assigned with the related party configuration.

</td></tr><tr><td>

Entity Type

</td><td>

Entity type such as an account, a consumer, or a product.

</td></tr><tr><td>

Reference Condition

</td><td>

Filter condition for defining the related party configuration. In the **Reference Condition** field, you can select **Add Filter Condition** or **Add "Or" Clause**.

</td></tr><tr><td>

Default Responsibility

</td><td>

Access level to different entities and the related information.**Note:** Whenever a related party record is created, the **Responsibility** field gets auto-populated from the default responsibility associated with the selected party type​.

</td></tr><tr><td>

Default Order

</td><td>

Numerical value given to establish the priority of the relationship.**Note:** Whenever a related party record is created, the **Order** field gets auto-populated from the default order associated with the selected party type​.

</td></tr></tbody>
</table>4.  Select **Submit**.


