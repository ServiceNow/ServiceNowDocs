---
title: SAP Fieldglass Spoke
description: The SAP Fieldglass spoke is built by Bristlecone, Inc. Manage job postings, workers, timesheets and expenses, and approvals in SAP Fieldglass account from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SAP Fieldglass Spoke

The SAP Fieldglass spoke is built by Bristlecone, Inc. Manage job postings, workers, timesheets and expenses, and approvals in SAP Fieldglass account from your ServiceNow instance.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). Starting on March 1st 2022, all SAP spokes will be available only on the Store.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SAP Fieldglass spoke v1.2.1 is the latest version.

## Supported versions

This spoke was built for SAP Fieldglass v2.0, but may be compatible with later versions.

**Note:** SAP Fieldglass APIs doesn’t support JSON by default. You must reach out to the SAP Fieldglass support to enable JSON support for the APIs.

## Spoke requirements

-   Copy and record the API Key. Contact the SAP Fieldglass support team if you don't have the value.
-   By default, all APIs are not enabled. Contact the SAP Fieldglass support team to enable these APIs and enable JSON support for these APIs:

    |API Type|API|
    |--------|---|
    |Job Posting|Job Posting Upload|
    |Job Posting Update Upload|
    |Job Posting Redistribution Upload|
    |Job Posting Cost Center Allocation Upload|
    |Standard Job Posting Qualification Upload|
    |Job Posting Close Upload|
    |Job Seeker Reject Upload|
    |Supplier Job Posting|Get Job Posting|
    |Submit Job Seeker|
    |Work Order Management|Work Order Upload|
    |Work Order Revision Upload|
    |Work Order Close Upload|
    |Supplier - Work Order|Get Work Order Offer|
    |Accept Work Order Offer|
    |Accept Work Order Multiple Rate|
    |Decline Work Order Offer|
    |Accept Work Order Revision|
    |Decline Work Order Revision|
    |Workers|Active Worker Delta Single Line Download \(LastRundate\)|
    |Active Worker Download|
    |Time Sheet and Expense|Time Sheet Upload|
    |Expense sheet Upload|
    |Approved Expense sheet download \(LastRundate\)|
    |Approved Timesheet Fixed Format Download \(LastRundate\)|
    |Time Sheet Rejection Upload|
    |Approvals and Rejection|approvals|
    |Master Data|Supplier Download|
    |Reason Code Download|
    |Business unit Download|
    |Cost center Download|
    |Legal Entity Download|
    |Shift Download|
    |Rate Schedule Download|
    |Site Details Download|


## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   Encryption Support \(com.glide.encryption\)
-   Key Management Framework plugin \(com.glide.kmf.global\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The SAP Fieldglass spoke provides sample flows to demonstrate automating the tasks. To customize a sample flow, copy it to the required application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Sample Look up Approval and Metadata Flow|Approves the pending approvals in SAP Fieldglass.|
|Sample Look up Flow|Retrieves or downloads data related to currently active workers and data related to workers who had revisions since the last successful run date of the connector.|

## Spoke actions

The SAP Fieldglass spoke provides actions to automate  tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Buyer - Approvals and Rejection|Approve|Approves the pending approvals in SAP Fieldglass.|
|Look up Pending Approvals|Retrieves the list of pending approvals.|
|Look up Reject Reasons|Retrieves the list of available reject reasons.|
|Reject|Rejects the pending approvals in SAP Fieldglass.|
|Buyer - Job Posting|Close Job Posting|Closes the specified job posting in SAP Fieldglass.|
|Close Job Posting Bulk|Closes multiple job postings in SAP Fieldglass.|
|Create Job Posting|Creates a job posting in SAP Fieldglass.|
|Reject Job Seeker|Rejects the specified job seeker in SAP Fieldglass.|
|Reject Job Seeker Bulk|Rejects multiple job seekers in SAP Fieldglass.|
|Update Job Posting|Updates details of the required job posting.|
|Update Job Posting Cost Center Allocation|Updates the cost center code for the existing job posting.|
|Update Job Posting Cost Center Allocation Bulk|Updates the cost center code for multiple existing job postings.|
|Update Job Posting Distribution|Distributes single or bulk job posting to the suppliers.|
|Update Job Posting Qualification|Updates or uploads one or more job posting templates or qualifications data for the required job posting.|
|Buyer - Time Sheet and Expense|Look up Approved Expense Sheets|Retrieves details of the approved expense sheets.|
|Look up Approved Time Sheets|Retrieves details of the approved time sheet.|
|Reject Time Sheet Bulk|Rejects single or bulk time sheet.|
|Upload Expense Sheet|Uploads expense sheet in SAP Fieldglass.|
|Upload Time Sheets|Uploads time sheets in SAP Fieldglass.|
|Buyer - Work Order Management|Close Work Order|Closes a work order if workers have not been on-boarded.|
|Revise Work Order|Revises the specified work order in SAP Fieldglass.|
|Upload Work Order|Uploads work order to SAP Fieldglass.|
|Buyer - Workers|Look up Active Workers|Retrieves or downloads data related to currently active workers.|
|Look up Active Workers Delta|Retrieves or downloads data related to workers who had revisions since the last successful run date of the connector.|
|Upload SOW Worker|Uploads or creates an SOW Worker for the existing Statement Of Work.|
|Metadata Retrieval|Get Buyer Token|Generates access token for SAP Fieldglass buyer.|
|Get Supplier Token|Generates access token for the SAP Fieldglass supplier.|
|Last Run Date|Retrieves the required data after the last run date.|
|Look up Business Units|Retrieves list of the available business units.|
|Look up Cost Centers|Retrieves list of the available Cost Centers.|
|Look up Legal Entities|Retrieves list of the available legal entities.|
|Look up Rate Schedules|Retrieves list of the available rate schedules.|
|Look up Reason Codes|Retrieves list of the available reason codes.|
|Look up Shift Details|Retrieves list of the available shifts.|
|Look up Site Details|Retrieves list of the available sites.|
|Look up Suppliers|Retrieves list of the available suppliers.|
|Sample JSON Parser Action|Parses the JSON object and converts it to an array of objects.|
|Supplier - Job Posting|Get Job Posting|Retrieves details of the required job posting.|
|Submit Job Seeker|Submits a job seeker in SAP Fieldglass.|
|Supplier - Work Order|Accept Work Order Multiple Rates|Accepts work order multiple rates in SAP Fieldglass.|
|Accept Work Order Offer|Accepts work order in SAP Fieldglass.|
|Accept Work Order Revision|Accepts the revised work order in SAP Fieldglass.|
|Accept Work Order Revision Multiple Rates|Accepts the revised Work order with multiple Rates.|
|Decline Work Order Offer|Declines the specified work order.|
|Decline Work Order Revision|Declines the revised work order.|
|Get Work Order Offer|Retrieves details of the required work order.|

## Spoke modules

The SAP Fieldglass spoke adds the SAP Fieldglass Spoke application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|Active Worker Downloads|Displays details of the active workers. Data is retrieved when you run the Look up Active Workers spoke action.|
|Create Job Postings|Displays details about the job postings. Data is retrieved from the SAP Fieldglass instance after you set up the webhook. For more information, see [Set up webhook for the SAP Fieldglass spoke](../task/fieldglass-webhk.md).|
|SAP Fieldglass Buyer Credentials|Displays the buyer credential records.|
|SAP Fieldglass Modules|Displays details about the modules. The spoke actions internally use these modules during flow execution. You can manage the modules as per your requirement.|
|SAP Fieldglass Supplier Credentials|Displays the supplier credential records.|
|SAP Fieldglass Webhook Registries|Displays the webhook registries. You can create webhook registry for an event as per your requirement. For more information, see [Set up webhook for the SAP Fieldglass spoke](../task/fieldglass-webhk.md).|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.

Two connection and credential aliases are available along with spoke; one record for supplier and another record for buyer. For information about setting up the spoke, see [Set up the SAP Fieldglass spoke](../task/fieldglass-setup.md).

