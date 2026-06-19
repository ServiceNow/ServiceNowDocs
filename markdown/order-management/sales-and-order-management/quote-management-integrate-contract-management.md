---
title: Integrate with Contract Management Pro
description: With the integration of Quote Management and Contract Management Pro, sales agents can initiate contract requests while finalizing a deal and formalizing agreements between you and your customers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/sales-and-order-management/quote-management-integrate-contract-management.html
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Quote management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Integrate with Contract Management Pro

With the integration of Quote Management and Contract Management Pro, sales agents can initiate contract requests while finalizing a deal and formalizing agreements between you and your customers.

## Before you begin

Role required: admin

## About this task

Manually run fix scripts if you have not installed the demo data at the time of installation. For more information on how to run the script see [Run fix scripts to update Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/run-fix-scripts-update-contract-management-pro.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for Contract Management for Sales and Order Management \(Quote Management with Contract Management Pro\) plugin \(com.sn\_som\_clm\).

    **Note:** To activate this plugin, there’s a dependency on the Contracts core plugin \(com.sn\_cm\_core\). Verify that it’s installed to use the contract creation workflow from a quote.

3.  Select **Activate**.

4.  Complete the initial configuration steps to set up this integration.

    For more information on setting up Contract Management Pro, see .


## What to do next

To learn more, see  and [Initiate a contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/order-management/sales-and-order-management/quote-management-create-contract.md).

