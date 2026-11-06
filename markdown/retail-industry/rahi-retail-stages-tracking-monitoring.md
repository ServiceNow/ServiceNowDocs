---
title: Stages of store plan tracking and monitoring
description: A store plan moves through distinct phases, each supported by specific screens and interactions. Tracking activates from the point of publication onward.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/retail-industry/rahi-retail-stages-tracking-monitoring.html
release: australia
topic_type: concept
last_updated: "2026-10-07"
reading_time_minutes: 1
breadcrumb: [Retail store plans tracking, Retail store plans, Explore, Retail]
---

# Stages of store plan tracking and monitoring

A store plan moves through distinct phases, each supported by specific screens and interactions. Tracking activates from the point of publication onward.

1.  Plan authoring - An HQ operations manager or regional manager \(for HQ communications plans\), or an audit manager or location audit manager \(for store audit plans\), creates a store plan that defines the plan type, tasks to be completed, store locations to assign, and a schedule \(immediate, one-time, or recurring\). This phase exists entirely in the Store Plan Authoring capability released in March 2026. Execution Tracking does not begin here.
2.  Plan publication and case generation - Once the plan is published, the system generates parent HQ cases and child store cases \(audit cases and audit tasks for a store audit plan\) according to the schedule. Each store assignment produces one store case containing the relevant tasks. For an immediate plan, records are generated when the plan is published. For one-time and recurring plans, records are generated when the schedule runs. For a plan that runs on a recurring schedule, each occurrence produces its own set of cases and tasks, and tracking is always scoped to one occurrence at a time.
3.  Plan progress review - The Track Plan tab on the published plan provides an overall completion summary for the selected occurrence. This allows an HQ operations manager to view the proportion of store cases that are closed, open, or overdue, along with the total number of store cases, without having to open individual records. Selecting a count moves straight to the matching records.
4.  Store-level execution - Regional managers access the store case list for their region, drill into specific store cases, and review the tasks being worked. They can monitor task-level status, reassign work, or flag blockers. This is the primary execution layer — where stores actually complete the plan.

**Parent Topic:**[Retail store plans tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-explore-store-plans-tracking.md)

