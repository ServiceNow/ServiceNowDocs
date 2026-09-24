---
title: Billing account tables and plugins
description: Lists the tables that the Billing Account Core application adds or reuses, and the applications required to enable billing accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/billing-account-tables-and-plugins.html
release: brazil
topic_type: reference
last_updated: "2026-09-11"
reading_time_minutes: 1
breadcrumb: [Configuring billing accounts, Billing accounts, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Billing account tables and plugins

Lists the tables that the Billing Account Core application adds or reuses, and the applications required to enable billing accounts.

## Tables

|Table|Table name|Added or reused|Dependency|
|-----|----------|---------------|----------|
|Billing Account|`sn_billing_account_billing_account`|Added|Billing Account Core|
|Billing Account Address|`sn_billing_account_address`|Added|Billing Account Core \(the Address Type field requires the CSM plugin\)|
|Billing Account Payment Profile|`sn_billing_account_payment_profile`|Added|Billing Account Core|
|Billing Account Related Party|`sn_billing_account_related_party`|Added|Requires the CSM plugin|
|Schedule|`cmn_schedule`|Reused|Platform|
|Schedule Entry|`cmn_schedule_span`|Reused|Platform|
|Location|`cmn_location`|Reused|Platform|

## Applications

|Application|ID|Purpose|
|-----------|---|-------|
|Billing Account Core|`sn_billing_account`|Adds the billing account data model. Required.|
|Customer Service Management|`com.sn_customerservice`, `com.snc.cs_base`|Enables the CSM dependent capabilities: the account, contact, and consumer relationships, related parties, and the Address Type field.|

## Activation

The payment profile and billing schedule fields appear on the existing billing account tables, so no net-new plugin is required. Ensure that Billing Account Core is up to date. The billing schedule is built on the platform Schedule data model.

**Related topics**  


[billing-account-data-model]

[Billing accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configuring-billing-accounts.md)

[Roles installed with billing accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/roles-installed-with-billing-accounts.md)

