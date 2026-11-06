---
title: ServiceNow Quote Experience runtime API calls
description: Reference for the runtime APIs used in the ServiceNow Quote Experience, including their purposes, responses, and a OpenAPI Specification for testing in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/quote-tm-runtime-api-calls.html
release: australia
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [ServiceNow Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# ServiceNow Quote Experience runtime API calls

Reference for the runtime APIs used in the ServiceNow Quote Experience, including their purposes, responses, and a OpenAPI Specification for testing in ServiceNow CPQ.

## API overview

ServiceNow CPQ APIs are divided into two categories: runtime APIs and admin APIs. Runtime APIs are the same APIs used in the runtime quote experience. The following table lists the runtime APIs for ServiceNow Quote Experience.

|API action|Purpose|Response|
|----------|-------|--------|
|Initialize a session|Initializes a session to establish a context for executing transaction events, managing state, and processing subsequent API calls. Can initialize for an existing transaction. If no transaction is specified, a new transaction is created.|Returns a session ID, a transaction ID, and transaction information.|
|Delete a session|Deletes a session to securely end user activity, clear session-specific data, and free up system resources.|Session is deleted. No information is returned.|
|Create a transaction|Creates a transaction, providing the object to manage the transaction lifecycle, configure and add products, and determine pricing.|Returns a transaction ID and transaction information.|
|Run events on a transaction|Triggers a specified system or custom event on a transaction to execute predefined logic or workflows, such as editing field values, initiating approvals, versioning transactions, and validating configurations.|Varies by event.|
|Add products to a transaction \(upsert\)|Adds one or more products to a transaction, enabling dynamic configuration and pricing updates based on the product's attributes.|Returns updated transaction data with the additional products.|
|Get a list of transactions|Retrieves a list of transactions, enabling users to view, manage, or take action on existing transactions.|A list of transactions with transaction IDs and metadata.|
|Get details of a transaction|Retrieves the header information of a transaction, including stage, account, and summary-level data.|All header field data for the transaction.|
|Get a transaction's lines|Retrieves the line item details for a transaction, including product data, quantities, pricing, and custom attributes for each line.|All line-level field data for the transaction.|

**Note:** Event APIs are authorized via session cookie only. Avoid building a scenario in which the user initiates an event that also fires an event API on the same transaction — such an implementation can result in unpredictable behavior.

## Additional APIs

For details about the API that retrieves metrics for transactions, see [Quote Experience metrics API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/quote-tm-metrics-api.md).

## OpenAPI Specification

The following OpenAPI specification describes all available REST endpoints, request payloads, response formats, parameters, and data models for the ServiceNow Quote Experience runtime APIs. For more information, see [KB3229681](https://support.servicenow.com/kb?sys_kb_id=ac68a3a947901b582c31b98a436d435a&id=kb_article_view).

