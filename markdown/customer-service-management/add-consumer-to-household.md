---
title: Add consumers to a household
description: Add consumers as members of a household.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring households, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Add consumers to a household

Add consumers as members of a household.

## Before you begin

Role required: One of the following roles:

-   sn\_crm\_consumer\_data\_manager
-   sn\_crm\_household\_data\_manager
-   sn\_crm\_household\_relationship\_data\_manager
-   sn\_crm\_consumer\_relationship\_data\_manager
-   sn\_crm\_foundation\_data\_manager
-   sn\_crm\_foundation\_admin
-   sn\_customerservice\_manager
-   admin

## About this task

You can add existing consumers from the Consumer table to a household.

-   A household can have multiple consumers.
-   A consumer can belong to multiple households. One household can be designated as the primary household for that consumer.

Household member records are added to the Household Member table. When a consumer is added to a household, the consumer is assigned as a unique household member number that begins with the prefix HM.

The Household form includes the following related lists for household members:

-   Current Members: Consumers that belong to the household as of the current date.
-   All Members: Current members and past members. The customer service manager or admin can indicate that a consumer no longer belongs to the household by adding a date to the **End Date** field. A consumer that has left a household can be added back to that household.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Households**.

2.  Select a household.

3.  In the Current Members related list, select **New**.

4.  Add a user from the Consumer table in the **Consumer** field.

    The **Household** field is automatically updated with the household selected in step 2.

5.  If desired, add the date that the consumer was added to the household in the **Start Date** field.

    If the consumer is removed from the household, you can add the **End Date** field.

6.  Select **Submit**.

    The consumer is added to the Current Members related list.

    On the Consumer form for this consumer, the household is added to the following related lists:

    -   Current Households
    -   All Households
    **Note:** You must configure the Consumer form to display these related lists. For more information, see [Configure Service Model Foundation](configure-industry-data-model.md).


