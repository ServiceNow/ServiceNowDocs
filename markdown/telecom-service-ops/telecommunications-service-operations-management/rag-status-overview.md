---
title: Mobile private network health status
description: The health status feature provides a quick indicator of radio and core server component health collected from a mobile private network \(MPN\). The system classifies each component using a configurable rule set and assigns error codes that identify specific detected conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/rag-status-overview.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [health status, MPN, Telecom Visibility]
breadcrumb: [Fault Management: Events and alerts, Telecom Assurance, Explore, Telecommunications Service Operations Management]
---

# Mobile private network health status

The health status feature provides a quick indicator of radio and core server component health collected from a mobile private network \(MPN\). The system classifies each component using a configurable rule set and assigns error codes that identify specific detected conditions.

## How health status is calculated

Each collected component is checked against a set of rules and assigned one of the following statuses:

-   **Red:** The component reports a condition that indicates a critical issue, such as an alarm status of major or critical, or the component is not reachable.
-   **Amber:** The component reports a condition that indicates a degraded but non-critical issue, such as a minor alarm or an indeterminate status.
-   **Green:** The component reports normal operating conditions across all evaluated fields.
-   **Unknown:** The component's status can't be determined from the available data.

The system checks the rules in a fixed priority order: red conditions first, then amber, then green. A component is marked green only when every green condition matches; if no rule matches at all, the status is unknown.

Rules are currently defined for two component types: radio and core server.

## Rule configuration

The active rule set is stored as a versioned system property, so you can trace which rule version produced a given status. The system provides a default rule set and supports an administrator-editable override.

The system uses the override when one is provided. If the override is empty or contains invalid data, the system automatically falls back to the default rule set so that health status calculation does not stop.

The rule set supports multiple vendors, each with its own component types and evaluation logic. Currently, only the Nokia rule set is implemented.

