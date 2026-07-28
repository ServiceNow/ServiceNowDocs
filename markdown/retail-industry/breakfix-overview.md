---
title: Break-Fix Case Management
description: Break-Fix Case Management enables store staff to report and resolve hardware and IT failures through a structured workflow involving requestors, HQ support agents, and field service technicians.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/breakfix-overview.html
release: australia
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 3
breadcrumb: [Explore, Retail]
---

# Break-Fix Case Management

Break-Fix Case Management enables store staff to report and resolve hardware and IT failures through a structured workflow involving requestors, HQ support agents, and field service technicians.

## Break-Fix Case Management overview

Break-Fix Case Management provides an end-to-end solution for managing equipment failures across store locations. Store staff submit cases for failed equipment \(POS terminals, printers, scanners, etc.\), HQ support agents diagnose and propose resolutions, and requestors accept or reject the proposed solutions.

## Three-Stage Workflow

1.  **Request Submission \(Portal/Mobile\):** Store Manager, Store Associate, or Regional Manager submits case. Requesting store is auto-populated. Equipment is filtered by Install Base buyer organization.
2.  **HQ Resolution \(Workspace\):** HQ Support Agent reviews case, selects service issue type, and proposes resolution \(troubleshooting, incident, or work order\).
3.  **Requestor Response \(Portal/Mobile\):** Original requestor reviews proposed resolution and accepts, rejects with reason, or self-closes.

## Key Characteristics

-   **Auto-Population:** Requesting store automatically filled from user's service organization. Store-level users cannot change.
-   **Equipment Filtering:** Equipment dropdown filtered by Install Base buyer organization. Only equipment registered to user's store appears.
-   **State-Dependent Actions:** Available actions depend on case state. Close only in New state. Accept/Reject only in Resolution Proposed state.
-   **Work Notes Reflect Linked Record Activity:** State changes and comments from a linked incident or work order are added as work notes on the break-fix case.
-   **Role-Based Permissions:** BREAKFIX\_AGENT \(base\) with sn\_incident\_write role for incident creation. sn\_incident\_read role for store associate, manager, or regional manager to view the incident.

## Personas and Responsibilities

-   **Store Manager / Store Associate**

    Submit cases via portal or mobile. Accept, reject, or self-close resolutions.

-   **Regional Manager / Area Manager**

    Submit cases on behalf of managed stores. Accept, reject, or self-close resolutions.

-   **HQ Support Agent**

    Resolve cases in workspace. Propose solutions via troubleshooting, incidents, or work orders.


## Case State Progression

-   **New:** Case created. Requestor can Close.
-   **In Progress:** HQ processing. Requestor has no actions \(read-only\).
-   **Resolution Proposed:** HQ proposed solution. Requestor can Accept or Reject.
-   **Closed:** Resolved. History only.

## Critical Data Relationship

**Install Base Buyer Organization:** Equipment is filtered based on the Install Base buyer organization field. Only equipment where buyer organization matches the user's current service organization appears in the equipment dropdown. This ensures store staff can only select equipment registered to their store.

## Three Resolution Methods

-   **Troubleshooting Steps**

    HQ documents instructions or KB references. For issues resolvable by store staff.

-   **Service Incident**

    HQ creates a linked incident for IT issues. Requires the sn\_incident\_write role, assigned to the Break-fix agent, to create the incident; the sn\_incident\_read role lets the store associate, manager, or regional manager view the incident. State changes and comments from the incident are added as work notes on the case.

-   **Work Order**

    HQ creates a linked work order for hardware issues. State changes and comments from the work order are added as work notes on the case.


## Related Tasks

-   [Submit Break-Fix Cases \(Portal and Mobile\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-submit-case.md)
-   [Resolve Cases in Workspace \(HQ Agents\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-resolve-workspace.md)
-   [Respond to Resolutions \(Portal and Mobile\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-respond-resolution.md)
-   [Break-Fix Reference: States, Fields, and Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/breakfix-reference.md)

**Parent Topic:**[Exploring Retail](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-operations-explore.md)

