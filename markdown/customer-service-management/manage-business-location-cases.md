---
title: Create and manage cases for a business location
description: As a staff member with the location agent role, create and manage cases for your business locations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business locations, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Create and manage cases for a business location

As a staff member with the location agent role, create and manage cases for your business locations.

## Before you begin

Role required: admin, sn\_customerservice.svc\_location\_agent, and sn\_customerservice.svc\_location\_manager

## About this task

Staff members with the location agent role can do the following:

-   View information for the customers at their location.
-   Create cases for the accounts, contacts, households, and consumers at their location.
-   Create consumers.
-   Update cases created at their location.

A case belongs to one business location. When a case is created by a location agent or manager, the **Service Organization** field on the Case form is automatically updated with the business location that the agent or manager belongs to. If the case is reassigned, this field is updated to show the new agent or manager.

If the location agent or manager belongs to multiple locations, the **Service Organization** field may be kept empty. When you fill in this field, make your selection carefully because the service organization controls a location agent's access to cases.

The **Service Organization** can be set manually for a new case or changed for an existing case. Changing the **Service Organization** doesn’t change the assigned agent.

Location agents and managers can create cases for business locations without adding an account, contact, or consumer. The location agent or manager who creates the case is added to the **Opened by** field.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Cases** and select **Create New**.

2.  Select the type of case that you want to create.

3.  On the form, fill in the fields.

    For a description of the field values, see [Case form](../reference/r_CustomerServiceCaseForm.md).

4.  Select **Submit**.


**Related topics**  


[Service Model Foundation cases](../reference/industry-data-model-cases.md)

[Assign responsibilities](csm-assign-responsibilities.md)

[Assign roles](configure-data-model-roles.md)

[Create a customer service case](t_CreateACaseFromCustServApp.md)

