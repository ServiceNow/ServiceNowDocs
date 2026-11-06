---
title: Data models
description: The CRM portfolio is built on a layered data architecture in which each tier inherits from the tier below it. The four layers \(ServiceNow AI Platform, CRM Foundation, Customer Workflows, and Industry Workflows\) are connected by shared objects that you configure, extend, and build on for CRM implementations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-relationship-management/crm-data-models.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Data foundations, Customer Relationship Management]
---

# Data models

The CRM portfolio is built on a layered data architecture in which each tier inherits from the tier below it. The four layers \(ServiceNow AI Platform, CRM Foundation, Customer Workflows, and Industry Workflows\) are connected by shared objects that you configure, extend, and build on for CRM implementations.

## CRM architecture

The CRM portfolio is organized into four tiers.

\[Omitted image "crm-product-architecture-ai-platform.png"\] Alt text: Architecture that shows the ServiceNow AI Platform as the bottom layer, with CRM Foundation components, Customer Workflows, and Industry Workflows.

At the base, the ServiceNow AI Platform provides the core tables, AI capabilities, and engines that every ServiceNow product inherits. Above it, the CRM Foundation defines the shared data objects \(Customer, Organization, Territory, Product, and Pricing\) along with shared engines. It also defines the transactional objects \(Opportunity, Quote, Order, Install Base, Contract, Case, Work Order\) that all CRM products use. The Customer Workflows tier delivers the three core CRM products at the same level: Sales CRM, Customer Service Management \(CSM\), and Field Service Management \(FSM\). At the top, Industry Workflows provide preconfigured solutions for verticals including Telecom, Technology, Financial Services, Public Sector, Healthcare, Retail, and Manufacturing.

Sales CRM, CSM, and FSM aren't separate systems sharing data through integrations. They're three products built on the same CRM Foundation and platform data model. A company record, a person record, a product, a contract—each exists once in the CRM Foundation. All three products and every industry solution built on them use these shared records.

## Layer 1: ServiceNow AI Platform base

Every ServiceNow product is built on the same core tables. These base objects aren't replicated per product; they are inherited. When a Case is created in CSM, it extends the same Task record that an ITSM incident extends. When an Order is created in Sales CRM or a Work Order in FSM, both extend the same Task record. The same holds for person records, company records, and SLA logic. This layer also includes Predictive AI and GenAI capabilities.

|Platform object|Table name|What it does|
|---------------|----------|------------|
|Task|task|Master table for all transactional records. Cases, Incidents, Work Orders, and Orders all extend Task, inheriting state, priority, assignment, and SLA fields.|
|User|sys\_user|Single person record shared across all products. CSM contacts, ITSM agents, and HR employee records are stored in this table or in tables that extend it.|
|Company|core\_company|Base organization record. The Account \[customer\_account\] table extends this table, so one company record is used across all modules.|
|CMDB/CI|cmdb\_ci|Configuration Management Database. Install Base Items reference configuration items \(CI\) here, linking customer product deployments to IT infrastructure.|
|SLA engine|contract\_sla|Platform-level SLA engine shared by CSM Entitlements and Sales CRM Contracts. Provides consistent SLA behavior across Cases, Orders, and Work Orders.|

## Layer 2: CRM Foundation

The CRM Foundation is the shared data layer that all three Customer Workflow products build on. It contains the core data objects that define customers, products, and service commitments, along with the transactional objects that Sales CRM, CSM, and FSM operate on. These objects are created once and consumed by all three products without duplication.

