---
title: Customer relationships and access management
description: Reference the framework that governs every relationship and access decision across Customer Data Foundation. Its components control what parties can do, which records carry multiple parties, and how parties are related.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-relationships-and-access-management.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Customer Data Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Customer relationships and access management

Reference the framework that governs every relationship and access decision across Customer Data Foundation. Its components control what parties can do, which records carry multiple parties, and how parties are related.

## Overview of customer relationships and access management

Customer relationships and customer access management \(CAM\) is the umbrella framework that governs every relationship in Customer Data Foundation, together with the access controls those relationships imply. It provides a single set of components that every relationship entity uses. The framework centralizes the definition of who can do what. This keeps access rules declarative \(configured, not coded\), consistent \(the same definition applied everywhere\), and can be audited \(each decision traces to a named responsibility\).

## Customer relationships data model diagram

\[Omitted image "refarch-customer-relationships-and-access-management.png"\] Alt text: Customer relationships and customer access management framework showing Responsibility Definition, Related Party Configuration, and Relationship Type as the three components, and the entities that refer to them.

In the customer relationships data model diagram, responsibility access configurations and responsibility definition provide declarative access for a relationship. Related party configuration governs which records carry multiple parties. Relationship type names a relationship. Relationship entities such as account team members, contact relationships, and asset contact refer to these components.

## Framework tables

<table id="table_ckd_dly_zjc"><thead><tr><th>

Label

</th><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Responsibility definition

</td><td>

sn\_customerservice\_responsibility\_def

</td><td>

Defines what a party can do \(view, comment, escalate, close, approve, and other named actions\). Declarative; actions are configured, not coded.Every relationship and team-membership entity refers to a Responsibility Definition.

</td></tr><tr><td>

Responsibility access configuration

</td><td>

sn\_customerservice\_responsibility\_access\_config

</td><td>

Configures how a responsibility maps to access on specific record types. Supports Simple, Dependent, and Advanced patterns.Applied to a responsibility definition to determine the resulting access on records.

</td></tr><tr><td>

Related party configuration

</td><td>

 

</td><td>

Defines which records can have multiple parties with them, and what categories of related party each record supports.For example, sold products, install base items, cases, and service organizations can have multiple parties.

</td></tr><tr><td>

Sold product related party

</td><td>

 

</td><td>

Multi-party assignment to a specific sold product.

</td></tr><tr><td>

Install base related party

</td><td>

 

</td><td>

Multi-party assignment to a specific install base item.

</td></tr><tr><td>

Case related party

</td><td>

 

</td><td>

Multi-party assignment to a case, with each party's responsibility.

</td></tr><tr><td>

Service Organization Member Responsibility

</td><td>

 

</td><td>

Responsibility scope for members of a service organization, used with Service Model Foundation.

</td></tr><tr><td>

Relationship type

</td><td>

 

</td><td>

Name of a relationship, such as partner, supplier, or broker.Referenced by account relationships to name the link between two accounts.

</td></tr></tbody>
</table>## Entities that depend on the framework

Every relationship and team-membership entity in Customer Data Foundation refers to the framework. This is what makes it an umbrella: any change to a responsibility definition or a relationship type applies consistently to every entity that uses it.

|Entity|Refers to|
|------|---------|
|Account Team Members|Responsibility definition|
|Contact Relationships|Responsibility definition|
|Consumer Relationships|Responsibility definition|
|Consumer Team Members|Responsibility definition|
|Household Member Relationships|Responsibility definition|
|Household Team Members|Responsibility definition|
|Asset Contact|Responsibility definition|
|Account Relationships|Relationship type|

## Principles of framework

-   Define relationships between parties \(organization, user, entity, group\) using named Relationship Types.
-   Manage access control between an entity and an organization or user through Responsibility Definitions and Responsibility Access Configurations.
-   Configure which record types can carry multiple parties, and what categories of party each supports, through Related Party Configuration.

**Related topics**  


[Configuring customer access management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configuring-cam.md)

[Create a responsibility definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/t_CreateAResponsibilityDefinition.md)

[Configure access through the responsibility access configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/declarative-resposibility-framework.md)

[Create related party configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/adding-related-party-config-to-case.md)

[Service Model Foundation overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-industry-data-model.md)

