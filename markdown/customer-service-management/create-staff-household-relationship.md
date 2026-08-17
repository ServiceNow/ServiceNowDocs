---
title: Create a household staff relationship
description: Create a relationship between a staff member at a business organization \(formerly business location\) and a household.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/create-staff-household-relationship.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business Organizations, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create a household staff relationship

Create a relationship between a staff member at a business organization \(formerly business location\) and a household.

## Before you begin

Role required: admin, sn\_crm\_household\_relationship\_data\_manager, sn\_customerservice\_manager, sn\_customerservice.svc\_location\_manager, sn\_customerservice.svc\_location\_manager\_contributor, and sn\_bus\_loc.location\_relationship\_manager

## About this task

Users who have been added as staff members to a business organization \(formerly business location\) can be assigned a household relationship.

Relationships are based on responsibilities. A responsibility definition describes a role or a function that supports a customer or consumer. To create a household relationship, use the Relationship Manager responsibility.

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Business Organizations** &gt; **Internal/External Organizations**.

2.  Select either an internal or an external organization \(formerly internal or an external business location\).

3.  In the Household Staff Relationships related list, select **New**.

    This related list shows the households that have a relationship to any staff member for the location.

4.  In the **Household** field, select the consumer to which the user is assigned.

5.  In the **Responsibility** field, select the **Relationship Manager** responsibility.

6.  In the **User** field, select the staff member to fulfill the responsibility.

7.  Select **Submit**.

    The relationship is added to the Household Staff Relationships related list.


