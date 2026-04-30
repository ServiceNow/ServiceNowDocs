---
title: Telephone allocation
description: Learn about telephone blocks, telephone numbers, and allocating telephone numbers. You can also learn what the benefits and relationships are between them and how you can manage them more effectively.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Inventory number allocation, Exploring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Telephone allocation

Learn about telephone blocks, telephone numbers, and allocating telephone numbers. You can also learn what the benefits and relationships are between them and how you can manage them more effectively.

## Telephone number infrastructure

-   **Telephone block**: A telephone block is a pool of telephone numbers that are allocated to a telco operator by an administrator.
-   **Telephone number**: A telephone number is a unique numerical identifier that is assigned to a telephone line or device for making and receiving telephone calls. You can add, review, and update the list of telephone numbers.
-   **Telephone number allocation**: A telephone number allocation consists of all the telephone numbers that are either allocated or available to allocate to the customer.

To learn more, see [Telephone number inventory management data model](../reference/data_model_of_telephone_number_inventory_management.md).

**Note:**

-   To perform any activity on telephone numbers, ensure that you’re assigned to the inventory number manager \(sn\_inv\_num\_mgmt.inventory\_number\_manager\) role.
-   To create any telephone block, number, or number allocation, ensure that you create the components of the telephone number. To learn more, see [Components of a telephone number](create_components.md).

## Use case of a telephone system

Let's say that a network operator has a large series of numbers that include ported in, third party, owned numbers, and other types of numbers. To manage these numbers, an inventory number manager can create a telephone block. To learn more, see [Create a telephone block](../task/create_telephone_block.md).

Now, a customer that has Voice over Internet Protocol \(VoIP\) or Unified Communication as a Service \(UCaas\)-based services submits a request to the operator for a series of numbers. The requested series of numbers belong to three different areas, countries, or a series of numbers.

To fulfill the earlier scenario, an inventory agent can create a telephone number allocation or create a telephone number for an area or region in a particular block. To learn more, see [Create a telephone number allocation](../task/create_telephone_allocation.md) and [Create a telephone number to an area or region](../task/create_telephone_number.md). This process helps an operator to identify the following issues:

-   Availability of a number by using telephone number allocation
-   Ported-in and ported-out numbers
-   Numbers assigned to a country or to an area

