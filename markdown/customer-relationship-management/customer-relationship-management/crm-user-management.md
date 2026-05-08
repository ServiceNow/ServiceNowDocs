---
title: User management
description: Configure internal and external users, assign roles and group memberships, and control access to CRM features and case data. Establish the user structures that support case routing, team collaboration, and portal access across the CRM portfolio.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-30"
reading_time_minutes: 6
---

# User management

Configure internal and external users, assign roles and group memberships, and control access to CRM features and case data. Establish the user structures that support case routing, team collaboration, and portal access across the CRM portfolio.

## Users and groups

A user is any individual who can access the CRM environment. A group is a set of users who share a common purpose. Roles and assignment rules applied to a group are automatically inherited by all members, so access and routing can be managed at the team level rather than individually. Group information is used across CRM processes for assigning work to teams and requesting approvals.

Users and groups can be imported or created directly using the platform user administration feature. After users are configured, roles are assigned to control what each user can see and do.

## Roles and access control

Roles control access to features, capabilities, and data in the CRM portfolio. The Customer Service Management application provides two categories of roles: internal roles for agents and managers, and external roles for customers, partners, and consumers. Roles can be assigned to individual users or to groups. When assigned to a group, all members inherit those roles.

**Internal roles** are assigned to employees who handle cases, manage service operations, or support customers through the CSM Configurable Workspace.

|Role|Role name|What it covers|
|----|---------|--------------|
|Service agent \(B2B\)|sn\_customerservice\_agent|Handles cases on behalf of business customers. Has access to case management, customer records, and agent tools in the configurable workspace.|
|Consumer agent \(B2C\)|sn\_customerservice.consumer\_agent|Handles cases for individual consumers in a B2C service model. Works with consumer profiles, households, and the consumer service portal.|
|Service manager|sn\_customerservice\_manager|Oversees service operations across B2B and B2C models. Manages queues, account teams, contact relationships, and has broader visibility across cases, teams, and performance data.|

**External roles** are assigned to customers, partners, and consumers who access the CRM through self-service portals. External roles control what these users can see, submit, and manage.

|Role|Role name|What it covers|
|----|---------|--------------|
|Customer \(B2B\)|sn\_customerservice.customer|Submits and views cases through the customer portal. Can view assets and service contracts associated with their account.|
|Customer administrator \(B2B\)|sn\_customerservice.customer\_admin|Manages cases and contacts across their account or account hierarchy. Has broader visibility than a standard customer role.|
|Customer case manager \(B2B\)|sn\_customerservice.customer\_case\_manager|Manages cases for their account with case management capabilities beyond the standard customer role.|
|Partner \(B2B\)|sn\_customerservice.partner|Creates and manages cases on behalf of the customer accounts they support. Can view assets and service information for partner-managed accounts.|
|Partner administrator \(B2B\)|sn\_customerservice.partner\_admin|Manages contacts, cases, and account information across the partner’s customer accounts with administrative access.|
|Consumer \(B2C\)|sn\_customerservice.consumer|Accesses services through the consumer portal. Submits and tracks cases, views products, and manages personal information.|

## Contributor users

Contributor users are internal or external employees who participate in resolving customer issues without full agent access. These are typically back-office specialists, middle-office team members, or employees from shared service organizations brought in for specific case tasks. The contributor user model supports unified customer support where shared service teams can serve both internal and external customers.

The contributor users feature enables three capabilities: service organizations can serve one another and external customers, employees can request support for themselves and for external customers, and middle-office agents can work on specific tasks required to resolve cases.

**Contributor roles** control what each contributor type can see and do. Each role maps to a specific requester scenario.

