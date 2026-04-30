---
title: Mastercard Spoke
description: Integrate ServiceNow instance with your Mastercard account to enable access to Mastercard's API suite, Mastercom and Mastercom Extended, for card dispute resolution. This integration enables you to perform tasks such as searching transactions, creating claims, and processing chargebacks.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Mastercard Spoke

Integrate ServiceNow instance with your Mastercard account to enable access to Mastercard's API suite, Mastercomand Mastercom Extended, for card dispute resolution. This integration enables you to perform tasks such as searching transactions, creating claims, and processing chargebacks.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Subscription information

This spoke requires a subscription. Contact your ServiceNow account manager or sales representative for subscription details. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf)

## Spoke version

Mastercard Spoke v2.0.1 is the latest version.

## Supported version

This spoke was built for Mastercom v6.

## Key features

Mastercard Spoke enables a flow designer to build workflows using actions that invoke Mastercomand Mastercom Extended. This includes the ability to:

-   Search transactions
-   Create claims and chargebacks
-   Collaborate with merchants to prevent chargebacks
-   Monitor disputes throughout the dispute lifecycle
-   Expedite the end-to-end dispute management process
-   Manage disputes for cleared Single Message System original transactions with Mastercom Extended

## Spoke requirements

Mastercard configuration details such as, certificate, key alias, consumer key, and keystore password.

## Spoke dependencies

Ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Mastercard Spoke provides actions to simplify card dispute resolution. Available actions include:

-   **Actions with sensitive information** - These actions contain sensitive information in the request and response body. When using Mastercom/Mastercom Extended APIs, it is recommended to use a Tokenization solution. This involves using a request builder to securely create requests and a response parser to handle encrypted API responses.

    |Category|Action|Description|
    |--------|------|-----------|
    |Transactions|Look up Authorization Details of Transaction Request Builder|Allows the issuers to look up authorization details for the original transaction involved in the claim after the issuer creates a claim.|
    |Look up Authorization Details of Transaction Response Parser|
    |Look up clearing Details of Transaction Request Builder|Allows the issuers to retrieve clearing details for the original transaction involved in the claim. Acquirers may also use this to retrieve clearing details associated with an original transaction.|
    |Look up Clearing Details of Transaction Response Parser|
    |Look up Transactions Request Builder|Allows the issuers to search for information about an original transaction. An issuer may use this information to take an action on the original transaction, such as creating a claim.|
    |Look up Transactions Response Parser|
    |Claims|Look up Claims in a Queue Request Builder|Allows the issuers to retrieve a list of claims in the queue within the date interval request builder.|
    |Look up Claims in a Queue Response Parser|
    |Look up Claim Details by Claim ID Request Builder|Allows the issuers and acquirers to retrieve details for an existing claim, including any cases with which the claim is associated.|
    |Look up Claim Details by Claim ID Response Parser|

    |Category|Action|Description|
    |--------|------|-----------|
    |Mastercom Extended - Claim Management|Look up Claim Details by ID Request Builder - Extended|Request Builder produces the request payload for this action. Use this endpoint to retrieve details for an existing claim.|
    |Look up Claim Details by ID Response Parser - Extended|Parses the response from the search. Use this endpoint to retrieve details for an existing claim.|
    |Look up Claim Details Request Builder - Extended|Request Builder produces the request payload for this action. Use this endpoint to retrieve a list of claims.|
    |Look up Claim Details Response Parser - Extended|Parses the response of the searchClaim. Use this endpoint to retrieve a list of claims.|
    |Mastercom Extended - Transaction Management|Look up Transactions Request Builder - Extended|Request Builder produces the request payload for this action. Use this endpoint to search for transactions.|
    |Look up Transactions Response Parser - Extended|Parses the response from the search. Use this endpoint to search for transactions.|
    |Mastercom Extended - Case Filing Document Management|Look up Processed Documents by Case ID Request Builder - Extended|Request Builder for Retrieve processed documents associated with cases API. Use this endpoint to retrieve all documents from a case. The documents include any documents attached by any party.|
    |Look up Processed Documents by Case ID Response Parser - Extended|Parses response of the Retrieve processed documents associated with cases. Use this endpoint to retrieve all documents from a case. The documents include any documents attached by the sender, receiver, or both.|
    |Mastercom Extended - Document Management|Look up Processed Documents by Document Completed ID Request Builder - Extended|Request Builder for Retrieve processed documents API. Use this endpoint to retrieve processed documents.|
    |Look up Processed Documents by Document Completed ID Response Parser - Extended|Response Parser for Retrieve processed documents API endpoint. Use this endpoint to retrieve processed documents.|

    The following example illustrates the solution overview when it integrates with a Tokenization solution: ![Tokenization solution overview.](../image/spoke-mastercard-flow.jpg)

