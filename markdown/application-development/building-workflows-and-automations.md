---
title: Building workflows and automations
description: Workflows and automation let your app take action automatically in response to events, record changes, or schedules. Rather than relying on users to manually move work forward, you define the logic once and let the platform execute it consistently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/building-workflows-and-automations.html
release: australia
topic_type: concept
last_updated: "2026-07-02"
reading_time_minutes: 1
breadcrumb: [Build your first app, Standard app development, Getting Started guide for developers, Building applications]
---

# Building workflows and automations

Workflows and automation let your app take action automatically in response to events, record changes, or schedules. Rather than relying on users to manually move work forward, you define the logic once and let the platform execute it consistently.

## How do flows work?

In ServiceNow app development, the primary tool for building automation is Workflow Studio, a low-code environment where you assemble workflows visually using triggers, conditions, and actions.

Triggers define what starts a workflow. A trigger fires when a specific event occurs, and the flow begins executing from that point. Common trigger types include:

-   Record-based: Fires when a record is created, updated, or deleted on a specific table
-   Scheduled: Fires at a defined time or recurring interval, useful for maintenance tasks or report generation
-   Inbound email: Fires when an email matching certain criteria arrives
-   Application: Fires based on custom events your app defines

Actions are the individual steps a flow performs after it is triggered. Each action represents a discrete operation, such as creating a record, sending a notification, calling an external API, or updating a field value. Workflow Studio provides a library of pre-built actions you can configure without writing code, so you can automate common operations quickly. For logic that requires more complexity, you can call a script include from within a flow action to keep your custom code centralized and reusable.

Subflows are reusable workflow components that you build once and call from multiple flows. They work similarly to script includes for business logic: if several workflows share a common sequence of steps, you define that sequence as a subflow and reference it wherever it is needed. This keeps your automation maintainable as your app grows, because changes to shared logic only must be made in one place.

Workflow Studio is the recommended approach for new ServiceNow development. For low-code app development, building automation in Workflow Studio helps ensure your app uses current platform patterns and benefits from ongoing improvements to the tooling.

**Parent Topic:**[Build your first application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-your-first-app.md)

