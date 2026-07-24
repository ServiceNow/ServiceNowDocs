---
title: Audit Management release notes
description: The ServiceNow Audit Management application supports activities related to planning audit engagements, executing engagements, and reporting findings to an audit committee. Audit Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-31"
reading_time_minutes: 1
---

# Audit Management release notes

The ServiceNow® Audit Management application supports activities related to planning audit engagements, executing engagements, and reporting findings to an audit committee. Audit Management was enhanced and updated in the Australia release.

## Audit Management highlights for the Australia release

-   Improve audit data governance by introducing an audit entry framework that separates audit-specific \(third-line\) records from operational \(second-line\) records with controlled visibility.

See [Audit Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/c_GRCAudits.md) for more information.

**Important:** Audit Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Audit entry fields on GRC objects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-entry-overview.md)**

    Classify the following GRC objects as third-line audit records using the new audit entry option:

    -   Entity
    -   Engagement
    -   Control objective
    -   Control
    -   Risk statement
    -   Risk
    Control visibility with role-based access so that only users with the sn\_audit\_ws.third\_line\_manager role can view audit entry \(third-line\) records. The **Audit entry** option is selected by default when the third-line manager creates a record and is set to read-only after the record is saved.

    **Note:** An administrator must manually assign the sn\_audit\_ws.third\_line\_manager role to a user to use this feature.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