-   **Actions with non-sensitive information** - You can directly invoke these Mastercom/Mastercom Extended APIs from your ServiceNow instance.

<table id="table_cjl_k2k_zyb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="8">

Mastercom Chargeback Management

</td><td>

Acknowledge Chargebacks

</td><td>

Acknowledges a chargeback or second representment moves the claim from the Unworked queue to the Worked queue.

</td></tr><tr><td>

Create Chargeback

</td><td>

Creates chargebacks and second presentments with the option to upload supporting documents.

</td></tr><tr><td>

Load Data for Chargebacks

</td><td>

Obtains information about a potential first chargeback or second presentment before creating the chargeback.

</td></tr><tr><td>

Look up Chargeback Documents

</td><td>

Retrieves documents in the required format associated with the chargeback type.

</td></tr><tr><td>

Look up Chargeback Image Status

</td><td>

Retrieves documents with a status \(completed, pending, failed, unavailable, or document not applicable\) for chargebacks.

</td></tr><tr><td>

Look up Status of Chargebacks

</td><td>

Retrieves the status of documents for a specific list of claim IDs and chargeback IDs.

**Note:** Issuers and acquirers can send a maximum of 2,000 chargeback IDs in a single request.

</td></tr><tr><td>

Reverse Chargeback

</td><td>

Reverses an existing chargeback when the issuer or acquirer creates a chargeback in error.

</td></tr><tr><td>

Update Chargeback

</td><td>

Updates existing chargebacks with memos or documents.

</td></tr><tr><td rowspan="2">

Mastercom Claim Management

</td><td>

Create Claim

</td><td>

e this endpoint to create a claim, which is required before creating a retrieval request or a first chargeback.

</td></tr><tr><td>

Take Action on Existing Claim

</td><td>

e this endpoint to perform operations \(reopen or close\) on an existing claim.

</td></tr><tr><td rowspan="2">

Mastercom Fraud Management

</td><td>

Create Fraud

</td><td>

Creates a fraud item when the issuer determines that a transaction was fraudulent. **Note:** Mastercom enables issuers to create fraud items in the Fraud and Loss database. However, issuers must use the Fraud and Loss application to make further updates to fraud items.

</td></tr><tr><td>

Look up Fraud Related Information

</td><td>

e this endpoint to obtain fraud-related information associated with a claim before creating a fraud item for the claim.

</td></tr><tr><td>

Mastercom Queues Management

</td><td>

Look up Queue Names

</td><td>

Retrieves a list of queue names.

</td></tr></tbody>
</table><table id="table_qlx_mp3_l2c"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Mastercom Extended - Case Filing Document Management

</td><td>

Attach Document by Case ID - Extended

</td><td>

Use this endpoint to attach a new document to an existing case when the previous document failed to process. Document processing status can be retrieved from the GET /cases/documents/attributes endpoint.

</td></tr><tr><td>

Look up Statuses for Documents Associated with Cases - Extended

</td><td>

Use this endpoint to retrieve the processing status of documents associated with cases.

</td></tr><tr><td rowspan="4">

