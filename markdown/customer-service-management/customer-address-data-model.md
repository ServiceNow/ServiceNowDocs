---
title: Customer address data model
description: Reference how customer entities associate with location records through address type. One location can be reused across customer entities and account hierarchies for billing, shipping, mailing, and service purposes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-address-data-model.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Customer Data Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Customer address data model

Reference how customer entities associate with location records through address type. One location can be reused across customer entities and account hierarchies for billing, shipping, mailing, and service purposes.

## Overview of customer address data model

The customer address data model captures the structures used to associate customer entities \(account, contact, consumer, consumer profile\) with physical locations. The model is built on three principles:

-   Define and manage addresses as location records: Every physical address is a Location \[cmn\_location\] record.
-   Define the type of address based on its purpose: The same location can play different roles through address type, such as billing, shipping, or mailing. The Address Type is a property of the association, not of the Location.
-   Reuse addresses across an account hierarchy, or across hierarchies: When multiple customer entities share a location, they reference the same location record.

## Account address data model diagram

\[Omitted image "refarch-customer-address-data-model.png"\] Alt text: Customer Address data model showing how Account, Contact, Consumer, and Consumer Profile associate with Location through Address Type, with many-to-many association tables for Account and Consumer Profile.

In the account address data model diagram, account and consumer profile associate with location through many-to-many association tables \(account addresses, consumer profile addresses\), classified by Address Type. Contact and consumer reference location directly. Account has a one-to-many relationship to contact, and consumer to consumer profile.

## Tables in the Customer Address data model

This model introduces the association tables that connect customer entities to locations. The Location record and the customer entities themselves are defined in the customer data model.

|Label|Table name|Description|
|-----|----------|-----------|
|Address Type| |Classification of a customer-to-location association, such as Billing, Shipping, or Mailing. Configurable per implementation.|
|Account Addresses| |Many-to-many link from `customer_account` to `cmn_location`, classified by Address Type. One Account can have multiple addresses, and one Location can serve multiple Accounts.|
|Consumer Profile Addresses| |Many-to-many link from `sn_csm_consumer_profile` to `cmn_location`, classified by Address Type. Enables per-profile address management.|

**Related topics**  


[Enhanced address data model for accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-enable-enhanced-address-data-model.md)

[Reusing addresses between multiple accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/reuse-account-addresses.md)

[Address sharing through account hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/address-sharing-account-hierarchy.md)

