---
title: Retail Store Audit Operations
description: Retail Store Audit Operations is a ServiceNow scoped application that automates the creation, assignment, and fulfillment of retail store audit cases and tasks, enabling Plan Authors to publish structured audit plans that generate work for field Auditors across selected store locations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-store-audit-overview.html
release: australia
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 5
keywords: [store audit, retail audit, audit plan, store audit case, audit operations]
breadcrumb: [Explore, Retail]
---

# Retail Store Audit Operations

Retail Store Audit Operations is a ServiceNow scoped application that automates the creation, assignment, and fulfillment of retail store audit cases and tasks, enabling Plan Authors to publish structured audit plans that generate work for field Auditors across selected store locations.

The Retail Store Audit Operations application \(scope ID: `sn_rtl_store_audit`\) enables structured, repeatable store audit programs on the ServiceNow platform. It runs on the CSM/FSM Next Experience Workspace and integrates natively with Task Plan Templates, Work Management \(FSM\), and Retail Core.

## Problem this application solves

Before this application, retail store audits were managed through ad hoc spreadsheets, emails, and disconnected task lists with no central system of record, no standardised plan structure, and no automated assignment to field auditors.

This application delivers a standardised, automated workflow where:

-   Audit plans are authored against pre-configured templates.
-   Store selection is part of plan authoring.
-   Case and task generation is fully automated on plan publication.
-   Auditors receive assignments through rules-based routing.
-   All audit activity—assignments, observations, and closures—is tracked on a single platform.

## How Retail Store Audit Operations works

1.  **Plan authoring**: A Plan Author uses the **Store audit** playbook—launched automatically from the CSM/FSM Workspace Record Generator—to configure audit template items, select store locations, set a schedule, and review the plan.
2.  **Plan publication**: The Plan Author publishes the plan. Publication makes it available for generation but does not create records automatically.
3.  **Case and task generation**: The Plan Author clicks **Generate Cases/Tasks**. The platform creates one Store Audit Case per selected Retail Organization and one or more Audit Tasks per case.
4.  **Assignment**: Platform-native assignment rules automatically route cases and tasks to Auditors. Store Audit Managers can override assignments.
5.  **Fulfillment**: Auditors work cases in CSM/FSM Workspace, record observations in work notes and comments, and progress cases through New → Open → Closed.

## Key design decisions

-   **Generation is separated from publication**

    Publishing makes a plan available. The Plan Author must explicitly click **Generate Cases/Tasks** to commit to record creation, allowing review of the plan before any cases exist.

-   **No custom fields in V1**

    Both the Store Audit Case \(`sn_rtl_store_audit_case`\) and the Audit Task \(`wm_audit_task`\) use only inherited fields from their parent tables. No custom columns are added.

-   **No parent Audit Case in V1**

    The Store Audit Case is the top-level record. A parent-level Audit Case can be introduced later if a use case for HQ- or region-level follow-up is identified.

-   **HQ Auditors use CSM/FSM Workspace exclusively**

    The `sn_rtl_store_audit.auditor` role fulfils exclusively via CSM/FSM Workspace. Retail Mobile is available for Location Auditors \(`sn_rtl_store_audit.location_auditor`\).


## Workspace experience

Auditors and Store Audit Managers access their work from the CSM/FSM Next Experience Workspace. All customisations use standard platform artifacts—the workspace shell is not modified.

-   **Store Audit Case form**: Three sections—2-column main \(case metadata\), Notes \(work notes, activity stream, comments\), and Closure Information. The action bar suppresses all inherited out-of-the-box UI Actions; only a custom **Save** button is present \(hidden when the case is Closed\).
-   **Audit Task form**: 2-column header and Notes sections, with an Overview pane showing Priority and State pills. Priority is colour-coded: Critical \(red\), High \(orange\), Moderate \(yellow\), Low \(green\), Planning \(grey\). The **Close Complete** button appears in the action bar when the task is in an active state and assigned.
-   **Related-list tabs**: **Audit tasks** on the Store Audit Case page, **Track plan** on the plan template page, and **Questionnaire** on the Audit Task page.
-   **List views**: **New** and **Add** buttons are suppressed everywhere—records are created only through the playbook or generation flow.

**Note:** Users with the `plan_author` role see every field except **Comments** as read-only on in-flight Store Audit Cases.

## Prerequisites

The following must be installed and active on the ServiceNow instance \(Xanadu or later\):

-   Task Plan Templates application
-   Retail Core \(`sn_retail`\)
-   Work Management \(FSM\)
-   CSM/FSM Workspace

**Note:** Retail Organization records for all stores to be audited must exist on the instance before plan authoring begins.

-   **[Data model and case generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-generation-flow.md)**  
Retail Store Audit Operations uses two record types—Store Audit Case and Audit Task—and generates them in a deliberate two-step flow: a Plan Author publishes an audit plan and then explicitly triggers generation, which creates one Store Audit Case per selected Retail Organization and one or more Audit Tasks per case.
-   **[Audit plan and playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-plan-playbook.md)**  
An audit plan defines what is audited, at which store locations, and when. Plan Authors create and configure audit plans through the **Store audit** playbook, which launches automatically from the CSM/FSM Workspace Record Generator.
-   **[Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-overview.md)**  
Field Service for Audit is a horizontal ServiceNow scoped app that provides a shared audit-task data model and a pluggable access-control framework so consuming apps can build audit experiences without duplicating infrastructure.
-   **[Audit tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-tasks.md)**  
The `wm_audit_task` table is a specialized work-management task that represents a single audit work item. It inherits all scheduling, assignment, state, and fulfillment behavior from the platform `wm_task` type and adds an audit-specific result field.
-   **[How access to audit tasks works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-access-control.md)**  
Field Service for Audit uses a layered access-control framework: platform ACLs enforce role-based deny-first rules, and a scripted extension point delegates fine-grained read/write decisions to consuming apps, with a permissive default when no consumer rule applies.
-   **[Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-roles.md)**  
Field Service for Audit defines three roles that map to three personas — Author, Auditor, and Audit Admin — each with a distinct set of permissions on the `wm_audit_task` table.
-   **[Custom access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-custom-access-rules.md)**  
The access-control extension point is the mechanism consuming apps use to register their own read and write access rules for audit tasks without modifying Field Service for Audit. Each consuming app implements the contract in its own scope on its own release cadence, and multiple consumers coexist through a deterministic first-match-wins evaluation order.

**Parent Topic:**[Exploring Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-operations-explore.md)

**Related topics**  


[Audit plan and playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-plan-playbook.md)

[Data model and case generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-generation-flow.md)

[Components installed with Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-reference.md)

