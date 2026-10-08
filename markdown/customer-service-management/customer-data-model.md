---
title: Customer data model
description: Reference the tables, entity relationships, and platform extensions behind Customer Data Foundation. This is the table-level view of the customer models, grouped into sub-models that each carry their own diagram and table reference.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-data-model.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Customer Data Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Customer data model

Reference the tables, entity relationships, and platform extensions behind Customer Data Foundation. This is the table-level view of the customer models, grouped into sub-models that each carry their own diagram and table reference.

## Overview of customer data model

The customer data model is the table-level reference for Customer Data Foundation. It identifies the tables that store customer records, the platform tables those records extend, and the relationships that connect customer organizations to the individual people associated with them. The model is grouped into sub-models, each with its own diagram, dependencies, and table reference. Explore each sub-model explained in this topic for its entities and tables.

## Dependencies

The customer data model depends on the following platform components and applications:

|Component|Dependency identifier|
|---------|---------------------|
|ServiceNow AI Platform|Provides `sys_user`, `core_company`, `cmn_location`, `task`|
|Customer Service Management \(CSM\)|com.sn\_customerservice|
|Expanded model and asset classes|com.sn\_ent \(verify\)|
|Install Base|com.snc.install\_base \(verify\)|

## Simplified customer data model

\[Omitted image "refarch-customer-data-model.png"\] Alt text: Simplified customer data model showing the B2B branch \(Account, Partner Account to Contact, Partner Contact\) and the B2C branch \(Household to Household Member; Consumer\)

The diagram shows the customer data model at the entity level, in two rows. The top row holds the customer organization entities, and the bottom row holds the people who belong to them. The B2B branch connects accounts and partner accounts to their contacts and partner contacts. The B2C branch connects households to household members, alongside consumers.

## Shared reference data

The customer models don't define reference data. They consume reference data defined elsewhere in the platform. Both B2B and B2C entities associate with the same shared reference data.

|Reference data|Examples|Where they are defined|
|--------------|--------|----------------------|
|Sold products|Deposit accounts, medical devices, SaaS subscriptions, policies, cloud service instances|Install base and product model|
|Install base items|MRI machines, X-ray machines, permits, deployed cloud instances, home equipment|Install base|
|Contracts|Support contracts, service plans, entitled channels, support hours|Platform contracts|
|Entitlements|SLAs, response commitments, escalation paths, tiered support|CSM entitlements|
|Locations|Billing, shipping, mailing, service, and primary addresses|Platform locations, and customer address data model|

## Shared transaction data

B2B and B2C interactions use the same task-derived tables. The customer side of each record references either an account and contact \(B2B\) or a consumer and household \(B2C\).

|Transaction data|Examples|
|----------------|--------|
|Case|Block a debit card, equipment not working, billing question, and claim submission|
|Case tasks|Fee review, approval, escalation, and identity verification|
|Interaction|Chat, phone, and messaging interactions from a customer|
|Work orders|Set up broadband, quarterly maintenance, on-site installation, and in-home service|

## Platform and CSM tables used in the customer data model

This table defines the platform and shared CSM tables. Each sub-model topic lists only the tables it introduces.

|Table|Description|Application|
|-----|-----------|-----------|
|sys\_user|Platform user record. Contact, Consumer, and other person entities extend this table.|AI Platform|
|core\_company|Platform company record. Account and Household extend this table.|AI Platform|
|cmn\_location|Platform location record. Customer addresses reference this table.|AI Platform|
|task|Platform task record. Cases, Case Tasks, and Work Orders extend this table.|AI Platform|
|customer\_account|B2B organization. Both Account and Partner Account use this table, distinguished by the Account type field. Extends `core_company`.|CSM|
|customer\_contact|Individual at a B2B account. Both Contact and Partner Contact use this table. Extends `sys_user`.|CSM|
|csm\_consumer|Individual B2C customer. Both Consumer and Household Member use this table. Extends `sys_user`.|CSM|
|csm\_household|B2C customers grouped under a shared address. Extends `core_company`.|CSM|
|sn\_csm\_consumer\_profile|A distinct context under a single consumer.|CSM|

**Related topics**  


[Data management for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-data-management.md)

[Service Model Foundation overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-industry-data-model.md)

[Configure customer data models for B2B2C](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-customer-data-model-b2b2c.md)

