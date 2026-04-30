---
title: Case lines and workflows
description: The Case lines and workflows application provides the ability to reference multiple line items on a case record. Agents can use these line items to capture, track, and resolve multiple related issues in a single case.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-09-16"
reading_time_minutes: 2
breadcrumb: [Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Case lines and workflows

The Case lines and workflows application provides the ability to reference multiple line items on a case record. Agents can use these line items to capture, track, and resolve multiple related issues in a single case.

The Case lines and workflows application provides the framework for a case type to handle multiple related issues. One example is the Orders case type available with the [Order Operations Case Management application](csm-case-mgmt-order-ops.md). This case type enables agents to create cases with case line items for multiple orders or for multiple order lines within a single order.

Case line items enable agents to track multiple issues for the same case. Agents can resolve these different issues, represented by case line items, independently before resolving and closing the case. Agents can take different actions on different case line items depending on the need.

This application supports different types of line items based on the source of the case. These line items can include entities such as orders or order lines, invoices or invoices lines, contracts, and sold products. Each case line item maps to an entity line \(for example, an order line\) and has its own resolution process.

## Benefits of using case line items

Using the Case lines and workflows application provides the following benefits:

-   Identify when an order cannot be filled completely and recommend alternative items.
-   Process inflight order changes and customer-initiated changes, such as changes to items, quantities, or requested ship dates.
-   Process order exceptions and manage the approval and fulfillment process.
-   Manage suppliers by creating supplier cases for order-related questions, such as increasing or decreasing quantity, quality issues, or status tracking.

## Case lines and workflows plugin

The Case lines and workflows application \(com.sn\_case\_line\) enables the Case table to store multiple line items on a case record. These line items are product instances and can be extended for various entities such as orders, order lines, invoices, invoice lines, and contracts.

The case lines and workflows application includes a Case Line Items list view in the Core UI. To access the Case Line Items list, navigate to **All** &gt; **Customer Service** &gt; **Cases** &gt; **All Line Items**.

The Case lines and workflows application application also includes tables and roles. For more information, see [Components installed with Case lines and workflows](../reference/csm-case-mgmt-case-lines-install-comp.md).

The Case lines and workflows application is available from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Related topics**  


[Order case pages](csm-case-mgmt-order-ops-case-page.md)

