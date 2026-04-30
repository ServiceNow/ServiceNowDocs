---
title: SAP Ariba Spoke
description: The SAP Ariba spoke is built by Bristlecone, Inc. Manage the primary and transactional data of buying and sourcing suites in the SAP Ariba instance from your ServiceNow instance. The SAP Ariba system offers a single SaaS offering edition and the SAP Ariba spoke works as-is irrespective of the datacenter chosen.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-06"
reading_time_minutes: 19
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# SAP Ariba Spoke

The SAP Ariba spoke is built by Bristlecone, Inc. Manage the primary and transactional data of buying and sourcing suites in the SAP Ariba instance from your ServiceNow instance. The SAP Ariba system offers a single SaaS offering edition and the SAP Ariba spoke works as-is irrespective of the datacenter chosen.

**Important:** The SAP Ariba spoke uses the ITK-style service \(file upload or file download\) REST APIs via MIME multi-part format, and not ITK jar. So, although SAP Ariba announced [end of life](https://support.ariba.com/item/view/KB0547223) of ITK jar by Dec 31st, 2023, which resulted in the removal of ITK from the SAP download site and SAP Portal, there is no functionality impact to the existing SAP Ariba spoke.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Starting on March 1st 2022, all SAP spokes will be available only on the Store.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SAP Ariba spoke v1.14.0 is the latest version.

## Supported versions

This spoke was built for SAP Ariba v2.0, but may be compatible with later versions.

## Spoke requirements

-   Enable file upload or file download REST services by creating a shared secret. Copy and record the integration password for later use.

    **Note:** If you want to create two shared secrets, one for sourcing suite and another for buying a suite, you must provide the same shared secret.

    -   To create a shared secret for sourcing suite, navigate to **Administration** in your SAP Ariba solution.
    -   To create a shared secret for buying a suite, navigate to **Core Administration** in your SAP Ariba solution.
    To create a new shared secret:

    1.  Log in to your SAP Ariba solution.
    2.  Select **Manage** in the navigation menu.
    3.  Select **Core Administration** or **Administration**.
    4.  Select the expansion arrow for **Integration Manager**.
    5.  Select **Integration Toolkit Security**.
    6.  In **Shared Secret Authentication**, enter integration password in **Integration password**.
    7.  Select **Save**.
    For more information, see [Security Configuration for Master Data Integration](https://help.sap.com/docs/strategic-sourcing/common-data-import-and-administration-guide-for-sap-strategic-sourcing-solutions-and-sap-ariba-supplier-management-solutions/security-configuration-for-master-data-integration?q=Integration%20toolkit%20security) in [SAP Help Portal](https://help.sap.com/docs/).

-   Copy and record the realm of your SAP Ariba instance.
-   In **Administration**, create an inbound endpoint in **End Point Configuration** under **Integration Manager**. Copy and record the login password that you have provided under **HTTP Authentication**. For information about creating an endpoint, see [Configure the SAP Ariba Solution](https://help.sap.com/docs/btp/sap-btp-neo-environment/configure-sap-ariba-solution) in [SAP Help Portal](https://help.sap.com/viewer/index).

    To create an integration end point in your SAP Ariba solution:

    1.  Log in to your SAP Ariba solution.
    2.  Select **Manage** in the navigation menu.
    3.  Select **Administration**.
    4.  Select the expansion arrow for **Integration Manager**.
    5.  Select **End Point Configuration**.
    6.  Select **Create New**.
    7.  On the End Point Configuration - Create End Point page, enter a name for the end point in **Name** and select **Inbound** for **Type**.
    8.  In the **HTTP Authentication** section, enter a user ID in the **Login** field and a password in the **Password** field.

        You need the user ID and password to authenticate your HTTP calls later.

    9.  Select **Save**.
    Enable SOAP service of the Import Sourcing Project task for your inbound endpoint in **Integration Configuration** under **Integration Manager**.

    -   Copy and record the URL in the Integration Task **URL** field.
    -   Open the WSDL file. Copy and record the value of the **targetNamespace** parameter.
    For information about Integration Task **URL** and **targetNamespace**, see [Configure the SAP Ariba Solution](https://help.sap.com/docs/btp/sap-btp-neo-environment/configure-sap-ariba-solution) in [SAP Help Portal](https://help.sap.com/docs/).

    To enable an integration task and link it to an existing end point:

    1.  Log in to your SAP Ariba solution.
    2.  Select **Manage** in the navigation menu.
    3.  Select **Administration**.
    4.  Select the expansion arrow for **Integration Manager**.
    5.  Select **Integration Configuration**.
    6.  Locate the task that you want to enable.

        Select **List All** or enter search criteria.

    7.  Select **Search**.
    8.  Select **Actions** and select **Edit** for the required task.
    9.  In the Edit data import/export task page, select **Enabled** for **Status**.
    10. For **End point**, select the required end point.
    11. Select **Save**.
-   In **Core Administration**, create an inbound endpoint in **End Point Configuration** under **Integration Manager**. Copy and record the login password that you have provided under **HTTP Authentication**. For information about creating an endpoint, see [Configure the SAP Ariba Solution](https://help.sap.com/docs/btp/sap-btp-neo-environment/configure-sap-ariba-solution) in [SAP Help Portal](https://help.sap.com/docs/).

    To create an integration end point in your SAP Ariba solution:

    1.  Log in into your SAP Ariba solution.
    2.  Select **Manage** in the navigation menu.
    3.  Select **Core Administration**.
    4.  Select the expansion arrow for **Integration Manager**.
    5.  Select **End Point Configuration**.
    6.  Select **Create New**.
    7.  On the End Point Configuration - Create End Point page, enter a name for the end point for **Name**.
    8.  Select **Inbound** for **Type**.
    9.  In the **HTTP Authentication** section, enter a user ID in the **Login** field and a password in the **Password** field.

        You need the user ID and password to authenticate your HTTP calls later.

    10. Select **Save**.
    Enable SOAP service of the Import Suppliers task for your inbound endpoint in **Integration Configuration** under **Integration Manager**.

    -   Copy and record the URL in the Integration Task **URL** field.
    -   Open the WSDL file. Copy and record the value of the **targetNamespace** parameter.
    To enable an integration task and link it to an existing end point:

    1.  Log in into your SAP Ariba solution.
    2.  Select **Manage** in the navigation menu.
    3.  Select **Core Administration**.
    4.  Select the expansion arrow for **Integration Manager**.
    5.  Select **Integration Configuration**.
    6.  Locate the task that you want to enable.

        Select **List All** or enter search criteria.

    7.  Select **Search**.
    8.  Select **Actions** and select **Edit** for the required task.
    9.  In the Edit data import/export task page, select **Enabled** for **Status**.
    10. For **End point**, select the required end point.
    11. Select **Save**.
    For information about Integration Task **URL** and **targetNamespace**, see [Configure the SAP ARiba Solution](https://help.sap.com/docs/btp/sap-btp-neo-environment/configure-sap-ariba-solution) in [SAP Help Portal](https://help.sap.com/docs/).


## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Flow Designer Action Step - Script on MID \(com.glide.hub.action\_step.script\_mid\)
-   [Utility Actions Spoke](utilityact-spoke.md)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The SAP Ariba spoke provides sample flows to demonstrate automating the SAP Ariba tasks. To customize a sample flow, copy it to the required application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Import Supplier Organizations Buyer|Imports supplier organizations from ServiceNow to the buying suite of your SAP Ariba instance.|
|Import Supplier Organizations Sourcing|Imports supplier organizations from ServiceNow to the sourcing suite of your SAP Ariba instance.|

## Spoke subflows

The SAP Ariba spoke provides sample subflows to demonstrate the sequence of reusable actions in a flow. To customize the sample subflows, copy them to the required application scope.

|Subflow|Description|
|-------|-----------|
|Look up Export Task - Subflow v2 \(Xanadu and Beyond\)|Searches for the export task event ZIP file, copies the ZIP file to an SFTP location. Then the file is unzipped and the unzipped XLS or CSV files are copied to the specified ServiceNow table record.|
|Update Requisition sample subflow|Updates the requestions specified in the payload.|
|Create Requisition sample subflow|Creates a requisition record after verifying that a requestion with the specified requisition details does not exist.|

**Note:** The sample subflow requires a server host, port, and working directory.

## Spoke actions

The SAP Ariba spoke provides actions to automate SAP Ariba tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Export Management|Copy Ariba File To Data Source|Takes sys ID of the source record and transfers the attachment to the target data source.|
|Import Management|Execute Ariba Import Task|Triggers the SAP Ariba import task for the specified operation.|
|Look up Export Task|Executes an Ariba export task event where a ZIP file is received as response and stored to the selected data source.|
|Invoice Management|Look up Invoices CXML|Retrieves invoices from SAP business network in cXML format.|
|Look up Pending Messages ID CXML|Retrieves the pending messages ID in CXML format.|
|Reject Invoice CXML|Rejects the specified invoice submitted by suppliers in SAP business network.|
|Approvals Procurement Management|Look up Approvals Status|Retrieves tasks that are pending for approval.|
|Look up Downstream Approvals Stream|Retrieves details related to the approvable invoices or requisitions.|
|Update Downstream Approval Status|Retrieves the details of approval entities.|
|Approval Sourcing Management|Create Approval Status|Performs the specified action on an entity. Possible values for the entity task are Approve, Deny, and DenyWithResubmit.|
|Look up Approval Entities|Retrieves the details of approval entities.|
|Buyer Management|Look up Purchase Order Lines Stream|Retrieves information from line items in purchase orders for a specified buyer.|
|Look up Purchase Orders Stream|Retrieves header information in purchase orders for a specified buyer.|
|Look up Shipment Notice Items Stream|Retrieves details of all the items in the shipment notice.|
|Look up Shipment Notices Stream|Retrieves shipment related data including delivery, transport, and supplier details.|
|Procurement Export Management|Look up Downstream Supplier Locations|Initiates an Ariba export process, prompting the system to generate and deliver a ZIP file which contains essential data stored as a response within the user's selected data source.|
|Look up Receipts|Initiates an Ariba export process, prompting the system to generate and deliver a ZIP file which contains essential data stored as a response within the user's selected data source.|
|Procurement Import Management|Import Downstream Supplier|Creates or updates supplier details in Ariba system along with supplier location and supplier remittance location.|
|Receipt Management|Create Receipt|Creates receipt or import receipt from external applications.|
|Requisition Management \(SOAP-based\)|Create Requisition|Creates a requisition record with the provided details.|
|Update Requisition|Updates a requisition record with the specified information.|
|Cancel requisition|Cancels a requisition record with the details provided.|
|Procurement Management \(REST-based\)|Look up Conversion Rates Stream|Retrieves details related to conversion rates.|
|Look up Cost Centers Stream|Retrieves cost centers details from SAP ARIBA REST.|
|Look up Currency Rates Stream|Retrieves details related to the currency rates.|
|Look up Fixed Assets Stream|Retrieves fixed assets details from SAP ARIBA REST.|
|Look up GL Accounts Stream|Retrieves details of the available primary data entities.|
|Look up Legal Entities Stream|Retrieves metadata for legal entity.|
|Look up Material Groups Stream|Retrieves the primary data of material group from SAP Ariba.|
|Look up Materials Stream|Retrieves the general data of materials in SAP Ariba REST.|
|Look up Payment Terms Stream|Retrieves details of the available primary data entities.|
|Look up Purchase Groups Stream|Retrieves purchase group details from SAP system.|
|Look up Purchasing Organizations Stream|Retrieves purchasing organization details from SAP ARIBA REST.|
|Look up Upstream Supplier Locations Stream|Retrieves the primary data of supplier locations.|
|Sourcing Event Management|Create Award Scenario|Creates an award scenario with the provided details.|
|Create Event Line Items|Adds line items to the specified event and sets term values as specified.|
|Create Event Questions|Adds questions to the specified event and sets term values as specified.|
|Create Item Attachments|Uploads a file as an attachment for the specified item and term in the specified event. The item and term must exist. The event state must be **Draft**.|
|Create Sourcing Event|Initiates the process of creating a sourcing event, such as a request for proposal \(RFP\), within the SAP Ariba Event Management.|
|Create Supplier Award|Awards the supplier by recognizing their successful proposal.|
|Create Supplier Invitations|Invites multiple suppliers to the specified event.|
|Delete Supplier Invitations|Deletes multiple suppliers for the specified event.|
|Download Attachment from Supplier Bid Responses|Retrieves details of the supplier response.|
|Look up Awarded Bids|Retrieves details of the awarded bids for an event.|
|Look up Event Templates|Retrieves sourcing template IDs and other template details, including item definitions.|
|Look up Supplier Bids|Retrieves supplier bids for an event.|
|Update Event State|Modifies an event's state using its unique identifier that is, Event ID.|
|Supplier Management|Create Sourcing Project|Creates a sourcing project with the provided details.|
|Update Sourcing Project|Updates the project header fields of an existing sourcing project.|
|Sourcing Management \(REST-based\)|Look up Departments Stream|Retrieves the department primary data available in the system.|
|Supplier Management \(REST-based\)|Look up Downstream Remittance Location Stream|Retrieves details of the available master data entities.|
|Look up Downstream Suppliers Stream|Retrieves details related to the suppliers.|
|Supplier Management \(SOAP-based\)|Create Suppliers|Creates a supplier with the provided details.|
| |Look up Upstream Suppliers Stream|Retrieves the general data of the primary supplier.|
|Contract Management|Create Contract|Creates contracts with the provided details, in contract workspaces.|
|Look up Contracts Stream|Retrieves details related to contract workspaces. |
|Async Reporting Job Management|Create Job|Creates the job to retrieve the record for PO and PR.|
|Look up Job Status|Retrieves details of the required job.|
|Look up transactions|Retrieves the requisition and purchase order details based on **Job ID** and **File Name**.|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|SAP Ariba approvals procurement management AI agent|Manages procurement approvals and workflows within SAP Ariba. This AI agent enables users to track approval statuses, streamline procurement processes, and maintain operational control through seamless integration with SAP Ariba.|
|SAP Ariba sourcing event management AI agent|Manages sourcing events and supplier-related processes within SAP Ariba. This AI agent supports tasks such as handling supplier bids, managing award scenarios, and updating event states, helping procurement teams and sourcing managers optimize workflows and improve operational efficiency.|
|SAP Ariba invoice management AI agent|Manages invoice-related tasks within SAP Ariba. This AI agent enables users to look up pending message IDs and retrieve invoice details, helping streamline invoice management and improve operational efficiency in SAP Ariba environments.|
|SAP Ariba procurement export management AI agent|Manages procurement export tasks and SAP Ariba integration within IntegrationHub. This AI agent provides capabilities such as looking up receipts to streamline procurement processes and enhance operational efficiency. It is ideal for procurement managers, integration specialists, and business users who need seamless access to SAP Ariba data and actions.|
|SAP Ariba approvals sourcing management AI agent|Manages approval workflows and sourcing management processes within SAP Ariba. This AI agent can perform actions such as creating approval statuses to streamline approvals and sourcing activities, helping users enhance efficiency in SAP Ariba integrations and approvals management.|

## Available sample agentic workflows

Install Now Assist for Integration Hub and start using the available sample agentic workflows and AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. Use the available sample agentic workflow in AI Agent Studio so that AI agents can coordinate to solve complex problems. To modify the available sample agentic workflow as per your requirement, see [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Available sample agentic workflow includes:

<table id="table_v11_v4w_c3c"><thead><tr><th>

Sample agentic workflow

</th><th>

Description

</th><th>

AI agents used

</th><th>

Always ON by default?

</th></tr></thead><tbody><tr><td>

Approval Status Lookup and Creation

</td><td>

Identifies the user’s approval-related intent, validates employee identity, executes the required SAP Ariba approval actions, and returns a single consolidated, HR-focused summary of the results.

</td><td>

 

</td><td>

No**Note:** To activate the workflow, see [Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

</td></tr></tbody>
</table>## Spoke module

The SAP Ariba spoke adds the SAP Ariba Spoke application to your instance and includes these modules:

<table id="table_hr4_vjq_xmb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ariba Export Configuration Definition

</td><td>

Displays the list of available export configurations. By default, 33 export configurations are available along with the spoke. You can modify the default export configuration or create export configurations, according to requirements.For example, if you have used the Execute Ariba Export Task action in your flow to export receipts, data is retrieved from your SAP Ariba instance to ServiceNow instance. You must copy these records to data source. Otherwise, the records are deleted after the time period mentioned in the Ariba Export Task Scheduler scheduled script has lapsed. You can use the Copy Ariba File To Data Source action in your flow to copy the record to your data source.

</td></tr><tr><td>

Ariba Export Task Execution

</td><td>

Displays the CSV files generated when data is exported from your SAP Ariba instance to ServiceNow instance. You must copy these records to data source. Otherwise, the records are deleted after the time period mentioned in the Ariba Export Task Scheduler scheduled script has lapsed.

</td></tr><tr><td>

Ariba Import Configuration Definition

</td><td>

Displays the list of available import configurations. By default, two import configurations are available along with the spoke. You must use Execute Ariba Import Task action in your flow to create the required records.-   If you have selected the **MasterDataBatchPull** task in the Execute Ariba Import Task action, the primary data records for the sourcing suite are created or updated in your SAP Ariba instance.
-   If you have selected the **CombinedDataPull** task in the Execute Ariba Import Task action, the primary data records for the buying suite are created or updated in your SAP Ariba instance.

</td></tr><tr><td>

Supplier IDs Buyer

</td><td>

Displays information about the suppliers in the buying suite. Admin must create the supplier records here.The Look Up Supplier IDs Buyer Records action in the Import Supplier Organizations Buyer sample flow uses these records to run the flow.

</td></tr><tr><td>

Supplier IDs Sourcing

</td><td>

Displays information about the suppliers in the sourcing suite. An admin must create the supplier records here.The Look Up Supplier IDs Sourcing Records action in the Import Supplier Organizations Sourcing sample flow uses these records to run the flow.

</td></tr><tr><td>

Supplier Organizations Buyer

</td><td>

Displays information about the supplier organizations in the buying suite. Admin must create records here.The Look Up Supplier Organizations Buyer Records action in the Import Supplier Organizations Buyer sample flow uses these records to run the flow.

</td></tr><tr><td>

Supplier Organizations Sourcing

</td><td>

Displays information about the supplier organizations in the sourcing suite. An admin must create records here.The Look Up Supplier Organizations Sourcing Records action in the Import Supplier Organizations Sourcing sample flow uses these records to run the flow.

</td></tr></tbody>
</table>Data accessed through these spoke modules is stored in these tables:

|Table|Description|
|-----|-----------|
|Ariba Export Configuration Definition \[sn\_sap\_ariba\_spoke\_ariba\_file\_definition\]|Stores information about the export configurations.|
|Ariba Import Configuration Definition \[sn\_sap\_ariba\_spoke\_ariba\_import\_configuration\_definition\]|Stores information about the import configurations.|
|Ariba Export Task Execution \[sn\_sap\_ariba\_spoke\_ariba\_task\_execution\]|Stores information about the CSV files generated when data is exported from your SAP Ariba instance to ServiceNow instance.|
|Supplier Organizations Sourcing \[sn\_sap\_ariba\_spoke\_import\_supplier\_organizations\_csv\]|Stores information about the supplier organizations in the sourcing suite. Admin must create these records in the Supplier Organizations Sourcing module.|
|Supplier IDs Sourcing \[sn\_sap\_ariba\_spoke\_supplier\_ids\]|Stores information about the suppliers in the sourcing suite. Admin must create these records in the Supplier IDs Sourcing module.|
|Supplier IDs Buyer \[sn\_sap\_ariba\_spoke\_supplier\_ids\_buyer\]|Stores information about the suppliers in the buying suite. Admin must create these records in the Supplier IDs Buyer module.|
|Supplier Organizations Buyer \[sn\_sap\_ariba\_spoke\_supplier\_organizations\]|Stores information about the supplier organizations in the buying suite. Admin must create these records in the Supplier Organizations Buyer module.|

## Spoke scheduled script and system property

A scheduled script, Ariba Export Task Scheduler, and system property, **sn\_sap\_ariba\_spoke.ariba.export.task.scheduler**, are available along with the spoke. The system property defines the number of days by which all the records older than this will be purged. The script uses this value to purge the records that have not been copied to the data source.

-   To view the scheduled script, enter `sysauto_script_list.do` in the filter navigator and search for the script, Ariba Export Task Scheduler.
-   To view the system property, navigate to **System Properties** &gt; **All Properties** and search for the system property, **sn\_sap\_ariba\_spoke.ariba.export.task.scheduler**.

You can configure the scheduled script and system property according to your requirement.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

These connection and credential alias records are available along with the spoke:

<table id="table_okf_zzx_dcc"><thead><tr><th>

Connection &amp; Credential Alias

</th><th>

Associated spoke action category

</th></tr></thead><tbody><tr><td>

SAP\_Ariba\_Import

</td><td>

Import Management

</td></tr><tr><td>

SAP\_Ariba\_Export

</td><td>

Export Management

</td></tr><tr><td>

SAP\_Ariba\_Sourcing

</td><td>

Sourcing Management

</td></tr><tr><td>

SAP\_Ariba\_Suppliers

</td><td>

Supplier Management \(SOAP-based\)

</td></tr><tr><td>

SAP Ariba SSH

</td><td>

SSH Management

</td></tr><tr><td>

SAP Ariba Rest Procurement

</td><td>

Procurement Management \(REST-based\)

</td></tr><tr><td>

SAP Ariba Rest Buyer

</td><td>

Buyer Management

</td></tr><tr><td>

SAP Ariba Rest Sourcing

</td><td>

Sourcing Management \(REST-based\)

</td></tr><tr><td>

SAP Ariba Procurement Export

</td><td>

Procurement Export Management

</td></tr><tr><td>

SAP Ariba Soap Receipts

</td><td>

Receipt Management

</td></tr><tr><td>

SAP Ariba Procurement Import

</td><td>

Procurement Import Management

</td></tr><tr><td>

SAP Ariba Rest Suppliers

</td><td>

Supplier Management \(REST-based\)

</td></tr><tr><td>

SAP Ariba Approvals Procurement

</td><td>

Approvals Procurement Management

</td></tr><tr><td>

SAP Ariba Approvals Sourcing

</td><td>

-   Approvals Sourcing Management
-   Approvals Procurement Management

</td></tr><tr><td>

SAP Ariba Rest Event

</td><td>

Sourcing Event Management

</td></tr><tr><td>

SAP Ariba Rest Ship Notices

</td><td>

Buyer Management

</td></tr><tr><td>

SAP Ariba Soap Requisition

</td><td>

Requisition Management\(SOAP-based\)

</td></tr></tbody>
</table>For information about setting up the spoke, see [Set up the SAP Ariba spoke](../task/setup-sap-ariba.md#).

## MID Server requirements

These actions use REST calls, which can run on an instance or MID Server. Use the connection record associated with the SAP Ariba alias to configure where actions run as well as set MID Server selection attributes. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md)

**Note:** The Linux server that is needed to create the SSH credential record, must be installed in the same network’s machine or virtual machine where your MID Server is installed.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