|Foundation object|Table name|What it does|
|-----------------|----------|------------|
|Account|customer\_account|Extends core\_company. Central hub for contacts, cases, contracts, and opportunities. Shared across Sales CRM, CSM, and FSM.|
|Contact|customer\_contact|Extends sys\_user. Represents a person at a customer account. Used for case routing in CSM, opportunity contacts in Sales CRM, and site contacts in FSM.|
|Consumer|csm\_consumer|Standalone table that stores the profile of an individual customer in a B2C model. Doesn’t extend sys\_user. Consumers interact through assisted service channels, or through self-service portals when linked to a consumer user record.|
|Consumer User|csm\_consumer\_user|Extends sys\_user. Stores the login record for a consumer who accesses self-service portals. Created when a consumer self-registers and linked to the corresponding consumer record.|
|Household|csm\_household|Groups consumers who share an address and common products or services. Supports a designated head of household with visibility into cases and account information for all members.|
|Product Model|cmdb\_model|Defines a product or service template. Sales CRM extends it with pricing through Product Offerings; CSM references it for case context.|
|Sold Product|sn\_install\_base\_sold\_product|Tracks a product or service sold to an account or consumer. Created by Sales CRM on order fulfillment; referenced by CSM cases and FSM work orders.|
|Install Base Item|sn\_install\_base\_item|Specific deployed instance with serial number. References a CMDB CI. Visible to agents in CSM and technicians in FSM.|
|Contract|ast\_contract|Defines the type of support a customer receives. Created during the sales motion in Sales CRM; verified by CSM on every case to confirm support terms.|
|Entitlement|service\_entitlement|Defines SLA tiers, support hours, and covered channels. Set by Sales CRM during the sales motion; auto-verified by CSM when an agent opens a case.|

**Note:** The products listed in the "What it does" column highlight the primary Customer Workflow products \(Sales CRM, CSM, FSM\) that operate on each foundation object. Industry Workflows such as Telecom, Technology, Financial Services, Public Sector, Healthcare, Retail, and Manufacturing also inherit and use these same foundation objects through the Customer Workflow products they build on.

<table id="table_hb5_rb5_y3c"><thead><tr><th>

Engine/capability

</th><th>

What it does

</th></tr></thead><tbody><tr><td>

Product Configuration Engine

</td><td>

Manages product bundles, compatibility rules, and configuration options.Primary consumer is Sales CRM during quoting and ordering. Also used by CSM during sold-product modification flows and by Industry Workflows that extend Sales CRM with vertical-specific configuration logic.

</td></tr><tr><td>

Pricing Engine

</td><td>

Applies pricing rules, discounts, and rate calculations to Product Offerings.Primary consumer is Sales CRM during the quote and order process. Also invoked by CSM modification flows and Industry Workflows that price quotes and orders.

</td></tr><tr><td>

Scheduling Optimization

</td><td>

Optimizes technician scheduling and dispatch in FSM based on location, skills, availability, and SLA requirements.FSM is the primary consumer. Industry Workflows with field operations, such as Telecom and Healthcare, also use it.

</td></tr></tbody>
</table>## Customer entities by business model

The CRM Foundation customer entities are organized into two categories: organization entities that represent companies and groupings, and individual entities that represent people. Which entities are used depends on the business model. B2B implementations use accounts and contacts. B2C implementations use consumers and households. B2B2C implementations combine both, adding account consumers to support business customers who serve end consumers. A single deployment can support all three models simultaneously.

|Entity type|B2B entities|B2C entities|B2B2C entities|
|-----------|------------|------------|--------------|
|Organization entities|Account \(customer\_account\), Partner Account \(customer\_account\)|Household \(csm\_household\)|Account + Household|
|Individual entities|Contact \(customer\_contact\), Partner Contact \(customer\_contact\)|Consumer \(csm\_consumer\), Household Member \(csm\_household\_member\)|Contact + Account Consumer \(csm\_consumer\)|

## Layer 3: Customer Workflows \(Sales CRM, CSM, and FSM\)

The Customer Workflows tier contains the three core CRM products at the same level: Sales CRM, CSM, and FSM. Each product operates on the shared CRM Foundation objects and adds its own product-specific objects. A record created in one product is immediately available to the others.

