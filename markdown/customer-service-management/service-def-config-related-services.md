---
title: Configure related services for a service definition
description: After creating a service definition, you can associate one or more related services with the service definition. This creates a parent-child relationship between service definitions.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring service definitions, Service definitions, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure related services for a service definition

After creating a service definition, you can associate one or more related services with the service definition. This creates a parent-child relationship between service definitions.

## Before you begin

Role required: sn\_csm\_case\_types.service\_definition\_manager, sn\_csm\_case\_types.service\_definition\_admin, or admin

## About this task

When creating relationships between services on the Service to Service Relationship record, only one relationship between the related service definition and the service definition can exist.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Service Definitions**.

2.  Select a service definition.

3.  In the Service to Service Relationships related list, select **New**.

    The system displays a new Service to Service Relationship record. The **Service definition** field is auto-filled with the name of the selected service definition.

4.  Select a related service in the **Related service definition** field.

    From the Service Definitions pop-up window, you can select the target table in the **Table** field and then select from the list of related services for that table.

    **Note:** You cannot relate the same service to a parent service more than once.

5.  Select **Submit**.

    The related service is added to the to the Service to Service Relationships related list. The **Table** column displays the name of the target table for the related service.


