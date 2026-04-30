---
title: Create a credit allocation rule
description: Assign an amount of credit that an employee shopper can use in Shopping Hub, by creating a condition-based allocation rule.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Shopping Hub, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create a credit allocation rule

Assign an amount of credit that an employee shopper can use in Shopping Hub, by creating a condition-based allocation rule.

## Before you begin

Role required: sn\_shop.shopping\_hub\_admin

To create a credit allocation rule, you must have already created some credits to be assigned to employee shoppers. For more information, see [Create an employee credit](create-employee-credit.md).

## About this task

You can create a condition-based credit allocation rule for an employee shopper from Shopping Hub.

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Manage Employee Credits** &gt; **Credit Allocation Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Credit name|The name you assign to an employee credit. This is visible to the shopper who is assigned the credit.|
    |Active|Option to decide if employee credits are to be created for this rule.|
    |Description|Additional information about the credit. This is visible to the shopper who is assigned the credit.|
    |One time credit|Option to decide if credits are to be assigned just once to employees that meet the conditions of this rule.|
    |Amount allocated|The amount of credit a shopper is allocated to spend.|
    |Credit expires after|The amount of time a credit remains active for a shopper to use.|
    |Allocation based on|Specify the conditions that determine if credits are to be assigned automatically. The options are Inventory Asset and User.|
    |Specify asset conditions|Specify the conditions that must be met for a credit to be created. This field is visible only if you select Inventory Asset in the **Allocation based on** field.|
    |Specify user conditions|Specify the conditions that must be met for a credit to be created. This field is visible only if you select User in the **Allocation based on** field.|
    |Payback options|The number of paycheck periods an employee is allowed to pay back costs in excess of the allocated credit amount.|
    |Restrict Use to Categories|Search for and select the categories for which employee credits can be used to purchase products in the category. You must select a value for either the **Restrict Use to Categories** or **Restrict Use to Products** fields to create the record.|
    |Restrict Use to Products|Search for and select the products for which employee credits can be used to purchase products related to the product model. You must select a value for either the **Restrict Use to Categories** or **Restrict Use to Products** fields to create the record.|

4.  Select **Submit**.


## What to do next

Use the related list of the credit allocation rule form to view the employee credits associated with this rule.

**Parent Topic:**[Using Shopping Hub](../reference/use-shoppinghub-portal.md)