-   **Customer Service Management \(CSM\)**

    CSM answers three questions for every service interaction: Who is the customer? What do they own? What are they entitled to? CSM uses the shared CRM Foundation objects to answer these questions. Case is the CSM specific object that ties them together.

    |CSM object|Table name|What it does|
    |----------|----------|------------|
    |Case|sn\_customerservice\_case|Extends Task. Central record for every service interaction. Connects Who \(Account/Contact/Consumer\), What \(Product/Asset\), and What’s Owed \(Contract/Entitlement\). Supports omnichannel intake.|

-   **Sales CRM**

    Sales CRM adds the full sales motion on top of the CRM Foundation, from Lead through Opportunity, Quote, Order, and Fulfillment. After fulfillment, the shared CRM Foundation objects take over. Sold Products, Contracts, and Entitlements are immediately available to CSM and FSM with no handoff required.

    |Sales CRM object|Table name|What it does|Stage|
    |----------------|----------|------------|-----|
    |Lead|lead|Prospective customer. Converts to Opportunity and Account/Contact on qualification.|Prospect|
    |Opportunity|opportunity|Potential deal linked to an Account. Tracks sales stage; one-to-one with a Quote.|Qualify|
    |Product Offering|sn\_prd\_pm\_product\_offering|Extends Product Model with pricing rules, bundles, and compatibility rules.|Configure|
    |Quote \(ServiceNow CPQ\)|quote|Priced proposal generated by the ServiceNow CPQ configurator. Applies pricing rules and bundles in real-time.|Price|
    |Order|sn\_order\_mgmt\_order|Confirmed purchase. Extends platform Task and triggers downstream fulfillment workflows.|Order|
    |Fulfillment Task|sc\_task|Extends platform Task. Represents individual work steps executed during order fulfillment.|Fulfill|

-   **Field Service Management \(FSM\)**

    FSM adds field operations capabilities on top of the CRM Foundation. Work Order is the FSM-specific object. FSM consumes shared Account, Contact, Install Base Item, Contract, and Entitlement records, so technicians arrive with the same customer context that agents and sales teams see. Scheduling Optimization from the CRM Foundation handles technician routing and dispatch.

    |FSM object|Table name|What it does|
    |----------|----------|------------|
    |Work Order|wm\_order|Extends Task. Represents a field service job dispatched to a technician. References the same account, contact, install base, and entitlement records from the CRM Foundation.|


## Layer 4: Industry Workflows

The top tier provides preconfigured solutions for Telecom, Technology, Financial Services, Public Sector, Healthcare, Retail, and Manufacturing. Each industry solution extends the CRM data model with domain-specific entities, such as subscriber records for telecom, policy records for financial services, or patient records for healthcare. These solutions inherit every shared object and engine from the layers below them.

Industry Workflows build on top of the CRM Foundation and Customer Workflows; they don't replace them. A telecom agent still works with the same Case, Account, Contact, and Entitlement objects that any CSM agent uses. The workspace, playbooks, and data model extensions are preconfigured for telecommunications workflows. Organizations can deploy an industry solution as a starting point and modify it as requirements evolve.

## How the layers connect

The connection between Sales CRM and CSM is structural, not integration-based. Because both products share the same underlying records, completing an order in Sales CRM immediately updates what CSM sees. There's no batch sync, no middleware, no delay.

-   Order fulfillment in Sales CRM creates Sold Product and Install Base Item records in the CRM Foundation, available immediately to CSM for case handling.
-   Contracts and Entitlements set during the sales motion are auto-verified when a CSM agent opens a Case. No manual lookup.
-   Account, Contact, and Product Model records are written once and read by both products. Changes are reflected everywhere instantly.
-   FSM work orders reference the same account, contact, and install base records, so technicians see the same customer context as agents and sales teams.

This structural connection is what makes the sell, fulfill, and service story coherent. It isn't a workflow between systems; it's a single data model with multiple operational views.

**Related topics**  


[Customer data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-data.md)

[User management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/user-management.md)

[Product data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/product-data.md)

[Data models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/data-models.md)

[Configure Service Model Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-industry-data-model.md)

