---
title: Retail case types
description: Retail case types are designed to address various business needs and streamline workflows for store-level and HQ-driven task management.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Retail]
---

# Retail case types

Retail case types are designed to address various business needs and streamline workflows for store-level and HQ-driven task management.

![Diagram showing a common retail operations workflow.](../image/z-retail-workflow1.png)

Case types are needed when an organization has different processes for supporting customers across multiple use cases, departments, business units, or products. Case types help to separate these processes through separate applications to support each process.

Retail customers have a diverse set of processes for end customers. Depending on how distinct these processes are, each type of process could be a separate case type. In conclusion, if the extension requires capturing of newer attributes that fit the new use case, use case types. If the same attributes of the retail base case can handle slightly different use cases, use service definitions.

Example: Various issues such as reporting an issue, recall, theft at the store, reporting a crash, and safety issues can share the same set of captured attributes. They differ primarily in their processes. These processes include capturing attributes, following a playbook, applying business rules, and fulfillment. You can use the same case type of retail base case and define these use cases as different service definition on top of it .

For each case type, you must create a table that extends the retail base table. You must also configure several items, such as business rules and client scripts. These configurations drive customer issues of this type from creation to resolution.

**Note:** Customers using the retail case table will no longer be able to create cases or update the existing cases. Customers should use case types instead.

The case types available are:

[Store inquiry case](rahi-retail-retail-store-services.md)

[Customer complaint case](rahi-retail-retail-customer-complaint.md)

[HQ communications case](rahi-retail-retail-hq-operations.md)

[In-store operations case](rahi-retail-retail-in-store-operations.md)

Customers can also extend their own case types other than the newly added case types. For more information on these changes, see [KB2216547](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2216547).

-   **[Store inquiry case](rahi-retail-retail-store-services.md)**  
The store inquiry case type facilitates seamless communication between store teams and headquarters, enabling efficient exchange of operational queries, information, and issues. This case type is included in the Retail store services plugin.
-   **[Customer complaint case](rahi-retail-retail-customer-complaint.md)**  
The customer complaint case type helps manage and resolve customer feedback related to store experiences. This case type enables customers to submit complaints anonymously to encourage honest feedback and help stores improve their service. This case type is included in the Retail customer complaint plugin.
-   **[HQ communications case](rahi-retail-retail-hq-operations.md)**  
The HQ communications case enables effective coordination between HQ teams. It facilitates the execution of assigned work and allows HQ teams to monitor progress. This case type is included in the Retail HQ operations plugin.
-   **[In-store operations case](rahi-retail-retail-in-store-operations.md)**  
The in-store operations case type allows store team members to report and track in-store operational issues, whether for routine or cyclical demands. This ensures that issues are documented and monitored for consistent execution and support. This case type is included in the Retail in-store operations plugin.

**Parent Topic:**[Exploring Retail](rahi-retail-operations-explore.md)

