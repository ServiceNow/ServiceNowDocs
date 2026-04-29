---
title: Create or update a household in Public Sector Digital Services
description: Create or update a household.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure households, Customer data, Set up your environment, Configure, Public Sector Digital Services \(PSDS\)]
---

# Create or update a household in Public Sector Digital Services

Create or update a household.

## Before you begin

Role required: sn\_customerservice.svc\_location\_manager, sn\_customerservice\_manager, admin

## About this task

A household is made up of a group of consumers who live at a common address and share products and services. A household can have a designated head of household and multiple current members. The head of household has access to all the cases and information for the other household members.

A user with the administrator role can create a household. This user can also delete a household. When a household is deleted, the system removes its references and associations—including members, sold products, cases, and work orders—but doesn’t delete the associated entities.

Service Model Foundation uses the household form to store details about a consumer household, including its members, their relationships, and any cases, entitlements, or contracts associated with them.

## Procedure

1.  Navigate to **All** &gt; **Constituent Services** &gt; **Customer** &gt; **Households**.

2.  Select **New** on the Households list.

3.  On the form, fill in the fields.

    For more information on the fields on the Household form, see [Household form](https://www.servicenow.com/docs/access?context=data-model-household-form&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

4.  Select **Submit**.


## Result

The household is added to the Households list. You can add constituents to the household entity, as well as create and manage cases for an entire household.

**Related topics**  


[Add constituents to a household in Public Sector Digital Services](psds-config-households-add-constituents.md)

[Create a relationship between household members in Public Sector Digital Services](psds-config-households-member-relations.md)

[Create and manage cases for a constituent or household in Public Sector Digital Services](psds-config-households-manage-cases.md)

