---
title: Entitlement form
description: The Entitlement form can be used to create entitlements in Customer Contracts and Entitlements.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer Contracts and Entitlements reference, Reference, Customer Service Management]
---

# Entitlement form

The Entitlement form can be used to create entitlements in Customer Contracts and Entitlements.

<table id="table_jtd_tbk_bzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the entitlement.

</td></tr><tr><td>

Product

</td><td>

The product associated with the entitlement.

</td></tr><tr><td>

Contract

</td><td>

The internal unique identification number that is generated when the customer contract is created. This number isn’t editable.

</td></tr><tr><td>

Account

</td><td>

The name of the account associated with this contract.**Note:**

-   A customer contract can be associated with either an account or a consumer.
-   An account can be created if no account is found by selecting **New** on the Accounts form. For more information on the fields in the Account form, see [Account form](../../customer-service-management/reference/customer-service-account-form.md).

</td></tr><tr><td>

Location

</td><td>

The service or installation location.

</td></tr><tr><td>

Product specification

</td><td>

The product specification that is mapped to the sold product.**Note:** Configure this field manually on the entitlement form using form layout.

</td></tr><tr><td>

Consumer

</td><td>

The name of the consumer associated with this contract.**Note:** If no consumer record is found, you can create a consumer and add it to the customer contract. For more information, see [Create a consumer record](../../customer-service-management/task/create-a-consumer-record.md).

</td></tr><tr><td>

Customer contract line

</td><td>

The name of the related customer contract line.

</td></tr><tr><td>

State

</td><td>

The current state of the entitlement:-   Draft
-   Active
-   Expired
-   Canceled
-   Suspended

**Note:** The state of the entitlement is inherited from its parent contract line.

</td></tr><tr><td>

Start date

</td><td>

The entitlement activation date.

</td></tr><tr><td>

End date

</td><td>

The date when the entitlement ends.

</td></tr><tr><td>

Sold entitlement

</td><td>

The name of the sold product that is added to the entitlement.**Note:**

-   If the entitlement is created manually, this field remains read-only.
-   The field must have the same state as its related entitlement.
-   The field becomes invalid when entitlements are created via integration.

</td></tr><tr><td>

Product offer

</td><td>

The product offering that is mapped to the order line item.

</td></tr><tr><td>

Renewal root

</td><td>

An entitlement can be renewed multiple times. Renewal root refers the entitlement reference of the first or base service entitlement.

</td></tr><tr><td>

Renewed from

</td><td>

An entitlement can be renewed multiple times. Renewed from field refers to the previous entitlement that was renewed.

</td></tr></tbody>
</table>You can see the pricing information on an entitlement for subscription contracts that helps you in reviewing your contract information.

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
</table>