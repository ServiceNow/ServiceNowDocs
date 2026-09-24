---
title: Associate a location with a billing account
description: Associate one or more locations with a billing account by creating billing account address records. Each billing account address links a billing account to a location and identifies the type of address.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/associate-location-with-billing-account.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring billing accounts, Billing accounts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Associate a location with a billing account

Associate one or more locations with a billing account by creating billing account address records. Each billing account address links a billing account to a location and identifies the type of address.

## Before you begin

Role required: sn\_billing\_account.crm\_b2b\_writer or sn\_billing\_account.crm\_b2c\_writer, or a role that contains \(sn\_billing\_account.crm\_data\_manager or sn\_billing\_account.crm\_admin\). The unrestricted billing account roles \(sn\_billing\_account.writer, sn\_billing\_account.data\_manager, sn\_billing\_account.admin\) also apply.

## About this task

A billing account address \[sn\_billing\_account\_address\] table links a billing account to a location and identifies the type of address using the available location types. Associating locations with a billing account gives you a structured record of where an account operates. You can maintain more than one address per account and mark one as the primary. This keeps address information consistent and reusable across the customer data model.

Verify the following prerequisites are in place:

-   A billing account record exists.
-   The location record that you want to associate with the billing account exists.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Billing Accounts**.

2.  Select a billing account from the list.

    For more information on how to create a billing account record, see [Install billing account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/install-billing-account.md).

3.  Select **New** from the Billing Account Addresses related list.

4.  On the form, fill in the fields.

    |Field|Definition|
    |-----|----------|
    |Billing account|Billing account that this address is associated with.|
    |Location|Location record associated with the billing account. References the Location \(cmn\_location\) table.|
    |Type|Type of address for the billing account. The available values are the configured location types.|
    |Primary|Indicates whether this is the primary address for the billing account.|
    |Active|Indicates whether the billing account address record is active.|

5.  Select **Submit** to create the billing account address record.


