---
title: Create customer accounts
description: An account is a supported external customer. Use the Customer Service Management application to create account records.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure accounts and contacts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Create customer accounts

An account is a supported external customer. Use the Customer Service Management application to create account records.

## Before you begin

Role required: sn\_customerservice\_manager or admin

## About this task

There are two types of accounts: customer accounts and partner accounts. The **Customer** and **Partner** fields on the Account form denote the account type. An account can be a customer account, a partner account, or both.

A partner is a supported external customer that sells to and supports other customers. A partner can report and manage cases on behalf of customers. A partner can also be a customer.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** and select one of the following actions:

    -   To create a customer account, select **Accounts**.
    -   To create a partner account, select **Partners**.
2.  Select **New** and fill in the fields on the [Account form](../reference/customer-service-account-form.md).

    When a new customer account record is created, the system uses the **com.snc.cs\_base.last.generated.code.tree.path** system property to determine a unique account code value for the account. The property is updated with the latest value to confirm the next account record receives a unique account code.

    **Note:** If the property is reset to its original value, the system might attempt to create accounts using already assigned account codes, which can result in an invalid insert.

3.  Select **Submit**.


