---
title: Create an account staff relationship
description: Create a relationship between a staff member at a business organization \(formerly business location\) and an account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/create-staff-account-relationship.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business Organizations, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create an account staff relationship

Create a relationship between a staff member at a business organization \(formerly business location\) and an account.

## Before you begin

Role required: admin, sn\_crm\_account\_relationship\_data\_manager, sn\_customerservice\_manager, sn\_customerservice.svc\_location\_manager, sn\_customerservice.svc\_location\_manager\_contributor, and sn\_bus\_loc.location\_relationship\_manager

## About this task

You can assign users who have been added as staff members to a business location to an account relationship.

-   Administrators and customer service managers can assign a staff member from any location.
-   Location managers can assign staff members from the locations that they have access to.

Relationships are based on responsibilities. A responsibility definition describes a role or a function that supports a customer or consumer. To create an account team member relationship, use the Account Manager responsibility.

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Business Organizations** &gt; **Internal/External Organizations**.

2.  Select either an internal or external organization \(formerly internal or external business location\).

3.  In the Account Staff Relationships related list, select **New**.

    This related list shows the accounts that have a relationship with any staff member at that location.

4.  In the **Account** field, select the account to which the staff member is assigned.

5.  In the **Responsibility** field, select **Account Manager**.

6.  In the **User** field, select the staff member to fulfill the responsibility.

7.  Select **Submit**.

    The relationship is added to the Account Staff Relationships related list.


