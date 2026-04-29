---
title: Extending FSO Case Types
description: You can extend from existing case types that are provided in Financial Services Operations \(FSO\) applications, enabling you to take advantage of prebuilt roles, business rules, and other business logic.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using case types and service definitions in FSO, Developer resources, Financial Services Operations \(FSO\)]
---

# Extending FSO Case Types

You can extend from existing case types that are provided in Financial Services Operations \(FSO\) applications, enabling you to take advantage of prebuilt roles, business rules, and other business logic.

All FSO applications have a base case type table. Use the base case type table when adding a new case type for that application. For example, if you need a new case type in Financial Services Treasury Operations, extend the Treasury Base Case.

For more information on the application case types that are available, see the following:

-   [Using banking applications](../../../../product/fso-common/concept/fso-banking-overview.md)
-   [Using insurance applications](../../../../product/fso-common/concept/fso-insurance-overview.md)

When implementing FSO, start with mapping your use cases to the FSO domain-level case types. This enables you to extend the prebuilt FSO applications and use the provided roles and business logic.

When a matching domain level exists, you can create a product level case type by extending the domain level case types.

## Advantages of extending FSO case types

There are several advantages to extending an FSO case type:

-   Access to base system Financial Account reference fields
-   Customer 360-degree view with Financial Accounts, Insurance Policies, Transactions, and so on
-   Ability to build playbooks and common utilities that work for many FSO Case Types
-   Contributor landing pages with Quick Links and Consolidated Case/Task Overviews
-   Inheriting Base Roles and scripts: included scripts provide business rules, client scripts, and script includes
-   Security Inheritance within the scoped admin-enabled application: roles such as fs\_agent and viewer roles in FSO Core simplify Case extension by providing all the basic access/ACLs to case types
-   Provide Financial Services related UI actions for all extensions instead of generic CSM UI actions
-   Service Definition interceptor to show the services offered
    -   Shows only the eligible Services that the customer &amp; agents can request
    -   Customer Criteria, Agent Criteria, Template, Show/Hide interceptor

**Note:** Only tables marked as “extensible” on the table definition should be extended.

For more information, see [Best Practices to Implement Case Types](https://learning.servicenow.com/nowcreate/en/pages/assets?id=nc_asset&asset_id=06f62529970b0a54496bb5bfe153af00&nc_source=copy_asset_link).

**Parent Topic:**[Using case types and service definitions in FSO](fso-int_guide-work_case_types.md)

