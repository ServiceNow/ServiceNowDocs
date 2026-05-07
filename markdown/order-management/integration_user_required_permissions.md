---
title: Required permissions for the integration user
description: The integration user, or refresh token user, must have the following permissions if it does not already have system administrator permissions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Required permissions for the integration user

The integration user, or refresh token user, must have the following permissions if it does not already have system administrator permissions.

The refresh token user \(or integration user\) is the user name that CPQ uses for API syncing of Configuration Line Data, Configuration Data, and to populate the caches of Product2, Pricebook, and Pricebook Entries in Salesforce. This sync occurs every 30 minutes for test and demo sites and every 15 minutes for production sites. Although using a system administrator as your refresh token user is the simplest and most common route to take when configuring CPQ, some CPQ customers prefer not to define their refresh token user with system administrator permissions \(usually because of a company-wide security policy\). The following list shows the necessary permissions for non-admin profiles to be set up as refresh token users when using CPQ with Salesforce CPQ:

-   The user must be API enabled
-   The LGKConfigurationLineItemc and LGK ConfigurationFieldDatac objects must have Create access
-   The user must have permission to read all fields and objects that are referenced in the SOQL queries of Salesforce external connections
-   The objects Product2, Pricebook2, and PricebookEntry must have Read/View access, including access to the following fields:

    Product2:

    -   Name
    -   Id
    -   ProductCode
    -   Description
    -   IsActive
    -   Family
    -   ExternalId
    -   SBQQ\_ExternallyConfigurable\_c
    -   QuantityUnitOfMeasure
    -   StockkeepingUnit
    Pricebook2:

    -   Id
    -   Name
    -   Description
    -   IsActive
    -   IsStandard
    -   CreatedDate
    -   LastModifiedDate
    PricebookEntry:

    -   Id
    -   Pricebook2Id
    -   Product2Id
    -   UnitPrice
    -   IsActive
    -   UseStandardPrice
    -   ProductCode
    -   CreatedDate
    -   LastModifiedDate
    -   CurrencyIsoCode \(if using multicurrency\)
    -   ProductSellingModelId

