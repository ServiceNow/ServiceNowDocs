---
title: Change Management release notes
description: The ServiceNow Change Management application provides a systematic approach to control the life cycle of all changes, facilitating beneficial changes to be made with minimum disruption to IT services. See the following sections for release notes by version.The Brazil Early Availability release introduces compliance dynamic schema, change lockdown, lockdown conflict detection, and scaled change for Change Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/change-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Change Management release notes

The ServiceNow® Change Management application provides a systematic approach to control the life cycle of all changes, facilitating beneficial changes to be made with minimum disruption to IT services. See the following sections for release notes by version.

## About Change Management

-   Control the full change lifecycle from request to closure using a structured workflow that reduces IT service disruption.
-   Define change models using custom state models, state transitions, and transition conditions. Out-of-the box change models include ITIL change models for Standard, Normal, or Emergency changes with dedicated approval paths.
-   Use machine learning to assess change risk and suggest standard change templates.
-   Run agentic AI workflows through a conversational interface. Use it to plan changes, assess conflicts, assess change quality, schedule changes, suggest configuration items, create outages, and generate standard change template proposals.
-   Track team performance with the Change Success Score, which uses historical data to predict successful change completion. This feature requires an ITSM Professional subscription.

See [Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/c_ITILChangeManagement.md) for more information.

## Activation and other requirements

-   **Activation information**

    Change Management is a ServiceNow AI Platform feature that is active by default. The Change Management plugins listed are activated by default.


## Accessibility and localization

-   **Accessibility information**

    Reflow support for the Create a change request page: Content can be zoomed up to 400% through your browser settings, with page layouts automatically transforming into a vertical, stacked view without loss of content or functionality. This enhancement helps users with low vision or who have trouble seeing web content due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-service-management-rn-landing.md)

## Brazil Early Availability

The Brazil Early Availability release introduces compliance dynamic schema, change lockdown, lockdown conflict detection, and scaled change for Change Management.

### What's new

-   **[Compliance dynamic schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/compliance-dynamic-schema.md)**

    Store risk and compliance details on change requests without adding columns to the Change Request table. Compliance dynamic schema saves these details as name and value pairs in a single field using the platform Dynamic Schema feature. Regulated industries can capture information such as whether a change handles personal data, whether an audit trail is required, and how long a rollback takes. The base system includes example dynamic categories such as Risk and Compliance, Financial Risk and Compliance, and SaaS/Cloud Security Compliance, and example attributes covering areas such as audit trail, downtime, estimated impacted users, lead time, rollback time, and compliance. You can deactivate the examples and define categories and attributes that match your organization's compliance requirements. You can also read and update attribute values from scripts, including risk condition scripts and business rules, using the dynamic schema scripting API.

-   **[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-lockdown.md)**

    Change lockdown allows change managers to pause all or a subset of in-flight change requests. Use it during major unplanned IT, critical, or financial events.

-   **[Change lockdown conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/lockdown-conflict-detection.md)**

    Automatically flag change requests that overlap an active lockdown period. Conflict detection runs alongside maintenance window and blackout window checks. Any change request inside a lockdown is marked as an Inside Change Lockdown conflict and placed on hold. Reschedule it outside the lockdown period to clear the conflict and continue processing.

-   **[Scaled change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/scaled-change-overview.md)**

    Scaled Change extends change management to complex environments with many configuration items. A single Scaled Change generates and coordinates child change records for every affected configuration item. It uses scheduling intelligence, conflict detection, and approval workflows to keep large-scale changes on track from planning through closure.

-   **[ITIL change process assignment for change models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itil_change_process_models.md)**

    Assign an ITIL change process to a change model so the ChangeRequest API uses that model when it creates a matching change request.


