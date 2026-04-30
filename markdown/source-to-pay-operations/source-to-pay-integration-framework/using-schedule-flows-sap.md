---
title: Use schedule flows in SAP
description: Use the schedule flows that interact with SAP to pull information on purchase requisition, purchase order, receipt, invoice, and sourcing.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Use, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use schedule flows in SAP

Use the schedule flows that interact with SAP to pull information on purchase requisition, purchase order, receipt, invoice, and sourcing.

You can either use the subflows to perform the required tasks or you can create a copy of the subflows and then customize it according to your requirements.

**Important:**

These subflows are read-only. To modify a flow or subflow, create a copy and then apply the required changes.

The Source-to-Pay with SAP integration supports the following subflows.

## Primary Data Integration with SAP

The Primary Data Integration with SAP supports the following subflows and system properties:

**Subflows for Primary Data Integration with SAP ECC**

|Subflow|Description|
|-------|-----------|
|Fetch Currencies|Use this subflow to fetch and synchronize all currencies from SAP ECC system.|
|Fetch Legal Entities|Use this subflow to fetch and synchronize all legal entities from SAP ECC system.|
|Fetch FX Currency Rates|Use this subflow to fetch and synchronize all FX currency rates from SAP ECC system.|
|Fetch Cost Centers|Use this subflow to fetch and synchronize all cost centers from SAP ECC system.|
|Fetch Departments|Use this subflow to fetch and synchronize all departments from SAP ECC.|
|Fetch Payment Terms|Use this subflow to fetch and synchronize all payment terms from SAP ECC system.|
|Fetch Purchasing Orgs|Use this subflow to fetch and synchronize all purchasing organizations from SAP ECC system.|
|Fetch GL Accounts|Use this subflow to fetch and synchronize all GL accounts from SAP ECC system.|
|Fetch Product Models|Use this subflow to fetch and synchronize all product models from SAP ECC system.|
|Fetch ServiceNow Product Models|Use this subflow to fetch and synchronize all ServiceNow product models from SAP ECC system.|
|Fetch Plant Addresses|Use this subflow to fetch plant addresses from SAP ECC system.|
|Fetch Suppliers|Use this subflow to fetch and synchronize all suppliers from SAP ECC system.|

**System Properties for Primary Data Integration with SAP ECC**

Use these system properties to configure settings for the Primary Data Integration with SAP ECC from the System Properties page. For more information, see [Source-to-Pay integrations with SAP reference](../reference/s2p-integrations-sap-reference.md).

Role required:

-   **Read Role**: sn\_shop.procurement\_specialist, sn\_shop.shopper, sn\_fcms\_intg.admin
-   **Write Role**: sn\_fcms\_intg.admin

<table id="table_zhx_grm_nhc"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sap\_data\_int.cloud\_base\_unit\_of\_measure\_service\_subflow

</td><td>

Use this subflow for fetching the base units of measure from SAP ECC system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_company\_codes\_service\_subflow

</td><td>

Use this subflow for fetching company codes from SAP ECC system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_cost\_centers\_service\_subflow

</td><td>

Use this subflow for fetching cost center data from SAP ECC system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_fetch\_suppliers\_service\_subflow

</td><td>

Use this subflow for fetching supplier details from SAP ECC system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_materials\_service\_subflow

</td><td>

Use this subflow for fetching material data from SAP ECC system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_material\_group\_service\_subflow

</td><td>

Use this subflow for fetching material group information from SAP ECC system.

</td></tr><tr><td>

sn\_sap\_data\_int.full\_load\_time\_range\_default

</td><td>

Defines the default time range for full data loads.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_base\_unit\_of\_measure\_service\_subflow

</td><td>

Use this subflow for fetching base unit of measure data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_cost\_centers\_service\_subflow

</td><td>

Use this subflow for fetching cost center details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_currencies\_service\_subflow

</td><td>

Use this subflow for syncing currency information using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_fx\_rate\_service\_subflow

</td><td>

Use this subflow for fetching foreign exchange rates using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_gl\_account\_service\_subflow

</td><td>

