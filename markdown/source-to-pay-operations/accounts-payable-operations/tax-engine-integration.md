---
title: Tax Engine Integration
description: Integrate an external tax engine to validate supplier-provided taxes against calculated from external tax engines resulting in accurate, compliant, straight through processing and improving efficiency.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Tax Engine Integration

Integrate an external tax engine to validate supplier-provided taxes against calculated from external tax engines resulting in accurate, compliant, straight through processing and improving efficiency.

The Accounts Payable invoice processing invokes the external tax engine to validate supplier tax \(based on ship to, item, service, category, amounts, jurisdiction, exemptions, other tax configuration\) against system tax and drive straight through processing for matching outcomes. During invoice data extraction, the tax rate and tax amount will be stored as supplier tax rate and supplier tax amount at both header and invoice line levels. Tax integration is applicable for invoices of type PO, Non-PO and credit memo; supporting automatic, manual, and scheduled tax validation ensuring taxes remain correct even when invoices change or temporary integration issues occur.

How system tax is calculated-When invoice data is submitted to the external tax engine, the system receives the calculated tax amounts based on the invoice details and configuration. The system uses this response to automatically generate tax lines. The generated tax lines are then validated against the supplier-provided taxes at the header and line levels.

Tax integration is triggered for invoices:

-   For Non- PO invoices, after the invoice state is changed to accepted state.
-   For PO invoices, after the PO matching state is completed.

## Key capabilities

-   External tax engine integration- Connects to enterprise tax engines using integration framework.
-   Intelligent tax calculation- System validates supplier tax against system tax using invoice fields \(based on ship to, item, service, amounts, jurisdiction, exemptions, customer tax configuration\).
-   Granular comparison logic-
    -   Line-level and Header-level validation- The extracted values are stored as it is and the system compares tax at the invoice line item and header level for maximum accuracy.
    -   Configurable tolerance-Define acceptable variance thresholds. The system auto-approves tax when the variance is within the configurable tolerance.
    -   Scheduler based re-calculation- The scheduler will automatically reinitiate the tax integration process for invoices with tax status of integration error, or recalculate tax.

## Benefits of Tax Engine integration

Customers using tax engine integration benefit from:

-   Reduced manual effort – Automatic tax calculation and reconciliation removes the need for manual tax line entry.
-   Improved accuracy – Taxes are calculated using authoritative third‑party tax logic.
-   Stronger compliance – Consistent validation across jurisdictions and invoice types.
-   Faster invoice processing – Higher straight‑through processing rates and fewer exceptions.
-   Clear exception visibility – Over‑tax and under‑tax variances are surfaced at line and header levels.

## Tax calculation framework

The tax calculation framework is structured as a modular, three-tier architecture to promote scalability, maintainability, and extensibility. The framework seamlessly integrates Accounts Payable Operations and the external Tax engine, enabling automated and coordinated tax computation. The validation logic is applied at:

-   Line‑level and Header-level comparison \(primary\)- Supplier tax and system tax are compared at the invoice line level and header level for maximum accuracy.
-   Configurable tolerance-Customers can define acceptable variance thresholds. Invoices within tolerance are automatically approved.

<table id="table_abq_srt_j3c"><thead><tr><th>

Components

</th><th>

Key functions

</th></tr></thead><tbody><tr><td>

The Accounts Payable Operations serves as entry point for tax calculation. When an invoice is in PO matching or accepted state in the Accounts Payable Operations, the system determines if tax calculation is required or not.

</td><td>

-   If tax calculation is required, then a record is created in the tax staging table \[sn\_spend\_intg\_tax\_staging\], and the tax status is set to in progress. For more information on tax status, see [Tax status](../reference/tax-status.md)
-   If tax calculation isn’t required, then the invoice processing continues through the regular exception flow and proceeds to payment.

</td></tr><tr><td>

The Source-to-Pay integration framework is a processing layer between Accounts Payable Operations and the external tax engine.

</td><td>

-   The vendor defines the data mapping required by the external tax engine.
-   Mapping tables are used during request creation \(outbound\) and response processing \(inbound\) between APO attributes and Accounts Payable Operations.
-   Responses from the tax engine are sent back to the staging table.
-   Invoice tax status is updated based on the response.
-   Failed records are processed manually. For more information on the tables, see [Configuration tables and prerequisites for Tax integration](config-tax-integ.md).

</td></tr><tr><td>

The external tax engine computes the tax.

</td><td>

Calculates the tax and returns the response. The response is processed, tax lines are created automatically for the applicable invoice in Accounts Payable Operations. The system triggers exception engine based on the response from tax engine. Tax exception is raised when supplier tax and system tax mismatch in the invoice. Invoice tax status is set to integration error and Accounts Payable specialist investigates the case manually. If the invoice is modified after last execution \(change amounts, add lines or adjust tax codes\), then the tax is recalculated. The tax processing is re-initiated. Upon successful validation, the invoice processing proceeds to payment.

</td></tr></tbody>
</table>## Tax validation modes

Tax calculation and validation can be triggered in multiple ways:

-   Automatic \(synchronous\)-Runs automatically at key invoice processing milestones
-   Manual \(on-demand\)-AP specialists can trigger tax validation during invoice exception review. This is applicable or accessible from the tax exception
-   Scheduler re-calculation-Background jobs automatically re‑initiate tax validation for invoices that are in progress, or recalculate tax status and integration error status. This ensures taxes stay accurate even if invoice data is updated or external calls fail temporarily.

## Tax integration workflow

A high level workflow of how tax integration works in Accounts Payable Operations is shown below.

![Tax integration workflow](../image/tax-integ-workflow.png)

**Note:** If you're upgrading from previous version of APO to latest version, you must execute the scheduled job \[APO - close open exception for deactivated exception definition\]. This scheduled job updates the status of invoice exceptions to inactive and closes the corresponding invoice exceptions.

