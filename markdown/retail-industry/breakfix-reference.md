---
title: Components for Break-Fix
description: Technical reference for Break-Fix case states, available actions, critical fields, tables, and data relationships.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/breakfix-reference.html
release: australia
topic_type: reference
last_updated: "2026-07-23"
reading_time_minutes: 3
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components for Break-Fix

Technical reference for Break-Fix case states, available actions, critical fields, tables, and data relationships.

## Case States and Available Actions

|**State**|**Description**|**Available Actions**|
|---------|---------------|---------------------|
|New|Case just created by requestor. Awaiting HQ triage.|Requestor: Close \(cancel case\)|
|In Progress|HQ agent reviewing and working on resolution.|Requestor: None \(read-only\). HQ Agent: Resolve|
|Resolution Proposed|HQ agent has proposed resolution.|Requestor: Accept or Reject. HQ Agent: Modify resolution|
|Closed|Case resolved or rejected. Complete.|View history only|

## Key Tables and Relationships

|**Table**|**Description**|
|---------|---------------|
|Break-Fix Case|Extends CSM Case. Represents equipment failure report. Contains: requestor, equipment, store, priority, state, resolution info.|
|Service Incident|Linked for IT issues. Pre-populated with case details. Requires the sn\_incident\_write role assigned to the Break-fix agent. State changes and comments are added as work notes on the case.|
|Work Order|Linked for hardware issues. Assigned to field technicians. Pre-populated with case details. State changes and comments are added as work notes on the case.|
|Install Base|**CRITICAL:** Registry of installed equipment. Key field: Buyer Organization \(Service Organization\). Equipment filtered by this relationship.|
|Service Organization|Represents store/location. Equipment registered with organization as buyer.|

**Key Relationships:**

-   **Install Base → Buyer Organization:** FILTERS equipment dropdown to user's store. Only equipment where buyer org = user's service org appears selectable.
-   **Break-Fix Case → Incident:** One-to-One link for IT issues. State changes and comments are added as work notes on the case.
-   **Break-Fix Case → Work Order:** One-to-One link for hardware issues. State changes and comments are added as work notes on the case.
-   **Break-Fix Case → Install Base:** Reference to track which equipment failed.

## Critical Fields

-   **Install Base Buyer Organization**

    KEY FILTERING MECHANISM. Field on Install Base table. Determines which equipment users can select. Only equipment where buyer organization matches user's current service organization appears in the case form's Affected device \(Install base\) dropdown.

-   **Service Organization**

    Represents the store. Auto-populated in case form from user's service organization. Cannot be changed by store-level users.

-   **Service Issue Type**

    Hardware or IT. Mandatory before HQ proposes resolution. Hardware enables work order creation. IT enables incident creation.

-   **Case State**

    New \| In Progress \| Resolution Proposed \| Closed. Determines available actions for requestors and HQ agents.


## Role-Based Permissions

-   **BREAKFIX\_AGENT**

    Base role for HQ Support Agents. Grants queue access, case triage capabilities, and resolution proposal actions, including creating work orders when the FSM integration plugin is installed.

-   **sn\_incident\_write**

    Required by the Break-fix agent to create a linked incident.

-   **sn\_incident\_read**

    Required by the store associate, manager, or regional manager to view a linked incident.

-   **WM\_INITIATOR \(Conditional\)**

    Enables work order creation. The Create Work Order button appears only if the FSM integration plugin is installed.


## Typical Case Data Flow

1.  Requestor creates case in "New" state with auto-populated store and filtered equipment
2.  Case routed to HQ queue
3.  HQ agent picks up case and selects Service Issue Type
4.  HQ agent creates Incident \(IT\) or Work Order \(hardware\) or documents troubleshooting steps
5.  HQ agent clicks Propose Solution → case state = "Resolution Proposed"
6.  State changes and comments from the Incident/Work Order are added as work notes on the case
7.  Requestor receives notification and reviews proposed resolution
8.  Requestor accepts \(closes case\), rejects \(reopens to HQ\), or self-closes
9.  Case state = "Closed" \(accepted/self-closed\) or "New" \(rejected, reopens to HQ\)

**Parent Topic:**[Components installed with plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-components-installed-with-plugins.md)

**Related topics**  


[Break-Fix Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-overview.md)

[Resolve Cases in Workspace through HQ Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-resolve-workspace.md)

[Submit Break-Fix Cases through Portal or Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-submit-case.md)

[Respond to resolutions through Portal or Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-respond-resolution.md)

