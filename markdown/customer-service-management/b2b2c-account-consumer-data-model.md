---
title: B2B2C - Account consumer data model
description: Reference the account consumer linkage entity that joins an account to a consumer in business-to-business-to-consumer \(B2B2C\) scenarios. An enterprise customer is responsible for individual consumers who use the products or services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/b2b2c-account-consumer-data-model.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Customer Data Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# B2B2C - Account consumer data model

Reference the account consumer linkage entity that joins an account to a consumer in business-to-business-to-consumer \(B2B2C\) scenarios. An enterprise customer is responsible for individual consumers who use the products or services.

## Overview of B2B2C data model

The B2B2C account consumer model is common across insurance, healthcare, telecommunications, and financial services. The model adds one new entity, account consumer, which links an account to a consumer with metadata about the relationship. The linkage forms a chain from account to account consumer to consumer, and then to the consumer user and the platform user.

## B2B2C - Account consumer data model diagram

\[Omitted image "refarch-b2b2c-account-consmer-data-model.png"\] Alt text: B2B2C entity mapping showing Account to Account Consumer to Consumer to Consumer User to User. Reference and transaction data apply as described in the customer data model.

In the B2B2C account consumer data model diagram, account consumer links an account to a consumer, forming the chain account, account consumer, consumer, consumer user, and user. The account is the enterprise customer, and the consumer is the individual customer. Reference data and transaction data apply as described in the customer data model.

## Tables in the B2B2C Account Consumer data model

|Label|Table name|Description|
|-----|----------|-----------|
|Account| | |
|Account Consumer| |B2B2C linkage entity. Links an Account to a Consumer with metadata about responsibility scope, effective dates, and relationship category. A Consumer can be linked to multiple Accounts, and an Account can be linked to many Consumers.|
|Consumer|csm\_consumer| |
|Consumer User \(linked\)|sys\_user| |
|User| | |

**Note:** B2B2C model does not redefine customer entities. It reuses the account entity from the [B2B - Account data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/b2b-account-data-model.md) and the consumer entity from the [B2C - Customer and household data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/b2c-customer-and-household-data-model.md). It also reuses the framework components from [Customer relationships and access management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/customer-relationships-and-access-management.md).The only entity it adds is Account Consumer.

## How data applies in B2B2C

The account consumer linkage allows reference and transaction data to apply at the account level, the consumer level, or both.

|Data category|Where it applies in BB2B2C|
|-------------|--------------------------|
|Sold products|Typically on the account \(the enterprise holds the product record\); can also be on the consumer for consumer-specific products such as a policy in the consumer's name.|
|Install base items|On the consumer for the consumer's own equipment \(a home medical device\); on the account for enterprise-issued equipment.|
|Contracts|Account-level contracts that cover linked consumers; consumer-specific contracts for individual arrangements.|
|Entitlements|Typically derived from the account contract and applied to the consumer through the linkage.|
|Locations|Account addresses \(billing, mailing to the enterprise\); consumer or profile addresses \(service delivery, primary residence, insured property\).|
|Case|Opened at the consumer level with visibility to the account, or at the account level with reference to a specific consumer.|
|Work orders|Dispatched to the consumer's service address but authorized through the account's contract and entitlement.|

**Related topics**  


[Configure customer data models for B2B2C](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-customer-data-model-b2b2c.md)

[Using customer data models for B2B2C](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/using-b2b2c.md)