Use this subflow for fetching general ledger account data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_legal\_entities\_service\_subflow

</td><td>

Use this subflow for fetching legal entity details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_materials\_service\_subflow

</td><td>

Use this subflow for fetching materials data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_material\_group\_service\_subflow

</td><td>

Use this subflow for fetching material group details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_payment\_terms\_service\_subflow

</td><td>

Use this subflow for fetching payment terms information using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_plant\_addresses\_service\_subflow

</td><td>

Use this subflow for retrieving plant address details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_purchasing\_group\_service\_subflow

</td><td>

Use this subflow for fetching purchasing group data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_purchasing\_organizations\_service\_subflow

</td><td>

Use this subflow for fetching purchasing organization details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_suppliers\_service\_subflow

</td><td>

Use this subflow for fetching supplier information through OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.Subflow.Resume.Count

</td><td>

Track the number of times a subflow resumes execution.Default value: 30

</td></tr><tr><td>

sn\_sap\_data\_int.subflow\_timeout\_value

</td><td>

Maximum timeout duration \(in milliseconds\) for subflow execution.Default value: 10000000

</td></tr></tbody>
</table>**Subflows for Primary Data Integration with SAP S4 HANA Cloud**

|Subflow|Description|
|-------|-----------|
|Fetch Legal Entities|Use this subflow to fetch and synchronize all legal entities from SAP S4 HANA Cloud system.|
|Fetch Cost Centers|Use this subflow to fetch and synchronize all cost centers from SAP S4 HANA Cloud system.|
|Fetch GL Accounts|Use this subflow to fetch and synchronize all GL accounts from SAP S4 HANA Cloud system.|
|Fetch Suppliers|Use this subflow to fetch and synchronize all supplier details from SAP S4 HANA Cloud system.|
|Fetch Product Models|Use this subflow to fetch and synchronize all product models from SAP S4 HANA Cloud system.|
|Fetch Units of Measure|Use this subflow to fetch base unit of measure from SAP S4 HANA Cloud system.|
|Fetch Product Categories|Use this subflow to fetch and synchronize all product categories from SAP S4 HANA Cloud system.|

**System Properties for Primary Data Integration with SAP S4 HANA Cloud**

Use these system properties to configure settings for the Primary Data Integration with SAP S4 HANA Cloud from the System Properties page. For more information, see [Source-to-Pay integrations with SAP reference](../reference/s2p-integrations-sap-reference.md).

Role required:

-   **Read Role**: sn\_shop.procurement\_specialist, sn\_shop.shopper, sn\_fcms\_intg.admin
-   **Write Role**: sn\_fcms\_intg.admin

<table id="table_r3d_t5m_nhc"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sap\_data\_int.cloud\_base\_unit\_of\_measure\_service\_subflow

</td><td>

Use this subflow for fetching the base units of measure from SAP S4 HANA Cloud system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_company\_codes\_service\_subflow

</td><td>

Use this subflow for fetching company codes from SAP S4 HANA Cloud system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_cost\_centers\_service\_subflow

</td><td>

Use this subflow for fetching cost center data from SAP S4 HANA Cloud system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_fetch\_suppliers\_service\_subflow

</td><td>

Use this subflow for fetching supplier details from SAP S4 HANA Cloud system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_materials\_service\_subflow

</td><td>

Use this subflow for fetching material data from SAP S4 HANA Cloud system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_material\_group\_service\_subflow

</td><td>

Use this subflow for fetching material group information from SAP S4 HANA Cloud system.

</td></tr><tr><td>

sn\_sap\_data\_int.full\_load\_time\_range\_default

</td><td>

Defines the default time range for full data loads.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_base\_unit\_of\_measure\_service\_subflow

</td><td>

Use this subflow for fetching base unit of measure data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_cost\_centers\_service\_subflow

</td><td>

Use this subflow for fetching cost center details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_currencies\_service\_subflow

</td><td>

Use this subflow for syncing currency information using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_fx\_rate\_service\_subflow

</td><td>

Use this subflow for fetching foreign exchange rates using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_gl\_account\_service\_subflow

</td><td>

