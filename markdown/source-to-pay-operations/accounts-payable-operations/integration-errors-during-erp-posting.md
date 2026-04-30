---
title: Integration errors
description: The ERP integration framework enables Accounts Payable Operations specialists to work on system-generated integration error tasks that record integration issues associated with invoices posted to the ERP system.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Accounts Payable Operations integration framework, Integrating APO with other applications, Accounts Payable Operations, Finance and Supply Chain]
---

# Integration errors

The ERP integration framework enables Accounts Payable Operations specialists to work on system-generated integration error tasks that record integration issues associated with invoices posted to the ERP system.

When the invoice is posted to an outbound staging table in the Accounts Payable Operations application, sometimes due to poor data connection, or missing data, the ERP integration can fail. Such integration failures are tracked in the form of system-generated integration error tasks. The integration error tasks are created and auto-assigned to the Accounts Payable Operations specialist involved in the processing of invoice case. With playbooks, Accounts Payable Operations specialist uses the **Review integration errors** activity card to review the error tasks associated with the invoice processing case, make required changes to the invoice header, invoice lines and resubmits the invoice to ERP by integration.

When invoices are ingested through DocIntel or integration, you can determine the ERP source for certain fields like Purchase order, Legal entity, Original invoice, Supplier tax id and Supplier. You can populate the reference fields matching the ERP source.

Integration admins are notified about the integration errors through **Integration Error Tasks** caused due to issues such as system time outs. If there are system issues, the integration admin can execute jobs of type scheduled, on-demand or auto-schedule to handle integration error tasks. The scheduled job triggers the posting of erroneous invoices.

When invoice and invoice lines ingested by DocIntel or integration can result in errors

Playbooks are designed to auto-create an error task and attach the error task to the respective invoice case.

The Accounts Payable Operations specialists can also view the ERP posting errors through the Accounts Payable Operations home page too. For more information on the home page, see [APO landing page](acc-pay-workspace-landing-page.md).

When the Accounts Payable Operations admin closes the integration error task and resubmits the invoice to ERP, the following actions occur in the Outbound Invoice record.

-   A new outbound invoice record is created
-   The ERP admin reviews the outbound invoice record with status **New** updates the ERP number, ERP line number, and ERP posting date
-   The ERP admin changes the **Integration status** to processed
-   The invoice processing case changes status to pending payment, and the review payments activity card is auto-selected

For manually created invoices, the selected ERP source reference field will serve as the primary ERP reference for any subsequent selections.

For example, if the user selects supplier as the primary attribute and this field references ERP1 as its source, then the corresponding ERP1 filter condition is applied to the invoice header and to all related reference fields in both the invoice table and invoice lines to be consistent with the ERP1 source.

If the supplier does not have an associated ERP source, and the user selects a different field—such as legal entity—that does not reference ERP2, the previously selected supplier field will be cleared. The legal entity will serve as the primary attribute, and because it references ERP2, the ERP2 filter condition will be applied to the invoice header and all related reference fields in both the invoice table and invoice lines to ensure alignment with the ERP2 source.

Invoices ingested through Document Intelligence and APIs include reference fields—such as purchase order, supplier, payment term, legal entity, default tax code are linked to a consistent ERP source to prevent integration errors.

For PO invoices, the ERP source is referenced in following order:

1.  Purchase order number
2.  Bill to legal entity
3.  Supplier

For credit memo type, the ERP source is referenced in following order:

1.  Bill to legal entity
2.  Supplier
3.  Original invoice

With Non-PO invoices, Bill to legal entity and supplier are referenced.

![ERP source](../image/erp-source.png)

**Related topics**  


[Work with invoices](work-with-invoices.md)

