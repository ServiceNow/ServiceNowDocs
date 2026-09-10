---
title: Exploring App Engine ERP Rapid Deployment Packs
description: App Engine ERP Rapid Deployment Packs provide a system of action on top of ERP systems. Available packs manage master data records, centralize business approvals, and complete month-end financial tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/aes-erp-rdp-explore.html
release: australia
topic_type: concept
last_updated: "2026-08-13"
reading_time_minutes: 3
keywords: [app, engine, sap, erp, rapid, deployment, pack, master data management, MDM, agentic, manufactur, operation, template, templatized, business, workflow, approve, approval, month-end close, month end close, month, end, close]
breadcrumb: [App Engine ERP Rapid Deployment Packs, Building low-code applications, Developing your application, Building applications]
---

# Exploring App Engine ERP Rapid Deployment Packs

App Engine ERP Rapid Deployment Packs provide a system of action on top of ERP systems. Available packs manage master data records, centralize business approvals, and complete month-end financial tasks.

## Workflow overview

App Engine ERP Rapid Deployment Packs are used on top of ERP systems such as SAP. Rapid deployment packs extend the capability of ERP systems by providing agentic workflow templates that you can deploy immediately and tailor to your needs.

Each rapid deployment pack includes AI agents embedded in the workflow. When a business process requires human involvement, such as enrichment, review, or approval, the workflow routes to the appropriate person automatically. After the human action is complete, the workflow continues to its next stage.

Rapid deployment packs send completed records to your existing integration layer. The scope of each rapid deployment pack ends at that point. The integration layer, such as Integration Hub spokes or Zero Copy Connector for ERP, carries the records to the target ERP system.

**Note:** Only users with App Engine Prime can download the App Engine ERP Rapid Deployment Packs from the ServiceNow Store.

## Available rapid deployment packs

The following rapid deployment packs are available:

-   MDM Orchestrator: Manages the full life cycle of master data records, including create, update, deactivate, activate, and bulk upload. For more information, see [MDM Orchestrator Rapid Deployment Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-mdm-orchestrator.md).
-   Approval Hub: Centralizes all ERP-based business approvals, including transactions, work orders, production orders, master data records, and month-end journal entries, into a single interface. For more information, see [Approval Hub Rapid Deployment Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-approval-hub.md).
-   Manual Journal Entry Posting: Orchestrates the tasks and posting mechanisms involved in month-end book corrections and financial reconciliation. For more information, see [Journal Entry Portal Rapid Deployment Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-journal-entry.md).

## Rapid deployment pack personas

Different users need different forms, permissions, and approval chains. Rapid deployment packs define core personas that move a request from creation to completion:

-   Requestors create requests for the domains assigned to them.
-   Enrichers add supplementary data from third-party or internal sources.
-   Governance users perform compliance and governance checks.
-   Approvers review prepared requests and approve or reject them in Approval Hub.

For more information and examples, see [App Engine ERP Rapid Deployment Packs user personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-user-personas.md).

-   **[MDM Orchestrator Rapid Deployment Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-mdm-orchestrator.md)**  
MDM Orchestrator, an App Engine ERP Rapid Deployment Pack, manages the full life cycle of master data records in your ERP system.
-   **[Approval Hub Rapid Deployment Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-approval-hub.md)**  
Approval Hub is the centralized interface where requests from MDM Orchestrator and journal entries converge for business approval. Approvers have one view of all pending actions, regardless of the originating rapid deployment pack.
-   **[Manual Journal Entry Posting Rapid Deployment Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-journal-entry.md)**  
The Manual Journal Entry Posting App Engine ERP Rapid Deployment Pack, helps you create, validate, and submit journal entries for month-end account closing.

**Parent Topic:**[App Engine ERP Rapid Deployment Packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/aes-erp-rdp-overview.md)

