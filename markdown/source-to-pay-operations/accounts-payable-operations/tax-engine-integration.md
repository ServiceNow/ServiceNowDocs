---
title: Tax engine integration
description: Integrate an external tax engine to validate supplier taxes and enable accurate, conforming straight-through processing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/accounts-payable-operations/tax-engine-integration.html
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [APO, Tax Engine Integration, Accounts Payable invoice, Accounts Payable Operation, Tax Calculation, System tax]
breadcrumb: [Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Tax engine integration

Integrate an external tax engine to validate supplier taxes and enable accurate, conforming straight-through processing.

Invoice processing invokes the external tax engine to validate supplier tax against system tax. Supplier tax factors include ship-to location, item, service, category, amounts, jurisdiction, exemptions, and other tax configuration. Matching outcomes drive straight-through processing.

During invoice data extraction, the tax rate and tax amount are stored as supplier tax rate and supplier tax amount at both header and line levels.

Tax integration applies to PO, Non-PO, and credit memo invoices. It supports automatic, manual, and scheduled tax validation, keeping taxes correct when invoices change or temporary integration issues occur.

The Vertex tax integration \(sn\_fsc\_vertex plugin\) connects the invoice tax verification process to the Vertex tax system, calculates the jurisdiction aware tax on buyer invoices automatically. The calculated tax is written back to the invoice staging record.

## How system tax is calculated

System tax can be handled either through an external tax engine such as Vertex or manually by the AP specialist using tax lines.

External Tax System \(Vertex\)

When Vertex tax system integration is enabled, the system:

-   Sends invoice line-item details \(amount, line description\) to Vertex's tax determination engine
-   Passes relevant tax context \(supplier name, address, bill-to location, ship-to location, transaction type\)
-   Receives calculated tax amounts back based on jurisdictional rules, exemptions, and tax codes
-   Stores the Vertex response in the same tax staging table and process
-   Automatically populates the tax lines in the invoice with Vertex-determined amounts

Manual Tax Calculation Path \(AP Specialist\)

When Vertex is unavailable, disabled, or not applicable the AP specialist:

-   Reviews the invoice line items and determines applicable tax rates manually
-   Enters tax lines directly into the invoice \(tax amount, tax rate, jurisdiction\) via the APO UI

Example: A supplier sends an invoice with a sales tax amount for each line item. During invoice processing, the AP specialist must validate the supplier-declared tax by comparing it against the system-calculated tax. The system tax is calculated at the invoice line and header levels through internal tax lines. These tax lines are created either through integration with an external tax system \(such as Vertex, when enabled\) or manually by the AP specialist. The individual tax lines roll up to create system tax amounts at the invoice line or header level. The rolled-up system tax is then validated against the supplier-declared tax amount shown on the invoice line.

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
-   Stronger conformance – Consistent validation across jurisdictions and invoice types.
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

The Accounts Payable Operations serves as entry point for tax calculation. When an invoice is in PO matching or accepted state in the Accounts Payable Operations, the system determines if tax calculation from external tax system is required or not.

</td><td>

-   If tax calculation from external tax system is required, a record is created in the tax staging table \[sn\_spend\_intg\_tax\_staging\]. The tax status is set to in progress. For more information on tax status, see [Tax status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/tax-status.md)
-   If tax calculation isn’t required from external tax system, then the invoice processing continues through the regular exception flow and proceeds to approval or payment.

</td></tr><tr><td>

The Source-to-Pay integration framework is a processing layer between Accounts Payable Operations and the external tax engine.

</td><td>

-   The out-of-the-box \(OOTB\) data mapping for the Vertex tax engine is available. Review and identify any configuration changes required. For alternative tax engines, specify the corresponding field mapping and verify format alignment.
-   Mapping tables are used during request creation \(outbound\) and response processing \(inbound\) between APO attributes and external tax system fields.
-   Responses from the tax engine stored in the same staging table.
-   Invoice tax status is updated based on the response.
-   Failed records are processed manually. For more information on the tables, see [Configuration tables and prerequisites for Tax integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/config-tax-integ.md).

</td></tr><tr><td>

The external tax engine computes the tax.

</td><td>

Calculates the tax and returns the response. The response is processed, tax lines are created automatically for the applicable invoice in Accounts Payable Operations. The system triggers exception engine based on the response from tax engine. Tax exception is raised when supplier tax and system tax mismatch in the invoice. Invoice tax status is set to integration error and Accounts Payable specialist investigates the case manually. If the invoice is modified after last execution \(change amounts, add lines or adjust tax codes\), then the tax is recalculated. The tax processing is re-initiated. on successful validation, the invoice processing proceeds to payment.

</td></tr></tbody>
</table>## How the Vertex integration works

The Tax Engine Integration with Vertex \(com.sn\_fsc\_vertex\) enables seamless connectivity between ServiceNow and Vertex tax system to automate tax calculation and validation.

The integration processes an invoice through the following stages:

-   Connectivity - The integration authenticates to Vertex over OAuth by using the client-credentials grant, through a reusable connection template and a connection alias. The connection attributes for product and API version are configurable for each environment.
-   Transformation - The integration converts the staging record into the Vertex request format, sends it to Vertex, and converts the response back into the staging format by using a shared field-mapping table.

    For more information on the mappings and jurisdictions, see [Tax integration field map fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/tax-integration-field-map-fields.md), [Jurisdictions main table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/accounts-payable-operations/jurisdiction-master-table.md).


## Tax validation modes

Tax calculation and validation can be triggered in multiple ways:

-   Automatic \(synchronous\)-Runs automatically at key invoice processing milestones
-   Manual \(on-demand\)-AP specialists can trigger tax validation during invoice exception review. This is applicable or accessible from the tax exception
-   Scheduler re-calculation-Background jobs automatically re‑initiate tax validation for invoices that are in progress, or recalculate tax status and integration error status. This verifies taxes stay accurate even if invoice data is updated or external calls fail temporarily.

## Tax integration workflow

A high level workflow of how tax integration works in Accounts Payable Operations is shown previous.

\[Omitted image "tax-integ-workflow.png"\] Alt text: Tax integration workflow

**Note:** If you're upgrading from previous version of APO to latest version, you must execute the scheduled job \[APO - close open exception for deactivated exception definition\]. This scheduled job updates the status of invoice exceptions to inactive and closes the corresponding invoice exceptions.

