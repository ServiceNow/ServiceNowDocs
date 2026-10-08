---
title: B2C - Customer and household data model
description: Reference the tables and relationships that store business-to-consumer \(B2C\) consumers, consumer profiles, households, household members, and the relationships that connect them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/b2c-customer-and-household-data-model.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Customer Data Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# B2C - Customer and household data model

Reference the tables and relationships that store business-to-consumer \(B2C\) consumers, consumer profiles, households, household members, and the relationships that connect them.

## Overview of B2C data model

The B2C consumer and household data model captures the structures used when the customer is an individual or a household.

Consumer is the core person entity. Consumer Profile lets a single consumer maintain multiple contexts, and household groups consumers who share an address or service arrangement. A family of relationship entities, such as consumer relationships, household member relationships, consumer team members, and household team members supports multi-party patterns across consumers and households.

The model supports scenarios such as a bank serving account holders, a healthcare provider serving patients, a telecommunications carrier serving residential subscribers, and a utility serving households.

## B2C - Consumer and household data model diagram

\[Omitted image "refarch-b2c-consumer-household-data-model.png"\] Alt text: B2C data model showing Consumer, Consumer Profile, Household, Household Member, and the relationship and team entities that govern multi-party access.

In the B2C consumer and household data model diagram, consumer and household are the core entities. Consumer profile, consumer profile location, household member, and the relationship and team entities govern multi-party access. Consumer can be extended for patients, constituents, and similar roles. Each entity refers to shared reference data and transaction data.

## Tables in the B2C Consumer and Household data model

|Label|Table name|Description|
|-----|----------|-----------|
|Consumer|csm\_consumer|Individual B2C customer. Extends `sys_user`. Can be extended for patients, constituents, and similar roles.|
|Consumer User \(linked\)|sys\_user|Platform user account associated with a consumer for login and self-service access.|
|Consumer Profile| |A distinct context \(role, relationship, or product line\) under a single consumer. A consumer can have multiple profiles.|
|Consumer Profile Location| |Many-to-many link from Consumer Profile to Location, classified by Address Type.|
|Consumer Relationship| |Bi-directional link between two consumers. Types include Authorized Representative, Attorney, Guarantor, Power of Attorney, Beneficiary.|
|Consumer Team Member|sn\_customer\_rel\_consumer\_to\_user|Internal employee assigned to a consumer in a named role, such as relationship manager, care coordinator, or financial planner.|
|Household|csm\_household|B2C customers grouped under a shared address or service arrangement. Extends `core_company`.|
|Household Member|csm\_consumer|Individual member of a household. Uses the same table as Consumer.|
|Household Member Relationship| |Relationship between two members of the same household. Types include Parent, Spouse, Child, Dependent, Guardian.|
|Household Team Member| |Internal employee assigned to a household in a named role.|

**Related topics**  


[Configure consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-csm-consumers.md)

[Configuring households](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-households.md)

[Creating multiple consumer profiles for a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/consumer-profiles-configuration.md)

[Configuring a Unified User](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configuring-unified-user.md)

