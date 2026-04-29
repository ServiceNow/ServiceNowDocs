---
title: Configure customer criteria for a service definition
description: After creating a service definition, configure customer-specific criteria to determine which customers are eligible for that service.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring service definitions, Service definitions, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure customer criteria for a service definition

After creating a service definition, configure customer-specific criteria to determine which customers are eligible for that service.

## Before you begin

Role required: sn\_csm\_case\_types.service\_definition\_manager, sn\_csm\_case\_types.service\_definition\_admin, or admin

## About this task

You can associate customer-specific criteria such as location, customer level, or related entities with a service definition that determine which customers are eligible to receive that service.

For example, you can configure customer criteria for service definitions like Free Delivery or Free Installation so that only customers who are loyalty members are eligible to receive these services.

You can associate several criteria, or conditions, with a single service definition. Customers need to match only one of these conditions to have access to the service.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions**.

2.  Select a service definition.

3.  In the Service Definition Customer Criteria related list, select **New**.

    The system displays a new Service Definition Customer Criteria record. The **Service definition** field is auto-filled with the name of the selected service definition.

4.  In the **Customer criteria** field, select a customer criteria record.

    These records are stored in the Entity Criteria \[sn\_req\_criteria\_customer\_condition\] table.

    You can also create a customer criteria record by selecting **New** on the Entity Criteria pop-up window and filling in the fields on the Entity Criteria form.

    For more information, see [Create entity criteria](create-new-entity-criteria.md).

5.  Enable the **Active** check box.

6.  Select **Submit**.


