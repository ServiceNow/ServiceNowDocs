---
title: Payment method options
description: As a shopper, you have the option to pay using one of your preferred payment methods or use another cost center. You even have the option to pay using multiple cost centers for the various products in your cart.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Select a payment method, Complete your checkout, Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Payment method options

As a shopper, you have the option to pay using one of your preferred payment methods or use another cost center. You even have the option to pay using multiple cost centers for the various products in your cart.

If you have credits allocated to you for a particular good or service, those credits are applied here. You can pay the remaining balance, if applicable, from your future paychecks.

You can use the toggle feature between entire purchase and product to specify if the payment method applies to the entire purchase or to individual products. This toggle is conditionally displayed based on predefined criteria. For example, if there is only a single item in your cart, the toggle feature does not apply and is therefore not displayed.

While you can always go with your default payment method that is preselected at the backend for faster checkout, the following options are also available:

-   **Use another cost center**: Allows you to create a new payment method by searching for and selecting another cost center. Select the **Save this cost center for future use** check box if you want to view it in your preferred payment methods list for any subsequent purchases. A new record is created in the backend in the sn\_shop\_payment\_method table with the preferred tag against this record.
-   **Pay with multiple cost centers**: Allows you to add another cost center for making your payment. Adding a new cost center automatically sets the payment percentage to 99% for the first cost center and 1% for the newly added one. You can update the percentage for both, but the total needs to add up to 100% for you to proceed to the next step. To revert to a single cost center for payment, you can either select **Pay with one cost center** or manually delete the newly added cost center rows and update the percentage.
-   Pay using credits: Allows you to use your allocated credits for specified products and services. The credits available for purchase towards the individual products are displayed accordingly. The estimated total and the amount you pay are automatically calculated by the system and displayed in the Summary section. Shipping and tax costs are excluded for both you pay and credit purchase calculations. For more information on employee credits and how to use them, see [Shop with employee credits](../task/shop-employee-credits.md).
-   Pay using paychecks: Allows you to pay the remaining amount, after optimum credit consumption, through equal deductions from your future paychecks. You can choose from the list of available paycheck options and accept the terms and conditions for paycheck payments to proceed to the next step.

**Parent Topic:**[Select a payment method](../task/select-payment-method.md)

