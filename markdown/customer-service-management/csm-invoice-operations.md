---
title: Case Management for Invoice Operations
description: The Case Management for Invoice Operations application enables customer service agents to create cases for specific lines from a single invoice or for multiple invoices.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Case Management for Invoice Operations

The Case Management for Invoice Operations application enables customer service agents to create cases for specific lines from a single invoice or for multiple invoices.

![Invoice case page with case details and the activity stream. This page also includes the configurable side panel.](../image/invoice-operations-case-form.png "Invoice case record")

The Case Management for Invoice Operations application includes the [Invoice case type](invoice-ops-installed-components.md#section_rvn_g3d_hdc). This case type provides the ability to reference multiple invoices or invoice lines as case lines on an invoice case record. By using case lines, agents can track multiple issues for the same invoice case and resolve the issues in each case line independently before resolving and closing the invoice case.

Use invoice cases to handle issues such as invoice disputes or requested corrections. With this application, agents can create an invoice case and add the invoices or invoice lines that are being disputed or that must be corrected. Agents can work through the case, create case tasks for other team members as needed, or assign case lines to other agents.

## Benefits of using invoice cases

Businesses can encounter invoice issues for many reasons including price or quantity discrepancies or incorrect products or services. Invoice issues can also result from incorrect customer details such as incorrect billing or shipping locations. The following table provides some examples of these issues and the resulting invoice cases.

|Reason|Case example|
|------|------------|
|Price adjustments|The quantity of items invoiced does not match what was ordered or delivered, leading to either underbilling or overbilling.|
|Price discrepancies|The amount billed does not match the agreed-upon price or contract terms, such as incorrect discounts, tax calculations, or unit prices.|
|Incorrect customer information|The invoice contains errors in the customer's name, address, or billing information, which can affect payment processing.|
|Missing or incorrect items|An invoice includes products or services that were not delivered, or omits items that were delivered but not invoiced.|
|Part number or SKU errors|The part numbers or SKUs listed on the invoice do not match the products that were ordered or delivered, causing confusion or errors in inventory and payment processing.|
|Currency issues|An invoice is issued in the wrong currency or without proper conversion rates, creating discrepancies in the payment amount.|
|Incorrect unit of measure \(UOM\)|The unit of measure \(for example, quantity per box, per meter, per kilogram\) on the invoice is incorrect, causing confusion or errors in pricing and quantity calculations.|
|Dispute on negotiated price, discounts, or promotions|The invoice reflects a different price than what was negotiated, or discounts and promotions are not applied, leading to a dispute over the final amount due.|
|Incorrect invoice number|The invoice number does not follow the correct sequence, leading to accounting or tracking problems.|

## Overview of creating an invoice case

The following table provides an overview of the process for creating an invoice case. For detailed steps, see [Create an invoice case](../task/invoice-ops-create-invoice-case.md).

<table id="table_hpc_lhk_fdc"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Creating an invoice case

</td><td>

An agent can create an invoice case from CSM Configurable Workspace or from the Core UI by selecting **New** from the Invoice Cases list view.

</td></tr><tr><td>

Viewing the invoice case record

</td><td>

After creating an invoice case record, agents can:

-   Add invoices or invoice lines to the case.
-   Delete invoices or invoice lines from the case.
-   Create new invoice case lines.
-   Edit the details of invoice case lines.
-   Assign invoice case lines to themselves.
-   Create tasks for invoice case lines.

</td></tr><tr><td>

Submitting the invoice case record

</td><td>

Selecting **Save** on the Invoice case record moves the invoice case to the Draft state. After reviewing the record details, the agent can select **Submit** on the Invoice case record to move the invoice case and the invoice case lines to the New state. Once in the New state, agents can begin working to resolve the invoice case. This includes creating tasks for invoice case lines, assigning them to other agents or team members, and monitoring case progress.

</td></tr></tbody>
</table>## Case Management for Invoice Operations plugin

Case Management for Invoice Operations \(com.sn\_csm\_invoice\) is a case management application for handling support requests on invoices or invoice lines. This application enables customers to process invoice service requests such as invoice disputes or invoice inquiries.

**Note:** The Case Management for Invoice Operations application has a dependency on the [Case lines and workflows](csm-case-mgmt-case-lines.md) application \(com.sn\_case\_line\).

The Case Management for Invoice Operations application includes list views for CSM Configurable Workspace and Core UI.

-   In CSM Configurable Workspace, expand the **Invoice Cases** list category in the Lists tab.
-   In Core UI, navigate to **All** &gt; **Invoice Case**.

The Case Management for Invoice Operations application also includes tables, roles, service definitions, the Invoice case type, and other components. For more information, see [Components installed with Case Management for Invoice Operations](invoice-ops-installed-components.md).

The Case Management for Invoice Operations application is available from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

