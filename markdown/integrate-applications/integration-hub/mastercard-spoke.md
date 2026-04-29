---
title: Mastercard Spoke
description: Integrate your ServiceNow instance with Mastercard’s Mastercom API Suite and Mastercom Extended APIs to manage the full card dispute lifecycle. Handle tasks such as searching transactions, creating claims, and processing chargebacks, pre-arbitration, and arbitration case filings efficiently.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Mastercard Spoke

Integrate your ServiceNow instance with Mastercard’s Mastercom API Suite and Mastercom Extended APIs to manage the full card dispute lifecycle. Handle tasks such as searching transactions, creating claims, and processing chargebacks, pre-arbitration, and arbitration case filings efficiently.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Mastercard Spoke v3.0.1 is the latest version.

## Supported version

This spoke was built for Mastercom v6.

## Key features

Mastercard Spoke enables a flow designer to build workflows using actions that invoke Mastercom. This includes the ability to:

-   Search transactions
-   Create claims and initiate chargebacks
-   Manage seamless filing of pre-arbitration and arbitration cases
-   Collaborate with merchants to prevent chargebacks
-   Monitor disputes throughout the dispute lifecycle
-   Expedite the end-to-end dispute management process

## Spoke requirements

-   Integration Hub subscription
-   Mastercard configuration details such as, certificate, key alias, consumer key, and keystore password

## Spoke dependencies

Ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Mastercard Spoke provides actions to simplify card dispute resolution. Available actions include:

-   **Actions with sensitive information** - These actions contain sensitive information in the request and response body. When using Mastercom APIs, it is recommended to use a Tokenization solution. This involves using a request builder to securely create requests and a response parser to handle encrypted API responses.

    |Category|Action|Description|
    |--------|------|-----------|
    |Mastercom Chargeback Management|Look up Chargeback Documents Request Builder|Retrieves and parses chargeback-related documents in the required format.|
    |Look up Chargeback Documents Response Parser|
    |Mastercom Case Filing Management|Create Case Request Builder|Allows issuers or acquirers to file a pre-arbitration, arbitration, pre-compliance, or compliance case and optionally upload documents. They can also use the endpoint to create an Expedited Billing Dispute Form \(EBDF\) and attach it to the claim.|
    |Create Case Response Parser|
    |Look up Case Documents Request Builder|Retrieves and parses documents associated with a case in the preferred format.|
    |Look up Case Documents Response Parser|
    |Transactions|Look up Authorization Details of Transaction Request Builder|Retrieves and parses authorization details for the original transaction involved in the claim.|
    |Look up Authorization Details of Transaction Response Parser|
    |Look up clearing Details of Transaction Request Builder|Retrieves and parses clearing details for the original transaction involved in the claim.|
    |Look up Clearing Details of Transaction Response Parser|
    |Look up Transactions Request Builder|Searches for and parses information about an original transaction to support claim-related actions.|
    |Look up Transactions Response Parser|
    |Claims|Look up Claims in a Queue Request Builder|Retrieves and parses a list of claims in the queue within the specified date range.|
    |Look up Claims in a Queue Response Parser|
    |Look up Claim Details by Claim ID Request Builder|Retrieves and parses detailed information about a specific claim and its associated cases.|
    |Look up Claim Details by Claim ID Response Parser|

    The following example illustrates the solution overview when it integrates with a Tokenization solution: ![Tokenization solution overview.](../image/spoke-mastercard-flow.jpg)

-   **Actions with non-sensitive information** - You can directly invoke these Mastercom APIs from your ServiceNow instance.

<table id="table_cjl_k2k_zyb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Mastercom Case Filing Management

</td><td>

Look up Cases Status

</td><td>

Allows issuers and acquirers search for the status of documents for a specific list of cases.

</td></tr><tr><td>

Take Action on Case

</td><td>

Allows issuers or acquirers take action on a case filing, such as accept, reject, rebut, escalate, or withdraw, with or without attaching documents.

</td></tr><tr><td>

Look up List of Claims

</td><td>

Allows issuers or acquirers retrieve a list of claims associated with the existing cases.

</td></tr><tr><td rowspan="8">

Mastercom Chargeback Management

</td><td>

Acknowledge Chargebacks

</td><td>

Moves a chargeback or second representment from the Unworked queue to the Worked queue.

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

Issuers use this endpoint to create a claim, which is required before creating a retrieval request or a first chargeback.

</td></tr><tr><td>

Take Action on Existing Claim

</td><td>

Issuers use this endpoint to perform operations \(reopen or close\) on an existing claim.

</td></tr><tr><td rowspan="2">

Mastercom Fraud Management

</td><td>

Create Fraud

</td><td>

Creates a fraud item when the issuer determines that a transaction was fraudulent. **Note:** Mastercom enables issuers to create fraud items in the Fraud and Loss database. However, issuers must use the Fraud and Loss application to make further updates to fraud items.

</td></tr><tr><td>

Look up Fraud Related Information

</td><td>

Issuers use this endpoint to obtain fraud-related information associated with a claim before creating a fraud item for the claim.

</td></tr><tr><td>

Mastercom Queues Management

</td><td>

Look up Queue Names

</td><td>

Retrieves a list of queue names.

</td></tr><tr><td>

Health Check

</td><td>

Look up API Suite Health

</td><td>

Retrieves the status of the Mastercom API suite.

</td></tr></tbody>
</table>
## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Mastercard spoke](../task/set-up-mastercard-spoke.md#)

