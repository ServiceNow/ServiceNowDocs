---
title: Complete the Payment Provider Configuration
description: Fill out the information in the Payment Provider Configuration table to connect your payment provider information to your ServiceNow instance.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Conversational Integration with Apple Messages for Business, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Complete the Payment Provider Configuration

Fill out the information in the Payment Provider Configuration table to connect your payment provider information to your ServiceNow® instance.

## Before you begin

Role required: admin

## About this task

Each payment provider has their own procedures for certification, or configuration of your merchant profile. Refer to the payment provider's documentation for more details.

## Procedure

1.  Navigate to `sn_va_payment_ctrl_payment_provider_configuration.list`.

2.  On the form, fill in the fields.

    All information must match the information you have input with the payment provider.

<table id="table_rbt_m52_3xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the payment provider.For example: Apple Pay, Google Pay, Stripe

</td></tr><tr><td>

Merchant Name

</td><td>

Your merchant name from your payment provider.

</td></tr><tr><td>

Merchant Identifier

</td><td>

Your merchant id from your payment provider.

</td></tr><tr><td>

Payment Gateway URL

</td><td>

The URL for the payment gateway you host which processes the customer credit card details.

</td></tr><tr><td>

Merchant Capabilities

</td><td>

The types of payment you can accept. For example: Debit, credit, 3DS

</td></tr><tr><td>

Supported Networks

</td><td>

The types of credit cards supported by the payment provider.For example: Mastercard, Visa, American Express

</td></tr><tr><td>

Protocol Profile

</td><td>

The name of the profile you have configured for processing payments.

</td></tr><tr><td>

Order Tracking URL

</td><td>

The URL that the user can access to track their order.

</td></tr><tr><td>

Shipping Contact Update URL

</td><td>

This URL allows the user to update their shipping contact information.

</td></tr><tr><td>

Fallback URL

</td><td>

An alternate URL to allow the user to access the order information.

</td></tr><tr><td>

Payment Method Update URL

</td><td>

This URL allows the user to update their payment method preference.

</td></tr><tr><td>

Supported Countries

</td><td>

Countries that you sell to.

</td></tr><tr><td>

Shipping Method Update URL

</td><td>

This URL allows the user to update their shipping method preference.

</td></tr></tbody>
</table>3.  Click **Update**.