Use this subflow for fetching general ledger account data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_legal\_entities\_service\_subflow

</td><td>

Use this subflow for fetching legal entity details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_materials\_service\_subflow

</td><td>

Use this subflow for fetching materials data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_material\_group\_service\_subflow

</td><td>

Use this subflow for fetching material group details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_payment\_terms\_service\_subflow

</td><td>

Use this subflow for fetching payment terms information using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_plant\_addresses\_service\_subflow

</td><td>

Use this subflow for retrieving plant address details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_purchasing\_group\_service\_subflow

</td><td>

Use this subflow for fetching purchasing group data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_purchasing\_organizations\_service\_subflow

</td><td>

Use this subflow for fetching purchasing organization details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_suppliers\_service\_subflow

</td><td>

Use this subflow for fetching supplier information through OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.Subflow.Resume.Count

</td><td>

Track the number of times a subflow resumes execution.Default value: 30

</td></tr><tr><td>

sn\_sap\_data\_int.subflow\_timeout\_value

</td><td>

Maximum timeout duration \(in milliseconds\) for subflow execution.Default value: 10000000

</td></tr></tbody>
</table>**Subflows for Primary Data Integration with SAP S4 HANA OData**

|Subflow|Description|
|-------|-----------|
|Fetch Currencies|Use this subflow to fetch and synchronize all Currencies from SAP S4 HANA OData system.|
|Fetch Legal Entities|Use this subflow to fetch and synchronize all legal entities from SAP S4 HANA OData system.|
|Fetch FX Currency Rates|Use this subflow to fetch and synchronize all FX rates from SAP S4 HANA OData system.|
|Fetch Cost Centers|Use this subflow to fetch and synchronize all cost centers from SAP S4 HANA OData system.|
|Fetch Departments|Use this subflow to fetch and synchronize all departments from SAP S4 HANA OData system.|
|Fetch Payment Terms|Use this subflow to fetch and synchronize all payment terms from SAP S4 HANA OData system.|
|Fetch Purchasing Orgs|Use this subflow to fetch and synchronize all Purchasing Organizations from SAP S4 HANA OData system.|
|Fetch GL Accounts|Use this subflow to fetch and synchronize all GL accounts from SAP S4 HANA OData system.|
|Fetch Plant Addresses|Use this subflow to Fetch Plant Addresses from SAP S4 HANA OData system.|
|Fetch Suppliers|Use this subflow to fetch and synchronize all supplier details from SAP S4 HANA OData system.|
|Fetch Product Models|Use this subflow to fetch and synchronize all product models from SAP S4 HANA Cloud system.|
|Fetch Units of Measure|Use this subflow to fetch base unit of measure from SAP S4 HANA Cloud system.|
|Fetch Product Categories|Use this subflow to fetch and synchronize all product categories from SAP S4 HANA Cloud system.|

**System Properties for Primary Data Integration with SAP S4 HANA OData**

Use these system properties to configure settings for the Primary Data Integration with SAP S4 HANA OData from the System Properties page. For more information, see [Source-to-Pay integrations with SAP reference](../reference/s2p-integrations-sap-reference.md).

Role required:

-   **Read Role**: sn\_shop.procurement\_specialist, sn\_shop.shopper, sn\_fcms\_intg.admin
-   **Write Role**: sn\_fcms\_intg.admin

<table id="table_m5v_m5m_nhc"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_sap\_data\_int.cloud\_base\_unit\_of\_measure\_service\_subflow

</td><td>

Use this subflow for fetching the base units of measure from SAP S4 HANA OData system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_company\_codes\_service\_subflow

</td><td>

Use this subflow for fetching company codes from SAP S4 HANA OData system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_cost\_centers\_service\_subflow

</td><td>

Use this subflow for fetching cost center data from SAP S4 HANA OData system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_fetch\_suppliers\_service\_subflow

</td><td>

Use this subflow for fetching supplier details from SAP S4 HANA OData system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_materials\_service\_subflow

</td><td>

Use this subflow for fetching material data from SAP S4 HANA OData system.

</td></tr><tr><td>

