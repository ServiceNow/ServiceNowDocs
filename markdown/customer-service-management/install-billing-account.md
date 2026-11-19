---
title: Install billing account
description: You can install the Billing Account Core \(sn\_billing\_account\) application if you have the admin role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/customer-service-management/install-billing-account.html
release: yokohama
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring billing accounts, Billing accounts, Customer data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Install billing account

You can install the Billing Account Core \(sn\_billing\_account\) application if you have the admin role.

## Before you begin

Role required: admin

## About this task

The billing account core application has a modular plugin structure:

-   Base plugin \(sn\_billing\_account\): Independent core functionality for billing account management
-   CSM integration: Install com.sn\_customerservice and com.snc.cs\_base to enable billing account integration with core CSM capabilities and the related party framework

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Customer** &gt; **Billing Accounts**.

2.  Select **New** from the billing accounts record.

3.  Fill the required details on the billing account form.

    For more information, see [Billing Account form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/customer-service-management/billing-account-form.md).

4.  Select **Submit** to create billing account record.


