---
title: Use schedule flows in Oracle EBS
description: Use the schedule flows to retrieve information from Oracle EBS, including invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, plant addresses, and legal entities.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Use schedule flows in Oracle EBS

Use the schedule flows to retrieve information from Oracle EBS, including invoices, cost centers, product models, payment terms, purchasing organizations, departments, GL accounts, currencies, FX rates, invoice payment details, suppliers, plant addresses, and legal entities.

You can either use the subflows to perform the required tasks or you can create a copy of the subflows and then customize it according to your requirements.

**Important:**

These subflows are read-only. To modify a flow or subflow, create a copy and then apply the required changes.

The Source-to-Pay with Oracle EBS integration supports the following subflows.

## Primary Data Integration with Oracle

The Primary Data Integration with Oracle supports the following subflows and system properties:

**Subflows for Primary Data Integration with Oracle**

|Subflow|Description|
|-------|-----------|
|Fetch Cost Centers|Use this subflow to lookup cost centers from Oracle EBS.|
|Fetch Product Models|Use this subflow to lookup product models from Oracle EBS.|
|Fetch Payment Terms|Use this subflow to lookup payment terms from Oracle EBS.|
|Fetch Purchasing Orgs|Use this subflow to lookup purchasing orgs from Oracle EBS.|
|Fetch Departments|Use this subflow to lookup departments from Oracle EBS.|
|Fetch GL Accounts|Use this subflow to lookup GL accounts from Oracle EBS.|
|Fetch Currencies|Use this subflow to lookup currencies from Oracle EBS.|
|Fetch FX Currency Rates|Use this subflow to lookup FX rates from Oracle EBS.|
|Fetch Invoice Payment Details|Use this subflow to lookup invoice payment details from Oracle EBS.|
|Fetch Suppliers|Use this subflow to lookup suppliers from Oracle EBS.|
|Fetch Plant Addresses|Use this subflow to lookup plant addresses from Oracle EBS.|
|Fetch Legal Entities|Use this subflow to lookup legal entities or company code details from Oracle EBS.|
|Fetch Invoices|Use this subflow to lookup invoices from Oracle EBS.|

**System Properties for Primary Data Integration with Oracle**

Use these system properties to configure settings for the Primary Data Integration with Oracle from the System Properties page. For more information, see [Source-to-Pay integrations with Oracle reference](../reference/s2p-integration-oracle-reference.md).

Role required:

-   **Read Role**: sn\_shop.procurement\_specialist, sn\_shop.shopper, sn\_fcms\_intg.admin
-   **Write Role**: sn\_fcms\_intg.admin

<table id="table_zhx_grm_nhc"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_orcl\_data\_int.action\_default\_page\_size

</td><td>

Oracle EBS action's default page size.

</td></tr><tr><td>

sn\_orcl\_data\_int.common\_object\_details\_service\_flow\_name

</td><td>

Use this subflow to look up common object details in Oracle.

</td></tr><tr><td>

sn\_orcl\_data\_int.cost\_centers\_service\_flow\_name

</td><td>

Use this subflow for fetching cost centers from the Oracle system.

</td></tr><tr><td>

sn\_orcl\_data\_int.currencies\_service\_flow\_name

</td><td>

Use this subflow for fetching currencies from Oracle EBS system.

</td></tr><tr><td>

sn\_orcl\_data\_int.fetch\_purchasing\_organizations\_service\_flow\_name

</td><td>

Use this subflow for fetching purchasing organizations from the Oracle system.

</td></tr><tr><td>

sn\_orcl\_data\_int.full\_load\_time\_range\_default

</td><td>

Defines the default time range for full data loads.

</td></tr><tr><td>

sn\_orcl\_data\_int.fx\_rates\_service\_flow\_name

</td><td>

Use this subflow for fetching FX rates from the Oracle system.

</td></tr><tr><td>

sn\_orcl\_data\_int.glide.rest.max\_content\_length

</td><td>

Defines the maximum content length allowed for REST API payloads.

</td></tr><tr><td>

sn\_orcl\_data\_int.gl\_account\_service\_flow\_name

</td><td>

Use this subflow for fetching GL accounts from the Oracle system.

</td></tr><tr><td>

