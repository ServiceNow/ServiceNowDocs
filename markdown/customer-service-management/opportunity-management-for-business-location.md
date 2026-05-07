---
title: Opportunity Management for business location
description: Integrate Service Model Foundation with Opportunity Management for Business Locations to support channel sales.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration with Sales Customer Relationship Management, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Opportunity Management for business location

Integrate Service Model Foundation with Opportunity Management for Business Locations to support channel sales.

## Overview of the integration

Use the Opportunity Management for Business Locations plugin \(com.snc.business\_organization\_opptym\) to perform the following actions.

-   Create opportunities for business locations
-   Modify and manage opportunities for the business locations
-   Track the end-to-end life cycle of opportunities
-   Enable external channel partners to track opportunities.

To create an opportunity for business location, see [Create an opportunity](https://www.servicenow.com/docs/access?context=create-new-opportunity&version=australia&pubname=australia-order-management&ft:locale=en-US).

## Data model

The Opportunity Related Channel Partner \[sn\_bus\_org\_opptym\_related\_business\_organization\] table is a list of service organizations. You can add a related party record to the table to provide access to another party that is different from the service organization associated with the customer opportunity. All related parties listed as **Authorized organizations** and associated with a particular customer opportunity have access to the opportunity, the order line items, and all other related entities. Channel partners such as referral partners, influencer partners, and more can be added as related parties to an opportunity.

|Field|Description|Type|
|-----|-----------|----|
|Opportunity|Opportunity that the related party can access.|Reference|
|Opportunity Role|Type of related party.|Reference|
|Responsibility|Responsibility associated with the related party.|Reference|
|Domain|Domain of the related party record.|Domain ID|
|Domain Path| |Domain Path|
|Class|Class of the record.|sys\_class\_name|
|Order|Numerical value assigned to determine the sequence to display the records.|Integer|
|Channel partner|Channel partner whose members can access the order when added as a related party.|Reference|
|Active|Current state of the record, whether active or inactive.|Boolean|
|Deal registration|Reference to Deal Registration \(sn\_prm\_dr\_deal\_registration\).|Reference|
|Program|Reference to Partner Program \(sn\_prm\_partner\_program\).|Reference|
|Deal Registration Type|Reference to Deal Registration Type \(sn\_prm\_dr\_deal\_registration\_type\).|Reference|

**Related topics**  


[Roles and responsibilities](personas-roles-and-tables-post-integration-oppMgmt.md)

[Activate Opportunity Management for Business Locations](../task/activate-opportunity-management-for-business-locations.md)