|Contributor type|Role name|What they can do|
|----------------|---------|----------------|
|Account contributor|sn\_customerservice.account\_contributor|Creates cases on behalf of any customer. Works with accounts and contacts. Uses the Customer Service Portal to assist customers.|
|Consumer contributor|sn\_customerservice.consumer\_contributor|Creates cases on behalf of any consumer. Works with consumers and households. Uses the Consumer Service Portal to assist consumers.|
|Relationship contributor|sn\_customerservice.relationship\_contributor|Creates cases on behalf of customers with whom they have an established relationship. Can view and follow up on all cases for related customers. Can update customer data such as contacts and addresses.|
|Self contributor|sn\_customerservice.self\_contributor|Creates cases on behalf of themselves as an internal employee. Uses the portal to request support for their own issues.|
|Service organization contributor|sn\_customerservice.service\_organization\_contributor|Creates cases on behalf of customers associated with their service organization. Operates within the Service Model Foundation hierarchy.|

**Viewer roles** provide read-only access to case data and customer records without the ability to create or modify them.

|Viewer role|What it provides|
|-----------|----------------|
|Case viewer|Enables employees to view case records without the ability to create or modify them.|
|Case task viewer|Enables employees to view case task records without the ability to create or modify them.|
|Customer data viewer|Enables employees to view core customer data \(accounts, contacts, consumers\) without the ability to modify records.|

## Account teams

Account teams bring together employees and customer contacts who fulfill specific roles in supporting a particular account. Teams are built using responsibility definitions, named roles that the administrator creates and assigns to team members. There are two types of responsibility definitions: one for employees \(internal users\) and one for contacts \(external users\).

After responsibility definitions are created, the customer service manager can build an account team by selecting an account, choosing a role, and assigning it to an employee. The manager can also add a contact relationship to an account by selecting a role and assigning it to a contact. Account team members with an account manager responsibility can view information and perform actions on behalf of the account, such as creating or updating cases from the customer portal.

## Customer access management

Customer access management enables multiple contacts and consumers to participate in a case or track a sold product, each with a defined level of access. This capability supports complex use cases across industry verticals, such as a loan application where a co-borrower, guarantor, and attorney all need access to the same case, or a product tracked by both a finance team \(for renewals\) and an operations team \(for maintenance\).

When adding related parties to a case, agents select a relationship type that determines the access level for each party. Customer access management improves the customer experience by enabling related parties to track and collaborate on cases, improves operational efficiency by enabling customers to track cases for products and services, and increases automation by automatically granting access to cases based on access to the sold product.

|Configuration task|What it does|
|------------------|------------|
|Responsibility definition|Defines a role or responsibility that controls what a related party can see and do on a case or sold product.|
|Responsibility access configuration|Configures the access level for each responsibility definition using the declarative responsibility framework.|
|Related party configuration|Links related party entity responsibilities to responsibility definitions. Determines which relationship types are available when adding related parties to a case.|

## Unified user profiles

The unified user feature allows a single individual who holds both an internal and external identity to maintain multiple profiles with one login and switch between them seamlessly. This eliminates the need to create and manage multiple user accounts for the same individual.

Before unified profiles, the platform prevented a user from holding both the snc\_internal and snc\_external roles simultaneously due to role collision. The unified consumer role resolves this by operating independently of both roles, enabling scenarios where an employee is also a consumer.

The following list describes some of the supported scenarios.

-   An employee who is also a consumer \(B2C\). For example, a bank employee who also holds a personal account at the same bank.
-   A user with multiple external profiles. For example, a consumer who has a patient profile in healthcare and a constituent profile in public sector services.
-   A user with profiles across CSM and other ServiceNow applications. For example, a user with a CSM account for vendor support and a VRM account for vendor risk management.

Individual consumers can have multiple profiles for different needs. Consumer profiles allow organizations to identify and differentiate profile-specific data for the same user. For example, a patient profile and a constituent profile for the same individual. Each profile maintains its own data while sharing the underlying user record.

**Related topics**  


[bundle-csm.user-management]

[bundle-csm.customer-data]

[bundle-csm.csm-workspaces-configure]

[bundle-csm.awa-csm-overview]

[bundle-csm.set-up-self-service]

[bundle-csm.r_RolesInstalledWithCustomerService]

