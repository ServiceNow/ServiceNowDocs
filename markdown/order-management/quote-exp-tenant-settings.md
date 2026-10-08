---
title: ServiceNow Quote Experience tenant settings
description: Configure these tenant settings on the CPQ microservice instance to enable ServiceNow Quote Experience and its capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-exp-tenant-settings.html
release: brazil
topic_type: reference
last_updated: "2026-09-23"
reading_time_minutes: 1
breadcrumb: [Without guided setup, Set up CPQ, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# ServiceNow Quote Experience tenant settings

Configure these tenant settings on the CPQ microservice instance to enable ServiceNow Quote Experience and its capabilities.

## Required settings

Set all of the following settings to `true`, except **optionPaginationLimit**, which takes a numeric value:

-   All CPQ Transaction Manager standard settings
-   **Transaction.oneQuoting.enabled**
-   **allowDynamicFieldOptions**
-   **optionPaginationLimit** — set to a positive number. Otherwise, options do not appear in dynamic picklist fields.
-   **connections.auth.type.jwtOAuth**
-   **enableTheme**
-   **features.enableDynamicBom**

## Capability-specific settings

Activate the following settings only if you use the corresponding capability:

|Capability|Setting name|
|----------|------------|
|Sync Quote to Opportunity|**transaction.oneQuoting.opportunitySync.enabled**|
|Advanced Approvals|**transaction.oneQuoting.approvals.enabled**|
|PDF Document Generation|**transaction.oneQuoting.docGen.enabled**|
|Pricing|**transaction.oneQuoting.pricing.enabled**|
|Subscriptions|**transaction.oneQuoting.subscriptions.enabled**|
|Partner Management|**transaction.oneQuoting.partnerMgmt.enabled**|