sn\_sap\_data\_int.cloud\_material\_group\_service\_subflow

</td><td>

Use this subflow for fetching material group information from SAP S4 HANA OData system.

</td></tr><tr><td>

sn\_sap\_data\_int.full\_load\_time\_range\_default

</td><td>

Defines the default time range for full data loads.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_base\_unit\_of\_measure\_service\_subflow

</td><td>

Use this subflow for fetching base unit of measure data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_cost\_centers\_service\_subflow

</td><td>

Use this subflow for fetching cost center details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_currencies\_service\_subflow

</td><td>

Use this subflow for syncing currency information using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_fx\_rate\_service\_subflow

</td><td>

Use this subflow for fetching foreign exchange rates using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_gl\_account\_service\_subflow

</td><td>

Use this subflow for fetching general ledger account data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_legal\_entities\_service\_subflow

</td><td>

Use this subflow for fetching legal entity details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_materials\_service\_subflow

</td><td>

Use this subflow for fetching materials data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_material\_group\_service\_subflow

</td><td>

Use this subflow for fetching material group details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_payment\_terms\_service\_subflow

</td><td>

Use this subflow for fetching payment terms information using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_plant\_addresses\_service\_subflow

</td><td>

Use this subflow for retrieving plant address details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_purchasing\_group\_service\_subflow

</td><td>

Use this subflow for fetching purchasing group data using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_purchasing\_organizations\_service\_subflow

</td><td>

Use this subflow for fetching purchasing organization details using OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.odata\_suppliers\_service\_subflow

</td><td>

Use this subflow for fetching supplier information through OData service.

</td></tr><tr><td>

sn\_sap\_data\_int.Subflow.Resume.Count

</td><td>

Track the number of times a subflow resumes execution.Default value: 30

</td></tr><tr><td>

sn\_sap\_data\_int.subflow\_timeout\_value

</td><td>

Maximum timeout duration \(in milliseconds\) for subflow execution.Default value: 10000000

</td></tr></tbody>
</table>## Supplier Lifecycle Operations Integration with SAP

The Supplier Lifecycle Operations Integration with SAP supports the following subflows:

**Subflows for Supplier Lifecycle Operations Integration with SAP ECC**

|Flow|Description|
|----|-----------|
|Create or update supplier|Creates or updates or deactivates suppliers in SAP ECC.|
|Deactivate supplier bank details|Deactivates the supplier bank details in SAP ECC.|
|Create or update supplier payment information|Creates or updates supplier payment information in SAP ECC.|

**Subflows for Supplier Lifecycle Operations Integration with SAP S4 HANA OData**

|Flow|Description|
|----|-----------|
|Create or update supplier|Creates or updates or deactivates suppliers in SAP S4 HANA OData.|
|Deactivate supplier bank details|Deactivates the supplier bank details in SAP S4 HANA OData.|
|Create or update supplier payment information|Creates or updates supplier payment information in SAP S4 HANA OData.|

## Sourcing and Procurement Operations Integration with SAP

The Sourcing and Procurement Operations Integration with SAP supports the following subflows:

**Subflows for Sourcing and Procurement Operations Integration with SAP ECC**

|Flow|Description|
|----|-----------|
|Create or update Purchase Order|Creates or updates purchase orders in SAP ECC.|
|Create Goods Receipts|Creates goods receipts in SAP ECC.|
|Cancel Goods Receipts|Cancels goods receipts in SAP ECC.|
|Fetch Purchase Order|Fetches and synchronize all purchase orders from SAP ECC.|
|Fetch Goods Receipts|Fetches and synchronize all goods receipts from SAP ECC.|

**Subflows for Sourcing and Procurement Operations Integration with SAP S4 HANA OData**

Role required:

-   **Read Role**: sn\_shop.procurement\_specialist, sn\_shop.shopper, sn\_fcms\_intg.admin
-   **Write Role**: sn\_fcms\_intg.admin