sn\_orcl\_data\_int.inventory\_items\_flow\_name

</td><td>

Use this subflow for fetching inventory items from the Oracle system.

</td></tr><tr><td>

sn\_orcl\_data\_int.legal\_entities\_service\_flow\_name

</td><td>

Use this subflow for fetching legal entities from the Oracle system.

</td></tr><tr><td>

sn\_orcl\_data\_int.payment\_terms\_service\_flow\_name

</td><td>

Use this subflow for fetching payment terms from the Oracle system.

</td></tr><tr><td>

sn\_orcl\_data\_int.plant\_address\_flow\_name

</td><td>

Use this subflow for fetching plant address from the Oracle system.

</td></tr><tr><td>

sn\_orcl\_data\_int.purchase\_groups\_service\_flow\_name

</td><td>

Use this subflow for fetching purchase groups from the Oracle system.

</td></tr><tr><td>

sn\_orcl\_data\_int.supplier\_service\_flow\_name

</td><td>

Use this subflow for fetching suppliers from the Oracle system.

</td></tr><tr><td>

sn\_orcl\_data\_int.timeout\_value

</td><td>

Maximum timeout duration \(in milliseconds\) for subflow execution.Default value: 10000000

</td></tr></tbody>
</table>## Supplier Lifecycle Operations Integration with Oracle

The Supplier Lifecycle Operations Integration with Oracle supports the following subflows:

|Flow|Description|
|----|-----------|
|Create or update or deactivate supplier|Creates or updates or deactivates supplier in Oracle EBS.|
|Create or update supplier location|Creates or updates supplier location in Oracle EBS.|
|Create or update supplier payment information|Creates or updates supplier payment information in Oracle EBS.|

**Important:**

These subflows are read-only. To modify a flow or subflow, create a copy and then apply the required changes.

**System Properties for Supplier Lifecycle Operations Integration with Oracle**

Use these system properties to configure settings for the Supplier Lifecycle Operations Integration with Oracle from the System Properties page. For more information, see [Source-to-Pay integrations with Oracle reference](../reference/s2p-integration-oracle-reference.md).

Role required:

-   **Read Role**: sn\_shop.procurement\_specialist, sn\_shop.shopper, sn\_fcms\_intg.admin
-   **Write Role**: sn\_fcms\_intg.admin

|Property Name|Description|
|-------------|-----------|
|sn\_slo\_orcl\_int.supplier\_location\_service\_flow\_name|Use this subflow to fetch supplier location data from the Oracle system.|
|sn\_slo\_orcl\_int.supplier\_payment\_service\_flow\_name|Use this subflow to fetch supplier payment information from the Oracle system.|
|sn\_slo\_orcl\_int.supplier\_service\_flow\_name|Use this subflow to fetch supplier data from the Oracle system.|

## Sourcing and Procurement Operations Integration with Oracle EBS

The Sourcing and Procurement Operations Integration with Oracle EBS supports the following subflows:

|Flow|Description|
|----|-----------|
|Create or updates or cancels purchase order|Creates or updates or cancels purchase order in Oracle EBS.|

## Accounts Payable Operations Integration with Oracle EBS

The Accounts Payable Operations Integration with Oracle EBS supports the following subflows:

|Flow|Description|
|----|-----------|
|Create AP invoice|Creates AP invoice in Oracle EBS.|

-   **[Manually trigger flows or subflows in Oracle EBS \(Inbound\)](../task/manually-trigger-subflows-oracle-ebs.md)**  
You can manually trigger flows or subflows in Oracle EBS on demand. Follow these steps to manually trigger a flow or subflow.
-   **[Use a flow or subflow in Oracle EBS \(Outbound\)](../task/use-flow-or-subflow-oracle-ebs.md)**  
A flow or subflow can be executed in Oracle EBS using the Workflow Studio. Follow these steps to run a flow or subflow.
-   **[Copy a flow or subflow in Oracle EBS](../task/copy-flow-or-subflow-oracle-ebs.md)**  
You can create a copy of the a flow or subflow and make the necessary modifications. Use the following steps to activate a flow or subflow.

**Parent Topic:**[Use Source-to-Pay integration with Oracle EBS](using-source-to-pay-oracle-ebs-integration.md)

