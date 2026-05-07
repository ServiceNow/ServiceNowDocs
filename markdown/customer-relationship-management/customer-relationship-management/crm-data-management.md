---
title: Data management
description: The ServiceNow CRM portfolio is built on a shared data foundation. The data models, customer records, product information, user roles, and service structures that underpin CRM are defined once and used across multiple products, including Customer Service Management \(CSM\), Field Service Management \(FSM\), Sales CRM, and industry solutions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 6
---

# Data management

The ServiceNow CRM portfolio is built on a shared data foundation. The data models, customer records, product information, user roles, and service structures that underpin CRM are defined once and used across multiple products, including Customer Service Management \(CSM\), Field Service Management \(FSM\), Sales CRM, and industry solutions.

## Customer service value chain

This shared data foundation ensures that every team works from the same information without duplication or manual synchronization.

![Shows the value that service organizations can provide to companies,employes and staff, and customers](../image/crm-customer-service-value-chain.png "Customer service value chain")

The CRM data management layer models the complete customer service value chain:

-   The company that offers products and services.
-   The service organizations \(branches, stores, offices, hospitals\) that deliver those services.
-   The employees and staff who work at those organizations.
-   The products and services themselves.
-   The customers who consume them.

Every data domain in the CRM portfolio maps to one of these entities.

|Entity|What it represents|
|------|------------------|
|Company|The organization building and offering products and services to end customers. This is the provider side of the service relationship: an enterprise, government agency, or other entity.|
|Service organizations|Internal or external entities of the company that serve customers directly. Includes branches, stores, franchises, offices, hospitals, and other service locations.|
|Employees and staff|People working at the internal and external service organizations: agents, technicians, fulfillers, managers, and specialists who deliver service.|
|Products and services|Physical and digital products and services that the company offers. Includes product models, sold products, install base items, contracts, and entitlements.|
|Customers|Individuals and organizations external to the company who consume products and services. Includes accounts, contacts, consumers, and households across B2B, B2C, and B2B2C models.|

## Customer service business models

The CRM data foundation supports several business models that determine how customer data is organized and how service is delivered. The business model defines which customer entities are used: accounts and contacts for B2B, consumers and households for B2C, or a combination of all entities for B2B2C. The business model also defines how access, relationships, and case routing are configured.

Beyond the core business models, the Service Model Foundation \(SMF\) framework and the contributor user model extend the data foundation to support complex organizational structures and cross-functional service delivery. SMF introduces service organizations, business locations, and location-based roles that provide the flexibility to model multi-tier service structures across industries. The contributor user model enables internal employees outside the front-line service team, such as back-office specialists and middle-office workers, to participate in case resolution through scoped access and task assignment.

![Shows the direct models (B2B, B2C) and the multi-level models (B2B2C, B2B2E)](../image/crm-csm-business-models.png "Customer service business models")

Together, these models and frameworks give organizations the ability to configure a CRM environment that matches how they sell, service, and support their customers.

|Business model|Description|
|--------------|-----------|
|B2B|In the business-to-business \(B2B\) model, the company provides products and services to other businesses. Customer data is organized around accounts \(organizations\) and contacts \(employees of those accounts\). The B2B model also supports customer relationships and account teams.|
|B2C|In the business-to-consumer \(B2C\) model, the company provides products and services directly to individual consumers. Customer data is organized around consumers and households.|
|B2B2C|In the business-to-business-to-consumer \(B2B2C\) model, the company supports business customers who, in turn, serve end consumers. Customer data spans accounts, contacts, and account consumers supporting multi-level relationships where a business customer's individual customers also need access to service.|
|B2B2E|In the business-to-business-to-employee \(B2B2E\) model, the company delivers products or services to another business, which then extends these offerings to its employees. The intermediary organization may be involved in procurement, customization, implementation, support, and training for its corporate employees.|
|SMF|The SMF framework expands the B2B and B2C models by introducing service organizations, internal and external business locations, households, and the relationships between these entities. SMF provides the core framework, security, and role-based access needed to model complex service structures across industry verticals.|
|Contributor users|The contributor user model provides unified customer support for internal and external customers. With this model, organizations can engage middle-office teams to resolve customer issues and requests, enabling employees to request support for themselves and for external customers, enabling service organizations to serve one another, and enabling middle-office agents to work on specific tasks required to resolve a case.|

## Customer data foundation

The customer data foundation provides the capabilities for modeling, managing, and maintaining customer data across the CRM portfolio. It covers four areas: the core data model for customers and their relationships, access management that controls who can see and act on customer data, unified identity for users who hold multiple roles, and data privacy and quality tools.

<table id="table_b5k_2yt_4uf"><thead><tr><th>

Capability

</th><th>

What it provides

</th></tr></thead><tbody><tr><td>

Data models

</td><td>

Models external customers and their relationships. Supports B2B \(accounts and contacts\), B2C \(consumers and households\), and B2B2C \(account consumers\) structures, along with customer profiles, addresses, relationships, and roles.

</td></tr><tr><td>

Customer access management

</td><td>

Provides configurable, granular access to CRM data through relationships and related parties, including:-   **Responsibilities**: Named access levels \(such as Authorized Representative or Account Manager\) that determine what a related party can see and do.
-   **Related Party Framework**: Links contacts, consumers or accounts to records \(such as cases, sold products, or install base items\) as related parties with assigned responsibilities so multiple users can collaborate on the same record with different access levels.
-   **Declarative Responsibility Framework**: A low-code/no-code framework for defining responsibility access configurations, reducing the need to write custom ACL scripts.

</td></tr><tr><td>

Unified customer identity

</td><td>

Models a CRM user with multiple functions or personas, both internal and external. Supports scenarios such as an employee who is also a consumer, or a contact who is also a consumer, through a unified user record.

</td></tr><tr><td>

Customer data privacy and quality

</td><td>

Manages data privacy compliance and maintains clean, accurate customer data including data classification.

</td></tr></tbody>
</table>## In this section

-   **[Data models](crm-data-models.md)**

    Understand the layered data architecture underpinning the CRM portfolio, including how the Now Platform, CRM Foundation, Customer Workflows \(Sales CRM, CSM, FSM\), and Industry Workflows relate to each other.

-   **[Customer data](crm-customer-data.md)**

    Configure and manage accounts, contacts, consumers, and households, the core customer records that agents, sales teams, and technicians rely on across the CRM portfolio.

-   **[User management](crm-user-management.md)**

    Define and organize internal and external users, assign roles and group memberships, and control access to CRM features and case data

-   **[Product data](crm-product-data.md)**

    Understand how product models, sold products, install base items, and installed products give agents and customers a shared view of what has been purchased and how it is deployed.

-   **[Product catalog](crm-product-catalog.md)**

    Understand how products and services are defined in the catalog and how catalog items connect to product models to enable self-service requests and order management.

-   **[Service Model Foundation](crm-service-model-foundation.md)**

    Understand the framework that models service organizations, internal and external business locations, and the relationships between them.

-   **[Partner relationship management](crm-partner-relationship-mgmt.md)**

    Understand how channel partners are onboarded, managed, and enabled to sell and support customers through partner programs, deal registration, and the partner workspace.


