---
title: Billing account data model
description: The billing account data model extends the Customer Data Foundation with a financial layer that captures how customers are billed and how they pay: billing accounts, their addresses, payment profiles, billing schedules, and related parties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/billing-account-data-model.html
release: brazil
topic_type: reference
last_updated: "2026-09-11"
reading_time_minutes: 2
breadcrumb: [Customer Data Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Billing account data model

The billing account data model extends the Customer Data Foundation with a financial layer that captures how customers are billed and how they pay: billing accounts, their addresses, payment profiles, billing schedules, and related parties.

## Billing account overview

A billing account is a centralized record that manages payment and invoicing for services, separate from the customer account that represents the organizational relationship. The billing account data model adds this financial layer to the Customer Data Foundation. It supports both B2B and B2C scenarios and captures payment ownership across self-paying, parent-funded, and designated-payer account structures.

## Entities and tables

|Entity|Table|Dependency|
|------|-----|----------|
|Billing Account|sn\_billing\_account\_billing\_account|Billing Account Core|
|Billing Account Address|sn\_billing\_account\_address|Billing Account Core \(the Address Type field requires the CSM plugin\)|
|Billing Account Payment Profile|sn\_billing\_account\_payment\_profile|Billing Account Core|
|Billing Account Related Party|sn\_billing\_account\_related\_party|Requires the CSM plugin|
|Schedule|cmn\_schedule|Platform \(reused\)|
|Schedule Entry|cmn\_schedule\_span|Platform \(reused\)|
|Location|cmn\_location|Platform|
|Account, Contact, Consumer| |Requires the CSM plugin|

## Relationships

-   A billing account references the customer it bills: an account, a contact, or a consumer. These relationships require the CSM plugin.
-   Billing accounts form a parent-child hierarchy, so that charges from sub-accounts can roll up to a parent for consolidated billing.
-   A billing account has one or more addresses, each pointing to a location. One address can be the primary address.
-   A billing account has one or more payment profiles that define the payment method and terms.
-   A billing account links to a platform schedule through its Billing Schedule field, and each schedule has one or more schedule entries. The schedule is scoped to billing accounts when its Type is Billing Account.
-   Related parties grant additional users access to a billing account through the responsibility framework and require the CSM plugin. A related party is either authorized, with read access through a responsibility, or listed, which tracks the party without granting access.

**Related topics**  


[Customer Data Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/customer-data-foundation.md)

[Billing accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configuring-billing-accounts.md)

[Billing Account form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/billing-account-form.md)

[Granular roles and entities for responsibility framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/granular-roles-and-supported-entities-CAM.md)

[Data management for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-data-management.md)

