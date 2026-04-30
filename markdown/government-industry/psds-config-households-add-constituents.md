---
title: Add constituents to a household in Public Sector Digital Services
description: Add constituents as members of a household.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-01-13"
reading_time_minutes: 2
breadcrumb: [Configure households, Customer data, Set up your environment, Configure, Public Sector Digital Services \(PSDS\)]
---

# Add constituents to a household in Public Sector Digital Services

Add constituents as members of a household.

## Before you begin

Role required: sn\_customerservice.svc\_location\_manager, sn\_customerservice\_manager, admin

## About this task

You can add existing constituents from the Consumer table to a household.

-   A household can have multiple consumers.
-   A constituent can belong to multiple households. One household can be designated as the primary household for that constituent.

Household member records are added to the Household Member table. When a constituent is added to a household, the constituent is assigned as a unique household member number that begins with the prefix HM.

The Household form includes the following related lists for household members:

-   Current Members: Constituents that belong to the household as of the current date.
-   All Members: Current members and past members. The government service manager or admin can indicate that a constituent no longer belongs to the household by adding a date to the **End Date** field. A constituent that has left a household can be added back to that household.

## Procedure

1.  Navigate to **All** &gt; **Constituent Services** &gt; **Customer** &gt; **Households**.

2.  Select a household.

    For information on how to create a household, see [Create or update a household in Public Sector Digital Services](psds-config-households-create-update.md).

3.  In the Current Members related list, select **New**.

4.  Add a user from the **Consumer** table in the Constituent field.

    For information on how to add a constituent to the **Consumer** table, see Configure constituents. The **Household** field is automatically updated with the household selected in step 2.

5.  If desired, add the date that the constituent was added to the household in the **Start Date** field.

    If the constituent is removed from the household, you can add the **End Date** field.

6.  Select **Submit**.

    The constituent is added to the Current Members related list.

    On the Consumer form for this constituent, the household is added to the following related lists:

    -   Current Households
    -   All Households

## Result

One or more constituents are added to the household entity. You can now create relationships between constituents, as well as create and manage cases for each constituent of the household.

**Related topics**  


[Create a relationship between household members in Public Sector Digital Services](psds-config-households-member-relations.md)

[Create and manage cases for a constituent or household in Public Sector Digital Services](psds-config-households-manage-cases.md)

