---
title: Configuration linking overview
description: Learn how configuration IDs link Configuration Line Items and quote lines in Salesforce. When a configuration is saved, all related line items share the same configuration ID. The same ID is added to the parent quote line when the quote is saved, allowing admins to easily pull configuration details into quotes or related records.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configuration linking overview

Learn how configuration IDs link Configuration Line Items and quote lines in Salesforce. When a configuration is saved, all related line items share the same configuration ID. The same ID is added to the parent quote line when the quote is saved, allowing admins to easily pull configuration details into quotes or related records.

Whenever a configuration session is saved, a collection of Configuration Line Item objects are created in SFDC that all share the same Configuration Id field.

![Quote line details](../images/cpq-salesforce-configuration-id-1.png)

When you save the quote, the quote line for the parent level configurable product will have a similar Configuration Id field, which should be populated with the same value.

![Quote line details](../images/cpq-salesforce-configuration-id-2.png)

A Salesforce admin can leverage the fact that these values match to pull information from the Configuration Line Items to the quote \(or its associated opportunity/account\). For more information about pulling information to the quote line, see:

-   [Use case: Configuration line item to quote line flow](use-case-configuration-line-item-to-quote-line-flow.md) \(if your Logik Extension for Salesforce CPQ Package is version 1.8 or later\)
-   [Use case: Using the Salesforce Quote Calculator plugin to integrate data from ServiceNow CPQ to Salesforce quotes and quote lines](integrate_config_data_from_productlist_extended_to_salesforce_quote_and_quote_lines_using_quote_calculator_pluginqcp.md) \(for CPQ Extension Package version 1.7 or earlier\)

