---
title: MDM Orchestrator rapid deployment pack
description: MDM Orchestrator, an App Engine for ERP rapid deployment pack, manages the full life cycle of master data records in your ERP system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-mdm-orchestrator.html
release: australia
topic_type: concept
last_updated: "2026-06-22"
reading_time_minutes: 2
keywords: [app, engine, erp, rapid, deployment, pack, mdm, master data]
breadcrumb: [Explore, App Engine for ERP rapid deployment packs, Building low-code applications, Developing your application, Building applications]
---

# MDM Orchestrator rapid deployment pack

MDM Orchestrator, an App Engine for ERP rapid deployment pack, manages the full life cycle of master data records in your ERP system.

## MDM Orchestrator capabilities

MDM Orchestrator manages the steps before and after a master data management record is created in your ERP system. It covers the full range of record operations, such as create, update, deactivate, activate, and bulk upload across multiple business domains.

Integration with the target ERP system requires either Integration Hub spokes or Zero Copy Connector for ERP.

## Key benefits

MDM Orchestrator provides the following benefits:

-   Reduces duplicate records through two levels of deduplication \(exact match and fuzzy match\) applied automatically before a record reaches the approval stage.
-   Converts existing data governance policy documents into configurable business rules within the orchestration, reducing manual governance overhead.
-   Applies domain-aware validation, checking that records include the correct field values for the domain, such as country codes and currency codes.
-   Routes records automatically to the appropriate person at each stage.

## MDM Orchestrator workflow

The generic workflow proceeds through the following stages:

-   A human requestor submits a new master data record request, selecting a domain and request type. Role-based access control \(RBAC\) restricts the domains and request types available to each user.
-   The Accuracy Report Agent assesses the new request using historical trends and generates a risk report.
-   The Knowledge to Execution Agent searches your knowledge base for applicable business rules and checks whether the record meets the criteria for auto-approval. Records that meet the criteria proceed without manual approval. Others are routed to a business approver.
-   The Deduplication Agent checks the record against existing records in the system of truth, flagging potential duplicates for review.
-   A human reviewer reads the record details and AI-generated accuracy reports and decides on enrichment and governance approval.
-   The record moves to Approval Hub, where a human approver reviews it alongside all other pending approvals. The Conversational Agent is available to provide additional context about a pending request before the approver acts.
-   After approval, MDM Orchestrator passes the record to your ERP integration layer, such as Integration Hub spokes or Zero Copy Connector for ERP, for creation in the target ERP system. MDM Orchestrator does not write directly to the ERP system.

\[Omitted image "aes-erp-rdp-mdm-orchestrator-flow-infographic.png"\] Alt text: Diagram of the MDM Orchestrator workflow, from request submission through ERP integration. See the surrounding text for a description of each stage.

## Supported domains

Domains are configurable. You can add or remove domains to match your organization's requirements.

MDM Orchestrator supports the following domains:

-   Customer
-   Business Partner
-   Material
-   Bill of Materials
-   Location
-   Cost Center

**Parent Topic:**[Exploring App Engine for ERP rapid deployment packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-explore.md)

