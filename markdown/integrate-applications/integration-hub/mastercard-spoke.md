---
title: Mastercard spoke
description: Integrate ServiceNow instance with your Mastercard account to enable access to Mastercard's API suite, Mastercom, for card dispute resolution. This integration enables you to perform tasks such as searching transactions, creating claims, and processing chargebacks.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Mastercard spoke

Integrate ServiceNow instance with your Mastercard account to enable access to Mastercard's API suite, Mastercom, for card dispute resolution. This integration enables you to perform tasks such as searching transactions, creating claims, and processing chargebacks.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Subscription information

This spoke requires a subscription. Contact your ServiceNow account manager or sales representative for subscription details. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf)

## Spoke version

Mastercard spoke v2.0.1 is the latest version.

## Supported version

This spoke was built for Mastercom v6.

## Key features

Mastercard spoke enables a flow designer to build workflows using actions that invoke Mastercom. This includes the ability to:

-   Search transactions
-   Create claims and chargebacks
-   Collaborate with merchants to prevent chargebacks
-   Monitor disputes throughout the dispute lifecycle
-   Expedite the end-to-end dispute management process

## Spoke requirements

Mastercard configuration details such as, certificate, key alias, consumer key, and keystore password.

## Spoke dependencies

Ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Mastercard spoke provides actions to simplify card dispute resolution. Available actions include:

-   **Actions with sensitive information** - These actions contain sensitive information in the request and response body. When using Mastercom APIs, it is recommended to use a Tokenization solution. This involves using a request builder to securely create requests and a response parser to handle encrypted API responses.

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

    The following example illustrates the solution overview when it integrates with a Tokenization solution: ![Tokenization solution overview.](../image/spoke-mastercard-flow.jpg)

-   **Actions with non-sensitive information** - You can directly invoke these Mastercom APIs from your ServiceNow instance.

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

</td></tr></tbody>
</table>
## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Mastercard spoke](../task/set-up-mastercard-spoke.md#)

