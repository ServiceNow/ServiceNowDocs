---
title: Inbound staging tables for Accounts Payable Operations
description: Inbound staging tables for Accounts Payable Operations temporarily store invoice data from ERP sources before transferring it to primary data tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/inbound-staging-tables-for-apo.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice management, staging table,, inbound integration]
breadcrumb: [Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Inbound staging tables for Accounts Payable Operations

Inbound staging tables for Accounts Payable Operations temporarily store invoice data from ERP sources before transferring it to primary data tables.

-   **[Invoice import inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/inbound-invoice-import-staging-table.md)**  
The invoice import inbound \[sn\_spend\_intg\_imp\_invoice\] staging table temporarily stores important data about the imported invoice before this data is sent to the \[sn\_shop\_invoice\] primary table.
-   **[Import error staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/import-error-staging-table.md)**  
Field descriptions for the Import error \[sn\_spend\_intg\_import\_error\] staging table, which temporarily stores import error data before it is transferred to the primary table.
-   **[Invoice line import inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/inbound-invoice-line-staging-table.md)**  
The Invoice line import inbound \[sn\_spend\_intg\_imp\_invoice\_line\] staging table temporarily stores important data about imported invoice line before this data is sent to the \[sn\_shop\_invoice\_line\] primary table.
-   **[Invoice payment detail import inbound table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/invoice-payment-detail-staging-table.md)**  
Field descriptions and data types for the Invoice Payment Detail Import Inbound \[sn\_spend\_intg\_imp\_invoice\_payment\_detail\] staging table used to store imported invoice payment detail data from ERP systems before transfer to the \[sn\_shop\_invoice\_payment\_detail\] primary table.
-   **[Organization tax details inbound staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/slo-org-tax-details-inbound-table.md)**  
The Organization tax details inbound \[sn\_fcms\_intg\_org\_tax\_detail\_inbound\] staging table temporarily stores important data about an organization's tax information before this data is sent to the Organization Tax Details \[sn\_fin\_org\_tax\_detail\] primary table.
-   **[Invoice tax line staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/inbound-invoice-tax-line-staging-table-apo.md)**  
The invoice tax line inbound \[sn\_spend\_intg\_imp\_invoice\_tax\_line\] staging table temporarily stores important data about the invoice tax line before this data is sent to the \[sn\_shop\_invoice\_tax\_line\] primary table.
-   **[Invoice staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/invoice-staging-table.md)**  
The invoice staging \[sn\_ap\_ic\_invoice\_stage\] table temporarily stores the header-level invoice data from Document Intelligence before it is transferred to the invoice record.
-   **[Invoice line stage table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/invoice-line-staging-table.md)**  
The invoice line stage \[sn\_ap\_ic\_invoice\_line\_stage\] table stores line-level invoice data extracted by Document Intelligence.

**Parent Topic:**[Inbound staging tables for Source-to-Pay Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-integration-framework/s2p-inbound-staging-tables.md)

**Related topics**  


[Inbound staging tables for Sourcing and Procurement Operations]()

[Inbound staging tables for Supplier Lifecycle Operations]()

