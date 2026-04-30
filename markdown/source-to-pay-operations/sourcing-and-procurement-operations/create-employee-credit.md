---
title: Create an employee credit
description: Manage and track credits that an employee shopper is allocated to in Shopping Hub, by creating an employee credit. If a credit already exists, allocated to an employee, it shows up as a payment option in Shopping Hub, and is created as a cost allocation entry at the backend.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create an employee credit

Manage and track credits that an employee shopper is allocated to in Shopping Hub, by creating an employee credit. If a credit already exists, allocated to an employee, it shows up as a payment option in Shopping Hub, and is created as a cost allocation entry at the backend.

## Before you begin

Role required: sn\_shop.shopping\_hub\_admin

## About this task

You can create a credit for an employee shopper from Shopping Hub.

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Manage Employee Credits** &gt; **Allocated Credits**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Credit name|The name you assign to an employee credit. This is visible to the shopper who is assigned the credit.|
    |Number|Unique identifier for this credit.|
    |Description|Additional information about the credit. This is visible to the shopper who is assigned the credit.|
    |Allocated to|Search for and select the user who this authorized to shop with this allocated credit.|
    |Responsible cost center|The cost center responsible for the user you selected in the **Allocated to** field. This is auto-populated and read-only.|
    |Amount allocated|The amount of credit a shopper is allocated to spend.|
    |Expiration date|The date after which a credit allocated to a shopper is no longer valid.|
    |Payback options|The number of paycheck periods an employee is allowed to pay back costs in excess of the allocated credit amount.|
    |Restrict Use to Categories|Search for and select the categories for which employee credits can be used to purchase products in the category. You must select a value for either the **Restrict Use to Categories** or **Restrict Use to Products** fields to create the record.|
    |Restrict Use to Products|Search for and select the products for which employee credits can be used to purchase products related to the product model. You must select a value for either the **Restrict Use to Categories** or **Restrict Use to Products** fields to create the record.|
    |Status|Specify the current status of a credit. The options are Pending Purchase, Credit Consumed, and Credit Expired. If you save the status as Credit Consumed or Credit Expired, the form becomes read-only.|
    |Allocated|Specifies how the employee credit was allocated. The options are Manually and By Credit Allocation Rule.|
    |Allocated by|The employee who created and allocated the credit to another employee. This field is required if credit allocation is done manually.|
    |Credit allocation rule|The rule that generated this employee credit. This field is visible only if allocation is done through a credit allocation rule.|

4.  Select **Submit**.


**Parent Topic:**[Using Shopping Hub](../reference/use-shoppinghub-portal.md)

