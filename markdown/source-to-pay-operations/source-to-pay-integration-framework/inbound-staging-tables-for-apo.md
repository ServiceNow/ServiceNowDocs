---
title: Inbound staging tables for Accounts Payable Operations
description: The inbound staging tables for Accounts Payable Operations temporarily stores invoice data before it is sent to the APO primary data tables.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Inbound staging tables for Accounts Payable Operations

The inbound staging tables for Accounts Payable Operations temporarily stores invoice data before it is sent to the APO primary data tables.

-   **[Invoice import inbound staging table](../../source-to-pay-integrations/reference/inbound-invoice-import-staging-table.md)**  
The invoice import inbound \[sn\_spend\_intg\_imp\_invoice\] staging table temporarily stores important data about the imported invoice before this data is sent to the \[sn\_shop\_invoice\] primary table.
-   **[Import error staging table](../reference/import-error-staging-table.md)**  
The Import error \[sn\_spend\_intg\_import\_error\] staging table temporarily stores important data on errors before this data is sent to the primary table.
-   **[Invoice line import inbound staging table](../../source-to-pay-integrations/reference/inbound-invoice-line-staging-table.md)**  
The Invoice line import inbound \[sn\_spend\_intg\_imp\_invoice\_line\] staging table temporarily stores important data about imported invoice line before this data is sent to the \[sn\_shop\_invoice\_line\] primary table.
-   **[Invoice payment detail import inbound table](../reference/invoice-payment-detail-staging-table.md)**  
The Invoice Payment detail import inbound \[sn\_spend\_intg\_imp\_invoice\_payment\_detail\] staging table temporarily stores important data about supplier before this data is sent to the \[sn\_shop\_invoice\_payment\_detail\] primary table.
-   **[Organization tax details inbound staging table](../../source-to-pay-integrations/reference/slo-org-tax-details-inbound-table.md)**  
The Organization tax details inbound \[sn\_fcms\_intg\_org\_tax\_detail\_inbound\] staging table temporarily stores important data about an organization's tax information before this data is sent to the Organization Tax Details \[sn\_fin\_org\_tax\_detail\] primary table.
-   **[Invoice tax line staging table](../../source-to-pay-operations/reference/inbound-invoice-tax-line-staging-table-apo.md)**  
The invoice tax line inbound \[sn\_spend\_intg\_imp\_invoice\_tax\_line\] staging table temporarily stores important data about the invoice tax line before this data is sent to the \[sn\_shop\_invoice\_tax\_line\] primary table.
-   **[Invoice staging table](../reference/invoice-staging-table.md)**  
The invoice staging \[sn\_ap\_ic\_invoice\_stage\] table temporarily stores the header-level invoice data from Document Intelligence before it is transferred to the invoice record.
-   **[Invoice line stage table](../reference/invoice-line-staging-table.md)**  
The invoice line stage \[sn\_ap\_ic\_invoice\_line\_stage\] table stores line-level invoice data extracted by Document Intelligence.

**Parent Topic:**[Inbound staging tables for Source-to-Pay Operations](../../source-to-pay-integrations/concept/s2p-inbound-staging-tables.md)

**Related topics**  


[Inbound staging tables for Sourcing and Procurement Operations](../../source-to-pay-integrations/concept/spo-inbound-staging-tables.md)

[Inbound staging tables for Supplier Lifecycle Operations](../../source-to-pay-integrations/concept/slo-inbound-staging-tables.md)

