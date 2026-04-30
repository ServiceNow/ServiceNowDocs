---
title: Oracle Financial Cloud Spoke
description: Manage invoices, ledger, and records in an Oracle Financial Cloud instance from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Oracle Financial Cloud Spoke

Manage invoices, ledger, and records in an Oracle Financial Cloud instance from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle Financial Cloud spoke v1.5 is the latest version.

## Supported versions

This spoke was built for Oracle Financial Cloud API version 11.13.18.05.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Utility Actions Spoke](utilityact-spoke-1.md)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Oracle Financial Cloud spoke provides sample flows to demonstrate automating the Oracle Financial Cloud tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

<table id="table_dzy_sjk_ymb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Get Accounted AP Invoices

</td><td>

Retrieves information about the accounted AP invoices. This flow triggers the Get Accounted AP Invoice subflow and includes the Look up Record Details action.

</td></tr><tr><td>

Import Journals

</td><td>

Imports the journal records from your ServiceNow instance to Oracle Financial Cloud system.To import the journal records, you must create the required records in the GL Interface module.

</td></tr><tr><td>

Import AP Invoices

</td><td>

Imports accounts payable invoice line and accounts payable invoice records from your ServiceNow instance to Oracle Financial Cloud system. To import the accounts payable invoice line and accounts payable invoice records, you must create the required records in the AP Invoices Interface and AP Invoices Lines Interface modules respectively.

</td></tr></tbody>
</table>**Note:** The success message displayed after flow executions during the data imports from ServiceNow instance to Oracle Financial Cloud system, only indicates that data has been successfully pushed to Oracle Financial Cloud system. You must verify that the data import is successfully completed by accessing the Oracle Financial Cloud system.

## Spoke subflows

The Oracle Financial Cloud spoke provides sample subflow, Get Accounted AP Invoice, to demonstrate automating Oracle Financial Cloud tasks. The subflow retrieves the accounted AP invoice records and is used in the Get Accounted AP Invoices flow. To customize the sample subflow, copy it to a new application scope.

## Spoke actions

The Oracle Financial Cloud spoke provides actions to automate Oracle Financial Cloud tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|All Record Management|Create Record|Creates a record related to the specified object in Oracle Financial Cloud.|
|Delete Record|Deletes a record related to the specified object in Oracle Financial Cloud.|
|Look up Record Details|Retrieves record details in an object.|
|Look up Record Details By ID|Retrieves details of the specified record in an object.|
|Look up Records Stream|Retrieves a list of records related to the specified record or object from Oracle Financial Cloud.|
|Update Record|Updates the record related to the specified object in Oracle Financial Cloud.|
|AP Invoice Management|Import AP Invoices|Imports the actionable payment invoices.|
|Look up AP Invoice Lines|Retrieves information about the accounts payable invoice lines.|
|Look up AP Invoices|Retrieves information about the actionable payment invoices.|
|Currency Conversion|Look up Currency Rates|Retrieves information about the currency rates.|
|General Ledger|Get Code Combinations Details|Retrieves information about the code combinations.|
|Get Subledger Balances|Retrieves information about the subledger balances.|
|Import Journals|Imports details about the journals.|
|Look up Ledger Balance|Retrieves information about the ledger balances.|
|Invoice Management|Look up Invoice Payments Status|Retrieves the status of invoice payment for the specified invoice ID from Oracle Financial Cloud.|
|Update Invoice Payment Status|Updates the status of an existing invoice payment in Oracle Financial Cloud.|
|Metadata Retrieval|Get Object Data for Oracle Cloud Financials|Retrieves the object metadata for the specified object from Oracle Financials Cloud.|
|Get Objects \(Metadata\)|Retrieves the list of all records or objects from Oracle Financial Cloud.|
|Get Object Schema \(Metadata\)|Retrieves all schema or fields related data from Oracle Financial Cloud for the specified object.|
|Get Dynamic Response Schema \(Metadata\)|Retrieves all output schema or fields related data from Oracle Financial Cloud for the specified object.|
|Primary Data Management|Look up HR Locations Stream|Retrieve the list of all locations with the object name "locations".|
|Look up Cost Centers Stream|Retrieves the details of the Cost Centers from the Oracle Financial Cloud.|
|Purchase Order Management|Create Purchase Order and PO Lines|Creates a purchase order and adds associated purchase order lines in Oracle Financial Cloud.|
|Update Purchase Order and PO Lines|Updates an existing purchase order and its associated purchase order lines in Oracle Financial Cloud.|
|Supplier Record Management|Look up Suppliers|Retrieves information about the suppliers.|

## Spoke modules

The Oracle Financial Cloud spoke adds the Oracle Financial Cloud application to your instance and includes these modules:

<table id="table_jzy_sjk_ymb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accounted AP Invoices

</td><td>

Displays information about the accounted AP invoices.This information is retrieved when the Get Accounted AP Invoices flow is triggered.

</td></tr><tr><td>

AP Invoices Interface

</td><td>

Displays the accounts payable invoice records.Admin must create these records in the ServiceNow instance in this module. The Import AP Invoices flow imports these invoices from your ServiceNow instance to Oracle Financial Cloud system.

</td></tr><tr><td>

AP Invoices Lines Interface

</td><td>

Displays the accounts payable invoice line records.Admin must create these records in the ServiceNow instance in this module. The Import AP Invoices flow imports these invoices from your ServiceNow instance to Oracle Financial Cloud system.

</td></tr><tr><td>

BI Report Paths

</td><td>

Displays information about the folder path where the required report is saved. The Get Subledger Balances and Get Code Combinations Details actions retrieve the subledger balances from these folder paths.Admin must create two records for the two actions and specify the folder path in this module.

 ![Folder paths in the BI Report Paths module](../image/bi-report-paths.png)

</td></tr><tr><td>

Get Currency Rates

</td><td>

Displays information about the currency rates.The currency rates are retrieved from the remote table, Get Currency Rates \[sn\_ofc\_spoke\_st\_get\_currency\_rates\]. You can use the remote table as reference and create another remote table for currency rates as per your requirement.

</td></tr><tr><td>

GL Interface

</td><td>

Displays the journal records. The Import Journals flow imports these records from your ServiceNow instance to Oracle Financial Cloud system.Admin must create the required journal records in this module.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

Two connection and credential records are available along with the spoke. You must configure these alias record to use the spoke. See [Set up the Oracle Financial Cloud spoke](../task/setup-oracle-fin-cloud.md#) for more information.

**Note:** Depending on the Oracle Financial Cloud policies and account settings, you may have to change or refresh the credentials in your credential record periodically.

For information about setting up the spoke, see [Set up the Oracle Financial Cloud spoke](../task/setup-oracle-fin-cloud.md#).

