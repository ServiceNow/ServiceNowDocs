---
title: Differences between Workplace Visitor Management versions
description: Workplace Visitor Management version 2.0.0 introduces significant architectural, data model, portal, security, and feature changes compared to earlier versions \(1.19 or earlier\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-visitor-management/visitor-mgmt-v1-v2-differences.html
release: australia
product: Workplace Visitor Management
classification: workplace-visitor-management
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 4
breadcrumb: [Reference, Workplace Visitor Management, Workplace Service Delivery, Employee Service Management]
---

# Differences between Workplace Visitor Management versions

Workplace Visitor Management version 2.0.0 introduces significant architectural, data model, portal, security, and feature changes compared to earlier versions \(1.19 or earlier\).

<table><thead><tr><th>

Workplace Visitor Management 1.19 or earlier

</th><th>

Workplace Visitor Management 2.0.0 or later

</th></tr></thead><tbody><tr><td>

Visitor identity is stored on registration records, coupling identity to a single visit.

</td><td>

Adds the `sn_wsd_visitor_user` table as a dedicated identity store, but identity is still stored on the registration record. The table enables reuse across multiple visits.

</td></tr><tr><td>

Visitor type is is a field \(**visitor\_type**\) on the `sn_wsd_visitor_vistor_registration` record.

</td><td>

Visitor type is an entity in the `sn_wsd_visitor_type` table, including a built-in Internal type for employee visitors. The **visitor\_type** field on the registration record is deprecated.

</td></tr><tr><td>

Uses the `sn_wsd_visitor_m2m_location_policy` table to link locations to policies and capture policy acceptance.

</td><td>

Policies are part of visit requirements, which can then be applied to workplace locations. For more information about creating visit requirements, see [Configure visit requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-visitor-management/configure-visit-requirements.md).

</td></tr><tr><td>

Uses the `sn_wsd_core_html_signing_template` table for badge templates. Policy signing uses only a signature-pad flow.

</td><td>

Extends the `sn_wsd_core_html_signing_template` table to support HTML-based policy signing templates in addition to badge templates.

</td></tr><tr><td>

Has no dedicated auth state table for the public visitor portal.

</td><td>

Introduces `sn_wsd_visitor_auth` to track OTP, passcode, and session state for the public visitor portal.

</td></tr><tr><td>

Uses a **location** field on visit, invitation, and registration records.

</td><td>

Adds a **workplace\_location** reference field across all affected tables. The original **location** field remains but is deprecated. Integrations that read the old field require updates.

</td></tr><tr><td>

The `sn_wsd_visitor_visit` table has a basic set of fields. The recurrence end date is stored using the internal key **endDate** in the legacy recurrence engine.

</td><td>

Extends `sn_wsd_visitor_visit` with recurring pattern fields, **workplace\_location**, draft state, and occurrence editing.Replaces the legacy recurrence engine with an rule-based engine; the internal key changes from **endDate** to **until**.

</td></tr><tr><td>

The `sn_wsd_visitor_visitor` table includes **license\_plate**, **parking\_type**, **vip**, and photo fields.

</td><td>

Removes **license\_plate** and **parking\_type** from `sn_wsd_visitor_visitor`. Adds custom-field sync to registration records.

</td></tr></tbody>
</table>|Workplace Visitor Management 1.19 or earlier|Workplace Visitor Management 2.0.0 or later|
|--------------------------------------------|-------------------------------------------|
|Has no dedicated host portal.|Introduces a host experience in the Employee Center with upcoming and past visit tabs, co-host visibility, visitor photo display, and visit or occurrence editing.|
|Has a basic receptionist view.|Delivers a redesigned receptionist portal with real-data integration, multi-select, drag-and-drop, and a condition builder for badge printing.|
|Has no public-facing visitor portal.|Introduces a public visitor portal with login, OTP authentication, and per-portal CSS branding support.|
|Has a kiosk UI with self-registration and a pre-arrival check-in flow. Several kiosk UI sections and lists are present.|Redesigns the kiosk with an additional-info page and a condition builder for badge printing. Removes the V1 kiosk UI sections and lists.|

|Workplace Visitor Management 1.19 or earlier|Workplace Visitor Management 2.0.0 or later|
|--------------------------------------------|-------------------------------------------|
|Supports recurring visits using the legacy recurrence engine.|Replaces the legacy recurrence engine with a rewritten rule-based engine, and adds occurrence-mode management.|
|Does not support draft visits.|Allows visits to be saved as drafts before submission.|
|Supports only visit creation; existing visits can't be edited.|Supports editing existing visits and individual occurrences.|
|Supports co-hosts with a co-host field and widget on visit records.|Adds a reference qualifier to the co-host field that excludes visitors. Co-host rows are displayed on the host portal.|
|Supports a pre-arrival check-in flow on the kiosk, but visitors cannot complete visit requirements through it.|Extends the pre-arrival check-in flow to allow visitors to complete visit requirements before arriving.|
|Visit cancellation cascades to related registrations but not to invitations.|Extends cancellation cascade to invitations and sends an email when an occurrence is cancelled.|

|Workplace Visitor Management 1.19 or earlier|Workplace Visitor Management 2.0.0 or later|
|--------------------------------------------|-------------------------------------------|
|Visitor notifications can be suppressed by global notification settings.|Enables **force\_delivery** on all visitor notifications so they are sent even when global notifications are turned off.|
|Emails include the location name, and parking and license plate information.|Adds the full address \(street, city, state, and zip code\) for campus and building locations to emails.|
|Renders dates and times in the recipient's time zone using a configurable format, but date and time strings are not localized.|Wraps date and time strings in `gs.getMessage()` to support localization across languages.|
|Emails include policy accept and decline buttons.|Removes policy accept and decline buttons from emails. Policy acceptance is handled through the requirements flow and signing templates.|

**Parent Topic:**[Workplace Visitor Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-visitor-management/workplace-visitor-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Visitor Management]()

[Properties installed with Workplace Visitor Management]()

[Kiosk Check-in Flow Configuration form]()

[Kiosk Check-out Flow Configuration form]()

[Kiosk Page Configuration form]()

[Kiosk Page Customizations]()

[Location Policy form]()

[New visit form]()

[Additional requirement form]()

