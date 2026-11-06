---
title: ServiceNow Quote Experience tenant settings
description: Configure these tenant settings on the ServiceNow CPQ microservice instance to enable ServiceNow Quote Experience and its capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/quote-exp-tenant-settings.html
release: australia
topic_type: reference
last_updated: "2026-09-23"
reading_time_minutes: 1
breadcrumb: [Without guided setup, Setting up ServiceNow CPQ, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# ServiceNow Quote Experience tenant settings

Configure these tenant settings on the ServiceNow CPQ microservice instance to enable ServiceNow Quote Experience and its capabilities.

## Required settings

Set all of the following settings to `true`, except where noted:

-   All ServiceNow CPQ Transaction Manager standard settings
-   **Transaction.oneQuoting.enabled**
-   **allowDynamicFieldOptions**
-   **optionPaginationLimit** - set to a positive number. This setting takes a numeric value. Otherwise, options do not appear in dynamic picklist fields.
-   **connections.auth.type.jwtOAuth**
-   **enableTheme**
-   **features.enableDynamicBom**
-   **transaction.oneQuoting.dataSyncToSNQuote.enabled**
-   **transaction.oneQuoting.dataSyncToSNQuote.api.version** - set to `v2`. This setting takes a text value.

## Capability-specific settings

Activate the following settings only if you use the corresponding capability:

<table id="table-capability-settings"><thead><tr><th>

Capability

</th><th>

Setting name

</th></tr></thead><tbody><tr><td>

Sync Quote to Opportunity

</td><td>

**transaction.oneQuoting.opportunitySync.enabled**

</td></tr><tr><td>

Advanced Approvals

</td><td>

**transaction.oneQuoting.approvals.enabled**

</td></tr><tr><td>

PDF Document Generation

</td><td>

**transaction.oneQuoting.docGen.enabled**

</td></tr><tr><td>

Pricing

</td><td>

**transaction.oneQuoting.pricing.enabled** set to `true`

 **transaction.oneQuoting.pricing.integration.type** set to `productized`

</td></tr><tr><td>

Subscriptions

</td><td>

**transaction.oneQuoting.subscriptions.enabled**

</td></tr><tr><td>

Partner Management

</td><td>

**transaction.oneQuoting.partnerMgmt.enabled**

</td></tr><tr><td>

Order Management

</td><td>

**transaction.oneQuoting.orders.enabled**

</td></tr></tbody>
</table>