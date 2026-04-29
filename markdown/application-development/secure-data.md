---
title: Secure data
description: Data security is one of the most important and overlooked aspects of creating an application. ServiceNow automatically configures access control for a new or selected role during the table creation process. Only users with the role can access the table to read, create, write, and delete.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Define and build the data model, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Secure data

Data security is one of the most important and overlooked aspects of creating an application. ServiceNow automatically configures access control for a new or selected role during the table creation process. Only users with the role can access the table to read, create, write, and delete.

Use access control rules to configure table and column-level security in the ServiceNow AI Platform. To properly configure access to an application, developers should understand how access controls work and the order in which access controls are evaluated. Apply multiple access controls that together make an Access Control List \(ACL\).

Self-Paced Training: [Securing Applications](https://developer.servicenow.com/dev.do#!/learn/courses/rome/app_store_learnv2_securingapps_rome_securing_applications)

Documentation: [Access control list rules](https://servicenow.com/docs/bundle/rome-platform-administration/page/administer/contextual-security/concept/access-control-rules.html)

When considering security:

-   Protect tables, UI pages, property pages, and other content with the appropriate access controls and roles.
-   Limit the use of GlideRecord queries in access control scripts. GlideRecord queries can affect performance.

Beginning with the Orlando Platform Subscription model, customers are charged by how many tables a user can access, regardless of whether the user does access the table. Configure ACLs to restrict access to a table to ensure that only the users that need access to a table can access the table.

**Note:** Consider making any auto-populated fields read only. If the system is populating the data, a user should not be able to.

Alternately, secure data on the ServiceNow AI Platform with before-query Business Rules. Before-query Business Rules run before the database query and are limited to controlling read access to a record. Only use before-query Business Rules when necessary. Some considerations when deciding to use Access Controls or before-query Business Rules:

-   GlideRecord queries will bypass read access controls on a table and will be restricted by before-query Business Rules on a table.
-   When access controls restrict read access to records in a list, ServiceNow shows a message saying that access has been restricted for the records. With before-query Business Rules, the number of records in the list total matches the number of records shown to the user. The user receives no indication that some records have been hidden from the list.

Review the user query Business Rule on the User \[sys\_user\] table for reference.

**Note:** Before-query Business Rules do not take the place of ACLs. Denying users access to a table via before-query Business Rule will still count the table against the subscription model. Use Access Controls to prevent the table from being counted for the users in the Platform Subscription model.

## Encryption

The ServiceNow AI Platform also provides various encryption solutions at the application tier, database tier, and hardware tier. Learn more in the [Data Encryption Whitepaper](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/resource-center/white-paper/wp-data-encryption-with-servicenow.pdf).

**Note:** Set up security before configuring any interfaces or business logic. Since security affects the data available to interfaces and business logic, waiting until the end of the application build process may cause rework and issues.

**Parent Topic:**[Define and build the data model](define-and-build-data-model.md)

