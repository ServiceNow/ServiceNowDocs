---
title: Field Service for Audit
description: Field Service for Audit is a horizontal ServiceNow scoped app that provides a shared audit-task data model and a pluggable access-control framework so consuming apps can build audit experiences without duplicating infrastructure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/fsm-audit-overview.html
release: australia
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 2
breadcrumb: [Retail Store Audit Operations, Explore, Retail]
---

# Field Service for Audit

Field Service for Audit is a horizontal ServiceNow scoped app that provides a shared audit-task data model and a pluggable access-control framework so consuming apps can build audit experiences without duplicating infrastructure.

## Overview

Field Service for Audit \(`sn_fsm_audit`\) is a horizontal infrastructure app that every consuming app — both ServiceNow-shipped vertical apps and customer-built customizations — can rely on for a single, consistent audit-task record shape and a single, shared access-control framework.

Before this app existed, each consuming team that needed audit work built its own task structure and its own access rules. That pattern caused data-shape drift between deployments, forced this app into the release cycle for every consumer access change, and made cross-deployment reporting unreliable.

## What Field Service for Audit provides

-   **A shared audit-task data model** — one table, `wm_audit_task`, specializes the platform work-management task type \(`wm_task`\) so all assignment, scheduling, state, and fulfillment data is inherited from the platform.
-   **A pluggable access-control framework** — consuming apps register their own access rules in their own scope and on their own release cadence. This app ships unchanged when a consumer changes its access logic.
-   **Permissive default access** — FSM-only deployments with no consuming app registered fall back to role-based default-allow behavior, so the app works out of the box.

**Important:** This app ships no user-facing UI. All workspace pages, portal surfaces, mobile screens, form layouts, and UI actions for audit work belong to consuming apps.

## Key concepts

|Concept|Description|
|-------|-----------|
|Audit task|A specialized work-management task \(`wm_audit_task`\) representing a discrete piece of audit work, with a pass/fail result field and all inherited `wm_task` fields.|
|Extension point|A ServiceNow platform scripted extension point that consuming apps implement to plug their own access rules into this app without modifying it.|
|Consumer|Any ServiceNow scoped app \(vertical or custom\) that creates audit tasks, registers access rules, or grants users audit roles.|
|Default-allow|The fallback behavior when no registered consumer extension applies — read and write access is granted based on role alone.|
|Horizontal app|An infrastructure app with no end-user UI of its own, designed to be consumed by multiple vertical or custom apps.|

**Parent Topic:**[Retail Store Audit Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-store-audit-overview.md)

**Related topics**  


[Audit tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[How access to audit tasks works](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)

[Components installed with Field Service for Audit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/fsm-audit-reference.md)

