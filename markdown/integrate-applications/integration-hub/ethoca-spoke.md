---
title: Ethoca spoke
description: Integrate ServiceNow instance with your Ethoca account to manage card dispute resolution and prevent fraud. By using this spoke, you can access detailed merchant information and subscription control, view digital receipts, and manage their disputes.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Ethoca spoke

Integrate ServiceNow instance with your Ethoca account to manage card dispute resolution and prevent fraud. By using this spoke, you can access detailed merchant information and subscription control, view digital receipts, and manage their disputes.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Ethoca spoke v3.0.0 is the latest version.

## Supported versions

This spoke was built for Consumer Clarity and Issuer Alerts Management.

## Key features

-   Streamlines dispute resolution processes
-   Facilitates collaboration between issuers and participating merchants through Ethoca Alerts during the dispute lifecycle
-   Resolves cases at the pre-dispute stage, benefiting both issuers and cardholders
-   Reduces the occurrence of disputes and chargebacks

## Spoke requirements

-   Integration Hub subscription
-   Ethoca configuration details such as, certificate, key alias, consumer key, and keystore password

## Spoke dependencies

Ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** If used outside the spoke implementation, some of these plugins are licensable features and need appropriate licenses.

## Spoke actions

The Ethoca spoke provides actions to obtain enriched merchant and transaction information. Available actions include:

<table id="table_byz_hkc_wyb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Consumer Clarity

</td><td>

Look up Consumer Clarity

</td><td>

Enables cardholders to view their credit card transactions with clear merchant information and transaction details.

</td></tr><tr><td rowspan="4">

Issuer Alerts Management

</td><td>

Create Transaction Alert

</td><td>

Submits a batch of transactions \(confirmed fraud or customer disputes\) to Ethoca. These transactions are processed and delivered to merchants as alerts.

</td></tr><tr><td>

Look up Transaction Alert Status by Batch

</td><td>

Returns the processing status of previously submitted transaction requests.

</td></tr><tr><td>

Look up Alert Status

</td><td>

Provides the status of the alert delivered to the merchant.

</td></tr><tr><td>

Look up Alert Outcome by Batch Stream

</td><td>

Retrieves a list of alerts and their outcomes based on the Batch ID provided by the Submit Batch endpoint or Ethoca Notification Callback. Results are paginated with up to 50 alerts per request and a maximum of 1000 alerts per batch.**Note:** To enable the Look up Alert Outcome by Batch Stream action, install the ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\) plugin.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Ethoca spoke](../task/set-up-ethoca-spoke.md#)

