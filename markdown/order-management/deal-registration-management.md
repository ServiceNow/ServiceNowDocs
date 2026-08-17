---
title: Deal Registration
description: Install the Deal Registration Management plugin \(com.snc.deal\_registration\_management\) to enable channel partners to identify and manage customer interest in products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/deal-registration-management.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 4
breadcrumb: [Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Deal Registration

Install the Deal Registration Management plugin \(com.snc.deal\_registration\_management\) to enable channel partners to identify and manage customer interest in products.

## Key benefits of Deal Registration

The Deal Registration Management application \(com.snc.deal\_registration\_management\) offers the following benefits to channel partners:

-   Deal registration forms that support multiple models, products, or partner programs.
-   Reduced manual follow-up for tracking deal registrations and related information.
-   Flexibility for channel partners to create deal registrations.
-   Deal lifecycle tracking through the enterprise CRM system to convert registrations to opportunities.

## Deal lifecycle

A typical deal registration follows this lifecycle:

1.  **Draft**: Deal is created but not yet submitted.
2.  **Submitted**: Deal is submitted for initial review.
3.  **Under Review**: Deal is being evaluated by internal team.
4.  **Pending Approval**: Deal is routed through approval workflow.
5.  **Approved**: Deal receives all required approvals.
6.  **Closed**: Deal work is completed and opportunity is created.
7.  **Canceled**: Deal is canceled and no longer active.

## User personas in Deal Registration

Deal registration involves several key personas:

-   Deal agents \(Enterprise B2B and B2C\): Create deals, Preview and submit for approval, and manage tasks.
-   Enterprise Relationship Managers: Oversee deals under their hierarchy.
-   Enterprise Contributors: Manage deals for their channel partners.
-   Deal registration admin: Configure approval rules, manage all deal records and tasks.
-   Internal team members: Work on deal-related tasks such as account creation and conformance review.

## Set up Deal Registration

Deal registration provides channel partners exclusive rights to work on a particular deal or customer for a period of time.

Install the Deal Registration Management plugin \(com.snc.deal\_registration\_management\). See [Install Deal Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-deal-registration-management.md).

Deal registrations and deal registration line items help to manage and track the products that are associated with submitted deal registrations. The Deal Registration Management plugin can promote trust and transparency between enterprises and their partners.

|Task|Description|Role|
|----|-----------|----|
|[Install Deal Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-deal-registration-management.md)|Install the Deal Registration Management application from ServiceNow® Store.|admin|
|[Data model for Deal Registration Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/data-model-for-deal-registration-management.md)|Add data in the deal registration tables to maintain and track deals and the line items linked to a deal registration..|Experience \(sn\_prm\_dr.deal\_reg\_ui\)|
|[Roles and components of Deal Registration Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/roles-and-components-of-deal-registration-management.md)|The Deal Registration Management \(com.snc.deal\_registration\_management\) application uses roles to provide access to information and identify internal and external users. Roles also maintain data security and establish different types of relationships between segments and partners.|admin|

## Deal Registration approvals

Deal registration approvals provide a configurable workflow to verify that deals are reviewed and approved by the appropriate team members.

Deal registration approvals use the [Advanced Approval Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-advanced-approval-for-sales.md) framework to create multi-step, configurable approval chains. This framework lets you define when approvals are required and who must approve at each step.

The approval process has two layers: configuration and runtime. During configuration, an administrator sets up approval configurations, trigger conditions \(when approvals are needed\), approval rules \(who approves\), and approval chains \(the sequence of approvers\). At runtime, users submit deals for approval, and the system routes approval requests to the appropriate approvers based on the configuration.

When you submit a deal for approval, you see a preview showing which approvers receive the request and in what order. After approval by all required approvers, the deal moves to the approved state.

Key approval concepts:

-   Approvals are based on trigger conditions, for example, deal size is less than $1 million.
-   Approval rules determine who receives approval requests based on deal characteristics.
-   Deal agents can submit any deal for approval, not just deals they created.
-   Approvers must be explicitly assigned an Approver role to access approval requests.
-   Approvals can have multiple steps with sequential or parallel review.

## Deal Registration tasks

Deal registration tasks provide a centralized way to organize and track all work items associated with a deal.

Key task concepts:

-   Tasks can be created whenever a deal is in an active state, excluding **Draft**, **Completed**, or **Canceled**.
-   Tasks can be assigned to any internal ServiceNow® user, beyond deal agents.
-   Non-deal users automatically receive the Fulfiller role to work on assigned tasks.
-   Each deal can have zero to many tasks based on work requirements.
-   Tasks are visible in the Partner CSM Configurable Workspace but not on the Partner portal.
-   When a deal is archived or deleted, all associated tasks are automatically archived or deleted.

-   **[Install Deal Registration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-deal-registration-management.md)**  
Install the plugin \(com.snc.deal\_registration\_management\), along with the demo data and installations that are related to ServiceNow® Store applications and plugins.
-   **[Data model for Deal Registration Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/data-model-for-deal-registration-management.md)**  
The deal registration management data model provides a framework for channel partners to establish a consistent and organized engagement model with channel partners.
-   **[Deal Registration approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/deal-registration-approvals-overview.md)**  
Enable deal agents to submit deals for approval through a configurable approval workflow built on the Advanced Approval Management framework.
-   **[Deal registration tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/deal-registration-tasks.md)**  
Create and manage tasks associated with a deal registration to organize work, track progress, and delegate deal-related activities.

**Parent Topic:**[Configure Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-partner-relationship-management.md)

**Related topics**  


[Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/partner-relationship-management.md)

[Using Partner Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-partner-relationship-management.md)

