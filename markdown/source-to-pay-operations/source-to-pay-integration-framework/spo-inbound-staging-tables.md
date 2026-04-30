---
title: Inbound staging tables for Sourcing and Procurement Operations
description: The inbound staging tables for Sourcing and Procurement Operations temporarily store sourcing and procurement data before it is sent to the SPO primary data tables.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Inbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Inbound staging tables for Sourcing and Procurement Operations

The inbound staging tables for Sourcing and Procurement Operations temporarily store sourcing and procurement data before it is sent to the SPO primary data tables.

-   **[CMDB Model Category Stage inbound staging table](../reference/spo-prod-cate-inbound-table.md)**  
The CMDB Model Category Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_category\_stage\] staging table temporarily stores important data about product model categories before this data is sent to the primary table.
-   **[CMDB Service Model Stage inbound staging table](../reference/spo-serv-mod-inbound-table.md)**  
The CMDB Service Model Stage inbound \[sn\_fcms\_intg\_cmdb\_service\_model\_stage\] staging table temporarily stores important data about service models before this data is sent to the primary table.
-   **[CMN Location Stage inbound staging table](../reference/spo-loc-inbound-table.md)**  
The CMN Location Stage inbound \[sn\_fcms\_intg\_cmn\_location\_stage\] staging table temporarily stores important data about locations before this data is sent to the primary table.
-   **[Catalog Import staging table](../reference/catalog-import-staging-table.md)**  
The Catalog Import \[sn\_spend\_intg\_imp\_catalog\] staging table temporarily stores important data about catalog imports before this data is sent to the primary table.
-   **[Catalog Error staging table](../reference/catalog-error.md)**  
The Catalog Error \[sn\_spend\_intg\_catalog\_error\] staging table temporarily stores important data about any catalog errors before this data is sent to the primary table.
-   **[Cost Center Stage inbound staging table](../reference/spo-cost-center-inbound-table.md)**  
The Cost Center Stage inbound \[sn\_fcms\_intg\_imp\_cost\_center\] staging table temporarily stores important data about cost centers before this data is sent to the primary table. You can use this table to lookup all the cost center details.
-   **[Department Stage inbound staging table](../reference/spo-dept-inbound-table.md)**  
The Department Stage inbound \[sn\_fcms\_intg\_department\_stage\] staging table temporarily stores important data about departments before this data is sent to the primary table.
-   **[ERP Plant Address Mapping Stage inbound staging table](../reference/spo-erp-plant-address-inbound-table.md)**  
The ERP Plant Address Mapping Stage inbound \[sn\_fcms\_intg\_erp\_plant\_address\_mapping\_stage\] staging table temporarily stores important data about ERP plant address before this data is sent to the primary table.
-   **[FX Currency Stage inbound staging table](../reference/spo-fx-currency-inbound-table.md)**  
The FX Currency Stage inbound \[sn\_fcms\_intg\_fx\_currency\_stage\] staging table temporarily stores important data about FX currencies before this data is sent to the primary table.
-   **[FX Rate Stage inbound staging table](../reference/spo-fx-rate-inbound-table.md)**  
The FX Rate Stage inbound \[sn\_fcms\_intg\_fx\_rate\_stage\] staging table temporarily stores important data about FX rates before this data is sent to the primary table.
-   **[Fixed asset details stage inbound table](../reference/fixed-asset-details-stage-inbound-table.md)**  
The Fixed asset details inbound \[sn\_fcms\_intg\_imp\_fixed\_asset\_details\] staging table temporarily stores important data about imported invoice line before this data is sent to the primary table.
-   **[GL Account Stage inbound staging table](../reference/spo-gl-account-inbound-table.md)**  
The GL Account Stage inbound \[sn\_fcms\_intg\_gl\_account\_stage\] staging table temporarily stores important data about General Ledger \(GL\) accounts before this data is sent to the primary table.
-   **[Import Availability Updates inbound staging table](../reference/spo-import-avail-inbound-table.md)**  
The Import Availability Updates inbound \[sn\_spend\_intg\_imp\_availability\] staging table temporarily stores important data about cost allocations before this data is sent to the primary table.
-   **[Availability Error staging table](../reference/availability-error-staging-table.md)**  
The Availability Error \[sn\_spend\_intg\_availability\_error\] staging table stores important data about availability error so that an ERP integrator can export this data to a third-party ERP system.
-   **[Cost Allocation inbound staging table \(Deprecated\)](../reference/spo-cost-alloc-inbound-table.md)**  
The Cost Allocation inbound \[sn\_spend\_intg\_imp\_cost\_allocation\] staging table temporarily stores important data about cost allocations before this data is sent to the primary table.
-   **[Invoice inbound staging table](../reference/spo-inbound-invoice-table.md)**  
The Invoice inbound \[sn\_shop\_invoice\] staging table temporarily stores important data about shopping invoices before this data is sent to the primary table.
-   **[Purchase Order inbound staging table](../reference/spo-inbound-pur-order-table.md)**  
The Purchase Order inbound \[sn\_fcms\_intg\_imp\_order\] staging table temporarily stores important data about purchase orders before this data is sent to the primary table.
-   **[Purchase Order Line inbound staging table](../reference/spo-inbound-pol-table.md)**  
The Purchase Order Line inbound \[sn\_fcms\_intg\_imp\_order\_line\] staging table temporarily stores important data about purchase order lines before this data is sent to the primary table.
-   **[Receipt inbound staging table](../reference/spo-inbound-receipt-table.md)**  
The Receipt inbound \[sn\_fcms\_intg\_imp\_receipt\] staging table temporarily stores important data about receipts before this data is sent to the primary table.
-   **[Legal Entity Stage inbound staging table](../reference/spo-legal-entity-inbound-table.md)**  
The Legal entity stage inbound \[sn\_fcms\_intg\_legal\_entity\_stage\] staging table temporarily stores important data about legal entities before this data is sent to the primary table.
-   **[Office Location Stage inbound staging table](../reference/spo-office-loc-inbound-table.md)**  
The Office Location Stage inbound \[sn\_fcms\_intg\_office\_location\_stage\] staging table temporarily stores important data about office locations before this data is sent to the primary table.
-   **[Order Acknowledgement staging table](../reference/order-acknowledgement-staging-table.md)**  
The Order Acknowledgment \[sn\_spend\_intg\_imp\_purchase\_order\_ack\] staging table temporarily stores important data about order acknowledgements before this data is sent to the primary table.
-   **[Order Acknowledgement Error staging table](../reference/order-acknowledgement-error.md)**  
The Order Acknowledgement Error \[sn\_spend\_intg\_order\_ack\_error\] staging table temporarily stores important data about any errors in the order price imports before this data is sent to the primary table.
-   **[Payment Terms Stage inbound staging table](../reference/spo-pay-terms-inbound-table.md)**  
The Payment Terms Stage inbound \[sn\_fcms\_intg\_payment\_term\_stage\] staging table temporarily stores important data about payment terms before this data is sent to the primary table.
-   **[Price Import staging table](../reference/price-import-staging-table.md)**  
The Price Import \[sn\_spend\_intg\_imp\_price\] staging table temporarily stores important data about price imports before this data is sent to the primary table.
-   **[Price Error outbound staging table](../reference/price-error-staging-table.md)**  
The Price Error \[sn\_spend\_intg\_price\_error\] staging table stores important data about pricing error so that an ERP integrator can export this data to a third-party ERP system.
-   **[Product Model Stage inbound staging table](../reference/spo-prod-mod-inbound-table.md)**  
The Product Model Stage inbound \[sn\_fcms\_intg\_cmdb\_model\_stage\] staging table temporarily stores important data about product models before this data is sent to the primary table.
-   **[Purchase Entity Stage inbound staging table](../reference/spo-purch-entity-inbound-table.md)**  
The Purchase Entity Stage inbound \[sn\_fcms\_intg\_imp\_purchase\_entity\] staging table temporarily stores important data about purchase entities before this data is sent to the primary table.
-   **[Purchase Line Stage inbound staging table](../reference/spo-purch-line-stage-inbound-table.md)**  
The Purchase Entity Stage inbound \[sn\_spend\_intg\_purchase\_line\] staging table temporarily stores important data about purchase entities before this data is sent to the primary table.
-   **[Purchase Requisition staging table](../reference/purchase-requisition-staging-table.md)**  
The Purchase requisition \[sn\_spend\_intg\_purchase\_requisition\] staging table temporarily stores important data about purchase requests before this data is sent to the primary table.
-   **[Spend Shipment Import inbound staging table](../reference/spend-shipment-import-inbound-table.md)**  
The Spend Shipment Import inbound \[sn\_spend\_intg\_imp\_shipment\] staging table temporarily stores important data about spend shipment imports before this data is sent to the primary table.
-   **[Shipment Error staging table](../reference/shipment-error-staging-table.md)**  
The Shipment Error \[sn\_spend\_intg\_shipment\_error\] staging table temporarily stores important data on any shipment errors before this data is sent to the primary table.
-   **[Supplier Product Stage inbound staging table](../reference/spo-supp-prod-inbound-table.md)**  
The Supplier Product Stage inbound \[sn\_spend\_intg\_supplier\_product\_stage\] staging table temporarily stores important data about supplier products before this data is sent to the primary table.
-   **[Third Party Sourcing Registration staging table](../reference/third-party-sourcing-registration-staging-table.md)**  
The Third Party Sourcing Registration \[sn\_spend\_intg\_sourcing\_vendor\] table temporarily stores important data on third party sourcing registrations before this data is sent to the primary table.
-   **[Third Party Unit Mapping staging table](../reference/third-party-unit-mapping-staging-table.md)**  
The Third Party Unit Mapping \[sn\_spend\_intg\_third\_party\_uom\_map\] staging table temporarily stores important data on third party mapping before this data is sent to the primary table.
-   **[Third Party Unit staging table](../reference/third-party-unit-staging-table.md)**  
The Third Party Unit \[sn\_spend\_intg\_third\_party\_uom\] staging table temporarily stores important data on third party units before this data is sent to the primary table.
-   **[Unit of Measure inbound staging table](../reference/unit-measure-inbound-staging-table.md)**  
The Third Party Unit \[sn\_fcms\_intg\_imp\_uom\] staging table temporarily stores important data on third party units before this data is sent to the primary table.

**Parent Topic:**[Inbound staging tables for Source-to-Pay Operations](s2p-inbound-staging-tables.md)

**Related topics**  


[Inbound staging tables for Supplier Lifecycle Operations](../../supplier-lifecycle-operations/concept/slo-inbound-staging-tables.md)

[Inbound staging tables for Accounts Payable Operations](../../accounts-payable-operations/concept/inbound-staging-tables-for-apo.md)

