---
title: Integration errors
description: Integration errors occur when invoices fail to post to the ERP system due to data connection issues or missing data, and the ERP integration framework tracks these failures as system-generated error tasks for specialist review and resubmission.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/integration-errors-during-erp-posting.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice management, ERP integration, invoice automation]
breadcrumb: [Accounts Payable Operations integration framework, Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Integration errors

Integration errors occur when invoices fail to post to the ERP system due to data connection issues or missing data, and the ERP integration framework tracks these failures as system-generated error tasks for specialist review and resubmission.

When the invoice is posted to an outbound staging table in the Accounts Payable Operations application, sometimes due to poor data connection, or missing data, the ERP integration can fail. Such integration failures are tracked in the form of system-generated integration error tasks. The integration error tasks are created and auto-assigned to the Accounts Payable Operations specialist involved in the processing of invoice case. With playbooks, Accounts Payable Operations specialist uses the **Review integration errors** activity card to review the error tasks associated with the invoice processing case, make required changes to the invoice header, invoice lines and resubmits the invoice to ERP by integration.

When invoices are ingested through DocIntel or integration, you can determine the ERP source for certain fields like Purchase order, Legal entity, Original invoice, Supplier tax id and Supplier. You can populate the reference fields matching the ERP source.

Integration admins are notified about the integration errors through **Integration Error Tasks** caused due to issues such as system time outs. If there are system issues, the integration admin can execute jobs of type scheduled, on-demand or auto-schedule to handle integration error tasks. The scheduled job triggers the posting of erroneous invoices.

When invoice and invoice lines ingested by DocIntel or integration can result in errors

Playbooks are designed to auto-create an error task and attach the error task to the respective invoice case.

The Accounts Payable Operations specialists can also view the ERP posting errors through the Accounts Payable Operations home page too. For more information on the home page, see [APO landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-workspace/acc-pay-workspace-landing-page.md).

When the Accounts Payable Operations admin closes the integration error task and resubmits the invoice to ERP, the following actions occur in the Outbound Invoice record.

-   A new outbound invoice record is created
-   The ERP admin reviews the outbound invoice record with status **New** updates the ERP number, ERP line number, and ERP posting date
-   The ERP admin changes the **Integration status** to processed
-   The invoice processing case changes status to pending payment, and the review payments activity card is auto-selected