Mastercom Extended - Case Filing Management

</td><td>

Create Pre-Arbitration/Arbitration Case - Extended

</td><td>

Use this endpoint to create a pre-arbitration or arbitration case.

</td></tr><tr><td>

Look up Case Details by ID - Extended

</td><td>

Use this endpoint to retrieve details for an existing case, providing comprehensive information about the case.

</td></tr><tr><td>

Update Pre-Arbitration/Arbitration Case - Extended

</td><td>

Use this endpoint to update or respond to a pre-arbitration or arbitration case.

</td></tr><tr><td>

Update Pre-Compliance/Compliance Case - Extended

</td><td>

Use this endpoint to update or respond to a pre-compliance or compliance case.

</td></tr><tr><td>

Mastercom Extended - Chargeback Management

</td><td>

Create Chargeback Reversal - Extended

</td><td>

Use this endpoint to reverse existing chargebacks.

</td></tr><tr><td rowspan="2">

Mastercom Extended - Claim Management

</td><td>

Create Claim - Extended

</td><td>

Use this endpoint to create a new claim.

</td></tr><tr><td>

Create Pre-Compliance/Compliance Case - Extended

</td><td>

Use this endpoint to create a pre-compliance or compliance case.

</td></tr><tr><td>

Mastercom Extended - Dispute Management

</td><td>

Initiate a Dispute by Claim ID - Extended

</td><td>

Use this endpoint to initiate a dispute. At this time, only creating a chargeback is supported.

</td></tr><tr><td rowspan="3">

Mastercom Extended - Document Management

</td><td>

Attach Documents by Claim ID and Event ID - Extended

</td><td>

Use this endpoint to attach previously uploaded documents to existing dispute events.

</td></tr><tr><td>

Check Document Details - Extended

</td><td>

Use this endpoint to get the details of documentation attached to their events, including status.

</td></tr><tr><td>

Upload Documents - Extended

</td><td>

Use this endpoint to upload documents.

 To see details about file restrictions, refer to the Tutorials and Guides section of the Mastercom Extended API Specifications.

</td></tr><tr><td rowspan="3">

Mastercom Extended - Queue Management

</td><td>

Look up Claims in a Queue by ID Stream - Extended

</td><td>

Use this endpoint to retrieve a list of claims in a queue within a specified date range.

</td></tr><tr><td>

Look up Queue by ID - Extended

</td><td>

Use this endpoint to retrieve fields within a specific queue.

</td></tr><tr><td>

Look up Queues Stream - Extended

</td><td>

Use this endpoint to retrieve a list of queues and their fields.

</td></tr><tr><td rowspan="2">

Mastercom Extended - Report Definition Management

</td><td>

Look up Report Fields - Extended

</td><td>

Use this endpoint to retrieve fields within a specific report.

</td></tr><tr><td>

Look up Report Fields Stream - Extended

</td><td>

Use this endpoint to retrieve a list of reports and their fields.

</td></tr><tr><td rowspan="4">

Mastercom Extended - Report Management

</td><td>

Create a Report - Extended

</td><td>

Use this endpoint to request the creation of report. NOTE: The system requires at least 120 seconds to generate a report.

</td></tr><tr><td>

Look up Completed Report - Extended

</td><td>

Use this endpoint to retrieve a completed report.

</td></tr><tr><td>

Look up Report Status - Extended

</td><td>

Use this endpoint to retrieve the status of a specific report.

</td></tr><tr><td>

Look up Reports Stream - Extended

</td><td>

Use this endpoint to obtain a report status and reportCompletedId.

</td></tr><tr><td>

Mastercom Extended - Representment Management

</td><td>

Update Representment by Claim ID and Event ID - Extended

</td><td>

Use this endpoint to acknowledge a representment, which moves the claim to the Worked queue. Issuers may take further actions on acknowledged claims.

</td></tr></tbody>
</table>
## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Mastercard spoke](../task/set-up-mastercard-spoke.md#).

