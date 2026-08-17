---
title: Create a consumer staff relationship
description: Create a relationship between a staff member at a business organization \(formerly business location\) and a consumer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/create-staff-consumer-relationship.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business Organizations, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create a consumer staff relationship

Create a relationship between a staff member at a business organization \(formerly business location\) and a consumer.

## Before you begin

Role required: admin, sn\_crm\_consumer\_relationship\_data\_manager, sn\_customerservice\_manager, sn\_customerservice.svc\_location\_manager, sn\_customerservice.svc\_location\_manager\_contributor, and sn\_bus\_loc.location\_relationship\_manager

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

## About this task

Users who have been added as staff members to a business organization can be assigned a consumer relationship.

-   Administrators and customer service managers can assign a staff member from any location.
-   Location managers can assign staff members from the locations that they have access to.

Relationships are based on responsibilities. A responsibility definition describes a role or a function that supports a customer or consumer. To create a consumer relationship, use the Relationship Manager responsibility.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Business Organizations** &gt; **Internal/External Organizations**.

2.  Select either an internal or external organization \(formerly internal or external business location\).

3.  In the Consumer Staff Relationships related list, select **New**.

    This related list shows the consumers that have a relationship to any staff member for the location.

4.  In the **Consumer** field, select the consumer to which the user is assigned.

5.  In the **Responsibility** field, select the **Relationship Manager** responsibility.

6.  In the **User** field, select the staff member to fulfill the responsibility.

7.  Select **Submit**.

    The relationship is added to the Consumer Staff Relationships related list.


