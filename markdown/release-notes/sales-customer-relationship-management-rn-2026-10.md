---
title: Version 1.0
description: Extend task plan template orchestration to Sales Customer Relationship Management \(Sales CRM\) customers, and generate templates automatically with an enhanced AI Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/sales-customer-relationship-management-rn-2026-10.html
release: brazil
topic_type: topic
last_updated: "2026-09-28"
reading_time_minutes: 1
keywords: [Task Plan Template, AI Agent, Order Orchestration, Legal Name, Order Integrator]
breadcrumb: [Sales CRM for Telecommunications release notes, Telecommunications, Media, and Technology release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Version 1.0

Extend task plan template orchestration to Sales Customer Relationship Management \(Sales CRM\) customers, and generate templates automatically with an enhanced AI Agent.

## What's new

-   **Task plan templates for Sales Customer Relationship Management \(Sales CRM\)**

    Define and use task plan templates without a Sales Customer Relationship Management for Telecommunications \(SOMT\) license. Define task plan templates, task plan items, and dependencies, and trigger them based on order action \(add, change\) and product type.

-   **AI Agent for template-driven order orchestration**

    Generate reusable orchestration templates with an enhanced conversational AI Agent instead of a flat task list. When no template exists for a product specification, the agent converts an uploaded fulfilment-journey image into a draft template, or proposes one from the closest matching specification's past orders. Product Catalog Managers define dependencies and publish the template, which then automatically orchestrates the current and all future orders for that specification and action.


## What's changed

-   **Legal name persistence during account creation**

    Legal name entered during account creation is now correctly persisted. Previously, the value was mapped to a database field that did not exist.

-   **Order integrator role no longer blocks other roles from creating consumers and locations**

    Fixed an access control issue where the order integrator role's create permissions on Consumer and Location records inadvertently blocked other roles, such as CSM Agent, from creating those records.


**Parent Topic:**[Sales CRM for Telecommunications release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/sales-customer-relationship-management-rn.md)

