---
title: Set up payment details for a billing account
description: Set up payment details for a billing account by defining the paying party on the account and adding a payment profile. The paying party settings capture who is responsible for payment; the payment profile records how the account is paid, including the payment method. Payment profiles are stored in the Billing Account Payment Profile table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/add-payment-profile-to-billing-account.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configuring billing accounts, Billing accounts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Set up payment details for a billing account

Set up payment details for a billing account by defining the paying party on the account and adding a payment profile. The paying party settings capture who is responsible for payment; the payment profile records how the account is paid, including the payment method. Payment profiles are stored in the Billing Account Payment Profile table.

## Before you begin

Role required: sn\_billing\_account.crm\_b2b\_writer or sn\_billing\_account.crm\_b2c\_writer, or a role that contains them \(sn\_billing\_account.crm\_data\_manager or sn\_billing\_account.crm\_admin\). The unrestricted billing account roles \(sn\_billing\_account.writer, sn\_billing\_account.data\_manager, sn\_billing\_account.admin\) also apply.

## About this task

A payment profile \[sn\_billing\_account\_payment\_profile\] table defines how a billing account is paid, including the payment method and any related payment details. Together with the paying party settings on the billing account, it captures who is responsible for payment — the account itself, a parent, or another designated billing account. Adding payment profiles helps your organization manage payment responsibility accurately across billing relationships and account hierarchies.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Billing Accounts**.

2.  Select a billing account from the list.

    For more information on how to create a billing account record, see [Install billing account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/install-billing-account.md).

3.  On the billing account form, define the paying party for the account.

<table id="table_ba_pay_party"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Paying party

</td><td>

Identifies the party responsible for paying. The available values are: -   None: No paying party is assigned. This is the default value until you select another option.
-   Self: The billing account pays its own charges. When you select this value, the **Paying billing account** field is set to the current account automatically.
-   Parent: A self-paying account higher in the billing account hierarchy pays the charges.
-   Designated: A billing account that you specify pays the charges. In the **Paying billing account** field, you can select any account of the same billing account type.


</td></tr><tr><td>

Paying billing account

</td><td>

Lists accounts of the matching billing account type \(for example, Customer account\).

</td></tr></tbody>
</table>4.  Select **New** from the Billing Account Payment Profiles related list.

5.  On the form, fill in the fields.

<table id="table_ba_pay_prof"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Payment method

</td><td>

Payment method for the profile. The available values are: -   Invoice: The account is billed by invoice and settles against it.
-   Direct Debit: Payments are collected automatically by direct debit; selecting this value enables **Payment method type** and **Payment reference ID**.


</td></tr><tr><td>

Billing account

</td><td>

Billing account that this payment profile belongs to.

</td></tr><tr><td>

Payment method type

</td><td>

Type of payment method. The available values are Card and Bank transfer. This field is available when Payment method is Direct Debit.

</td></tr><tr><td>

Payment reference ID

</td><td>

Reference identifier for the payment method. This field is available when Payment method is Direct Debit.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the payment profile is active. Selected by default.

</td></tr></tbody>
</table>6.  Select **Submit** to create the billing account payment profile record.


