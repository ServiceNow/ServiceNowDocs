---
title: Verifi Spoke
description: Integrate your ServiceNow instance with the Verifi Spoke to streamline the card dispute resolution process by using the Verifi APIs. This integration facilitates early connections between issuers and merchants in the dispute lifecycle, which simplifies conflict resolutions at the pre-dispute stage and minimizes chargebacks.Also reuse this short description in the release notes.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Verifi Spoke

Integrate your ServiceNow instance with the Verifi Spoke to streamline the card dispute resolution process by using the Verifi APIs. This integration facilitates early connections between issuers and merchants in the dispute lifecycle, which simplifies conflict resolutions at the pre-dispute stage and minimizes chargebacks.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Subscription information

This spoke requires a subscription. Contact your ServiceNow account manager or sales representative for subscription details. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf)

## Spoke version

Verifi Spoke v1.0 is the latest version.

## Supported versions

This spoke was built for Verifi API version 4.0 but may be compatible with later versions.

## Key features

Verifi Spoke enables a flow designer to build workflows by using actions that invoke Verifi APIs. This integration enables you to do the following tasks:

-   Address disputes with merchants to prevent escalation, which saves time and resources for both issuers and cardholders.
-   Create, manage, and close dispute cases by using API actions to ensure smoother operations and enhanced collaboration among stakeholders.
-   Resolve disputes early with direct merchant involvement to minimize chargebacks.
-   Leverage streamlined processes and pre-dispute resolutions to reduce the effort required in managing disputes.
-   Improve cooperation and communication between cardholders, issuers, and merchants.

## Spoke requirements

Set up the JSON Web Token \(JWT\) Key with a shared key \(HMAC\) and connect a JWT provider to the signing configuration by using a JWT key reference.

## Spoke dependencies

Ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Verifi Spoke provides actions to resolve cardholder disputes efficiently.

The actions with sensitive information contain sensitive information in the request and response body. One action involves a request builder to securely create requests and a response parser to handle encrypted API responses. The following table lists the actions that have sensitive information.

|Category|Action|Description|
|--------|------|-----------|
|Verifi Case Management|Create Case Request Builder|Use the Request Builder and response parser of the Verifi Create Case API to create a case that represents the cardholder's dispute and submit it for merchant communication.|
|Create Case Response Parser|
|Look up Case Request Builder|Use the Request Builder and response parser of the Look up Case API to retrieve the case details from Verifi API.|
|Look up Case Response Parser|
|Look up Multiple Cases Request Builder|Use the Request Builder and response parser of the Look up Multiple Cases API to retrieve multiple case details from the Verifi API. The issuer can identify multiple case IDs in a single retrieve attempt.|
|Look up Multiple Cases Response Parser|
|CDRN Eligibility Request Builder|Submit a real-time check for merchant eligibility on a case using the CDRN case inquiry-only call, which is facilitated by the request builder and response parser of the Verifi eligibility API.|
|CDRN Eligibility Response Parser|
|Update Case Request Builder|Use the request builder and response parser of the Verifi patch API to update the case status to either CLOSED or REVOKED. This functionality enables issuers to efficiently manage case outcomes.|
|Update Case Response Parser|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Verifi Spoke](../task/set-up-verifi-spoke.md#)

