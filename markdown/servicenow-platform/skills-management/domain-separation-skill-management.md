---
title: Domain separation and Skills Management
description: Domain separation is supported in the Skills Management app, and configured to apply to all features of the application. Separation of data is configured along with separation of logic and process.
locale: en-US
release: australia
product: Skills Management
classification: skills-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference for Skills Management, Skills Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Skills Management

Domain separation is supported in the Skills Management app, and configured to apply to all features of the application. Separation of data is configured along with separation of logic and process.

Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## How domain separation works in Skills Management

Domain separation is supported in Skill Management with no explicit setup or configuration requirements. Skills, skill categories, skills levels can be created in separate domains, including the global domain. When domain separation is implemented, people with skill app roles can view skill information only in the domain assigned. **Domain** and **Domain Path** columns are available for all Skill tables provided with the base system. The **Domain** column contains the name of the domain to which the event or alert belongs, and the **Domain Path** column contains the unique domain identifier.

|Table name|Description|
|----------|-----------|
|sys\_user\_has\_skill|User skill information|
|cmn\_skill|Main skill table|
|cmn\_skill\_category|Define skill categories|
|cmn\_skill\_level\_type|Define skill level type|
|cmn\_skill\_level|Define skill level|
|sys\_group\_has\_skill|Group skills|
|cmn\_skill\_contains|Define skills contained within skills|
|task\_m2m\_skill|Task skill information|

**Note:** If the domain column is not shown, click the **Update Personalized List** icon and add the required column. You can also add the domain path column, if desired.

Use cases:

-   A Skill Manager that belongs to the Acme domain creates a skill and wants to view and associate it to user in the Acme domain. A user must belong to the Acme domain, its parent domain, or the global domain to view the skill record.
-   A Skill Manager that belongs to a parent domain tries to view a skill in a child domain. The user of a parent domain can view a skill record of the parent as well as all child domains of that parent.
-   A Skill Manager that belongs to a parent domain wants to create/associate a skill on behalf of another user in the Acme domain. A user must belong to the same domain as the user for which the skill record is created.
-   A Skill Manager wants to associate a record for an integrated application in the Acme domain. A user must belong to the domain of the integrated application from which a record is associated.
-   A Skill Manager has access to multiple domains but wants to update a record with content within a specific domain. The domain specified for the current record drives the functionality of that record and reference fields.

