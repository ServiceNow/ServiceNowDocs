---
title: Accounts Payable Operations integration framework
description: Invoice integration facilitates inbound and outbound integration with third party applications or any external systems into the ServiceNow application.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Accounts Payable Operations integration framework

Invoice integration facilitates inbound and outbound integration with third party applications or any external systems into the ServiceNow® application.

The integration framework consists of inbound invoice and outbound invoice interface tables. Invoice integration involves the transfer of invoice and invoice line data by running transform maps through various sources or external systems. For more information on integration, see [Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/integrationhub.md).

The integration framework enables the following use cases:

-   Ingest invoices from external sources - The invoice data is extracted from ERP sources into ServiceNow® inbound staging tables and is referred as inbound integration.
-   Post invoices into ERP- The invoice and invoice line data with **Approved** status is synchronized with ServiceNow® outbound invoice and invoice line tables. The integration status is set to **New** and is referred as outbound integration.
-   Ingest invoice payment details from ERP- The ERP number received from the third party application is updated in the invoice table with payment status as **Pending Payment**. The supplier selects the payment method, proceeds with the payment and sets the payment status as **Paid**.

For example, You’re receiving invoice data from various sources. The invoice data is transferred to inbound invoice and invoice lines if the required fields are set on the invoice. For more information on the required fields, see [Inbound Invoice Fields](../reference/inbound-invoice-fields.md) and [Inbound invoice line fields](../reference/inbound-invoice-line-fields.md). The invoice status changes to **Approved** and the invoice data is transferred to outbound invoice tables. The outbound invoice displays the integration status as **New**. The ERP integrator fetches the outbound invoices with status as **New**, creates a record in the third party application and sets the integration status to **In progress**. After the outbound data is successfully processed by the third party application, the system auto updates the ERP number in the outbound invoice tables and sets the integration status to **Processed**. The ERP number is updated in the invoice table with payment status set to **Pending Payment**.The supplier verifies the invoice payment details, proceeds with the payment and the payment status is set to **Paid**. For more information on payment fields, see [Inbound invoice payment fields](../reference/inbound-invoice-payment-fields.md).

The advantages of integration framework are:

-   Expedites the integration of the Accounts Payable Operations application with external systems and reduces the time to verify invoices. Integration framework enables bulk import of invoice and invoice line data through scheduled jobs. A scheduled job runs every 30 minutes, verifies, and auto process the invoices. Scheduled jobs result in increased efficiency of creating invoices.
-   Expedite the payment processing process and enhance the user experience by seamlessly exchanging data with external systems.

