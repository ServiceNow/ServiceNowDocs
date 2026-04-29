---
title: Customer contract line form
description: You can create customer contract lines in the Customer Contracts and Entitlements application by using the Customer Contract Line form.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer Contracts and Entitlements reference, Reference, Customer Service Management]
---

# Customer contract line form

You can create customer contract lines in the Customer Contracts and Entitlements application by using the Customer Contract Line form.

<table id="table_jtd_tbk_bzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the customer contract line.

</td></tr><tr><td>

Contract

</td><td>

The internal unique identification number that is generated when the customer contract is created. This number isn’t editable.

</td></tr><tr><td>

Parent contract line

</td><td>

The internal unique identification number of the parent customer contract line that is associated with the child customer contract line.

</td></tr><tr><td>

Account

</td><td>

The name of the account associated with this customer contract.**Note:**

-   A customer contract can be associated with either an account or a consumer.
-   An account can be created if no account is found by selecting **New** on the Accounts form. For more information on the fields in the Account form, see [Account form](../../customer-service-management/reference/customer-service-account-form.md).

</td></tr><tr><td>

Location

</td><td>

The customer or installation location.

</td></tr><tr><td>

Product specification

</td><td>

The product specification that is mapped to the sold product.

</td></tr><tr><td>

Number

</td><td>

The internal unique identification number of the customer contract line that is generated when it is created. This number isn’t editable.

</td></tr><tr><td>

Consumer

</td><td>

The name of the consumer associated with this contract.**Note:** If no consumer record is found, you can create a consumer and add it to the customer contract. For more information, see [Create a consumer record](../../customer-service-management/task/create-a-consumer-record.md).

</td></tr><tr><td>

State

</td><td>

The current state of the contract line:-   Draft
-   Active
-   Expired
-   Canceled
-   Suspended

**Note:**

-   The state of the customer contract line is inherited from its parent customer contract.
-   Suspended state is only applicable when the contract line item is created via the Sales and Order Management workflow.

</td></tr><tr><td>

Start date

</td><td>

The date of activation of the customer contract line.

</td></tr><tr><td>

End date

</td><td>

The date when the customer contract line expires.

</td></tr><tr><td>

Product

</td><td>

The product model that is mapped to the product offering for the sold product.

</td></tr><tr><td>

Product offer

</td><td>

The product offering that is mapped to the sold product.

</td></tr><tr><td>

Sold product

</td><td>

The name of the sold product that is added to the contract line.**Note:**

-   When the customer contract line item is created via the Sales and Order Management workflow, this field displays the sold product name from which the contract line is generated.
-   When customer contract lines are created via integration, the field becomes invalid.

</td></tr><tr><td>

Renewal root

</td><td>

A customer contract line can be renewed multiple times. Renewal root refers the customer contract line reference of the first or base customer contract line.

</td></tr><tr><td>

Renewed from

</td><td>

A customer contract line can be renewed multiple times. Renewed from field refers to the previous customer contract line that was renewed.

</td></tr></tbody>
</table>You can see the pricing information on a contract line for subscription contracts that helps you in reviewing your contract information.

<table id="table_j21_txb_tdc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Term \(Months\)

</td><td>

Validity period of having access to the service or product.

</td></tr><tr><td>

Subscription Start Date

</td><td>

Start date of the contract subscription.

</td></tr><tr><td>

Subscription End Date

</td><td>

End date of the contract subscription.

</td></tr><tr><td>

Price List

</td><td>

Price list associated for servicing the product.

</td></tr><tr><td>

Unit net price

</td><td>

The price for each unit within the product offering. The net price of a single unit of the sold product.

</td></tr><tr><td>

Pricing method

</td><td>

The pricing method for the selected sold product. It can be one-time or recurring. One-time pricing charges one fee for the product offering. Recurring pricing lets you set the pricing periodicity.

</td></tr><tr><td>

Periodicity

</td><td>

The frequency of the pricing method. It can be monthly, quarterly, semiannually, or annually.This field becomes valid only when the method in the **Pricing method** field is a recurring payment.

</td></tr><tr><td>

One Time Price

</td><td>

Represents one-time charges to be paid for the product or service.

</td></tr><tr><td>

Monthly Recurring Price

</td><td>

Represents the price that the customer is supposed to pay monthly during usage of the product.

</td></tr><tr><td>

Annual Recurring Price

</td><td>

Represents the price to pay annually during usage of the product.

</td></tr><tr><td>

Cumulative one-time price

</td><td>

Represents one-time charges to be paid for the parent line and all the child line items.

</td></tr><tr><td>

Cumulative monthly recurring price

</td><td>

Represents monthly price for the parent line and all the child line items

</td></tr><tr><td>

Cumulative annual recurring price

</td><td>

Represents annual price for the parent line and all the child line items.

</td></tr><tr><td>

Cumulative net price

</td><td>

Represents the total price of the contract line by calculating the roll-up amount of all root lines.

</td></tr></tbody>
</table>**Note:** When a customer contract line item is created manually, the **Pricing method**, **Unit net price**, and **Periodicity** fields are invalid. They’re only applicable when the contract line is created by the Sales and Order Management workflow or by integration. In that case, these fields are auto-populated with the details from the related sold product. The start and end dates of a child customer contract line must be in between the start and end date of the associated parent customer contract line.

