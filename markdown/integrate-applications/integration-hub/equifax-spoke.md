---
title: Equifax Spoke
description: Integrate the ServiceNow instance with the Equifax spoke to access important information about the credit history for a customer, fraud alerts, digital identity verification, transaction screening, and other relevant data.Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Equifax Spoke

Integrate the ServiceNow instance with the Equifax spoke to access important information about the credit history for a customer, fraud alerts, digital identity verification, transaction screening, and other relevant data.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

Equifax spoke v1.0.0 supports Equifax OneView - 1.0.2212 \(Consumer API\).

## Key features

Equifax spoke enables a flow designer to do the following tasks:

-   Access customer information, such as the credit history for a customer, the credit score for a customer, and fraud alerts.
-   Evaluate a customer's creditworthiness to make lending decisions faster.
-   Verify customer identities to ensure that you have accurate information.

## Spoke actions

The Equifax spoke provides actions \(under the Equifax Credit Report category\) to automate tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Equifax Credit Report|Look up One View Credit Report|Provides the JSON response that gives the credit history of the customer.|
|Look up One View Credit Report by Request ID|Provides the PDF report of the credit history for the customer.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Equifax spoke](../task/set-up-equifax-spoke.md#).