|Flow|Description|
|----|-----------|
|Create or update Purchase Order|Creates or updates purchase orders in SAP S4 HANA OData.|
|Create Goods Receipts|Creates goods receipts in SAP S4 HANA OData.|
|Cancel Goods Receipts|Cancels goods receipts in SAP S4 HANA OData.|
|Fetch Purchase Order|Fetches and synchronize all purchase orders from SAP S4 HANA OData system.|
|Fetch Goods Receipts|Fetches and synchronize all goods receipts from SAP S4 HANA OData system.|

**System Properties for Sourcing and Procurement Operations Integration with SAP**

Use these system properties to configure settings for the Sourcing and Procurement Operations Integration with SAP from the System Properties page. For more information, see [Source-to-Pay integrations with SAP reference](../reference/s2p-integrations-sap-reference.md).

Role required:

-   **Read Role**: sn\_shop.procurement\_specialist, sn\_shop.shopper, sn\_fcms\_intg.admin
-   **Write Role**: sn\_fcms\_intg.admin

|Property Name|Description|
|-------------|-----------|
|sn\_psm\_sap\_int.should\_transactions\_flow\_through\_idoc|Indicates whether procurement transactions should be processed through SAP IDoc integration.|
|sn\_psm\_sap\_int.status\_for\_goods\_receipt|Current status of goods receipt in the procurement process.|
|sn\_psm\_sap\_int.status\_for\_purchase\_order|Current status of a purchase order within the SAP-integrated procurement workflow|

## Accounts Payable Operations Integration with SAP

The Accounts Payable Operations Integration with SAP supports the following subflows:

**Accounts Payable Operations Integration with SAP ECC**

Role required:

-   **Read Role**: sn\_shop.procurement\_specialist, sn\_shop.shopper, sn\_fcms\_intg.admin
-   **Write Role**: sn\_fcms\_intg.admin

|Flow|Description|
|----|-----------|
|Create Invoice|Creates invoices in SAP ECC.|
|Create Non-Purchase Order Invoice|Creates non-purchase order Invoices in SAP ECC.|
|Cancel Invoice|Cancels invoices in SAP ECC.|
|Authorize Payment|Authorizes and releases payment for supplier invoice in SAP ECC.|
|Fetch Invoice|Fetches and synchronize all invoices from the SAP ECC system.|

**Accounts Payable Operations Integration with SAP S4 HANA OData**

|Flow|Description|
|----|-----------|
|Create Invoice|Creates invoices in SAP S4 HANA OData.|
|Create Non-Purchase Order Invoice|Create non-purchase order Invoices in SAP S4 HANA OData.|
|Cancel Invoice|Cancels invoices in SAP S4 HANA OData.|
|Authorize Payment|Authorizes and releases payment for supplier invoice in SAP S4 HANA OData.|
|Fetch Invoice|Fetches and synchronize all invoices from the SAP S4 HANA OData system.|

**System Properties for Accounts Payable Operations Integration with SAP**

Use these system properties to configure settings for the Accounts Payable Operations Integration with SAP from the System Properties page. For more information, see [Source-to-Pay integrations with SAP reference](../reference/s2p-integrations-sap-reference.md).

Role required:

-   **Read Role**: sn\_shop.procurement\_specialist, sn\_shop.shopper, sn\_fcms\_intg.admin
-   **Write Role**: sn\_fcms\_intg.admin

|Property Name|Description|
|-------------|-----------|
|sn\_apm\_sap\_int.cloud\_invoices\_service\_subflow|Specifies the subflow used to fetch invoice data from the Cloud-based SAP service.|
|sn\_apm\_sap\_int.odata\_invoices\_service\_subflow|Defines the subflow responsible for fetching invoices via SAP OData services.|

-   **[Use a flow or subflow in SAP \(Outbound\)](../task/use-flow-or-subflow-sap.md)**  
A flow or subflow can be executed in SAP using the Workflow Studio. Follow these steps to run a flow or subflow.
-   **[Copy a flow or subflow in SAP](../task/copy-flow-or-subflow-sap.md)**  
You can create a copy of the flow or subflow and make the necessary modifications. Use the following steps to activate a flow or subflow.

**Parent Topic:**[Use Source-to-Pay integration with SAP](using-source-to-pay-sap-integration.md)

