---
title: Configure exception reason properties
description: When real-time enforcement, enforce\_real\_time\_validation, is enabled, exception reasons can be configured for Suggest, Review, Recommend, and Act level findings based on the exception reason scope. Settings determine which finding levels require approval before the form can be saved.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/exception-reason-properties.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure Scan Engine parameters, Activate Scan Engine and review settings, Impact Guided Setup, Configuring Impact, Impact]
---

# Configure exception reason properties

When real-time enforcement, `enforce_real_time_validation`, is enabled, exception reasons can be configured for Suggest, Review, Recommend, and Act level findings based on the exception reason scope. Settings determine which finding levels require approval before the form can be saved.

## Before you begin

Role required: sn\_se.scan\_engine\_admin, sn\_se.scan\_engine\_read\_user, or sn\_se.internal\_rest\_integration

## About this task

## Procedure

1.  Navigate to **All** &gt; **** &gt; **Impact** &gt; **Scan Engine Properties** and select the **Exception Reason** tab

2.  Configure the following settings to control exception reason behavior.

<table><thead><tr><th>

Field

</th><th>

Description

</th><th>

Values

</th></tr></thead><tbody><tr><td>

Exception reason scope

</td><td>

Determines which finding levels \(Suggest, Review, Recommend, or Act\) can have exception reasons submitted and approved. Choose the scope that matches your organization's exception workflow requirements.

</td><td>

-   **Recommend only** - Exception reasons can only be submitted for Recommend level findings.
-   **Act and Recommend** - Exception reasons can be submitted for both Act and Recommend level findings.
-   **All levels** - Exception reasons can be submitted for Suggest, Review, Recommend, and Act level findings.


</td></tr><tr><td>

Enforce rejected exception reason validations

</td><td>

-   When enabled and an exception reason is rejected, the object linked to that reason is set to read-only.
-   Users can't make additional changes until the finding message is resolved or a new exception reason is submitted.
-   This confirms strict conformance with validation rules and prevents inconsistent or unauthorized updates while an exception is unresolved.


</td><td>

Selected or cleared

</td></tr><tr><td>

Enable approvals in production \(**enable\_exception\_reason\_approvals\_in\_production**\)

</td><td>

-   Controls whether exceptions can be approved in production instances or only in development environments.
-   When disabled, exceptions can only be approved in the instances in which they are raised.
-   This setting is only applicable to development instances.


</td><td>

Selected or cleared

</td></tr><tr><td>

Approval group\(s\)

</td><td>

The group or groups that approve or reject exception reasons and receive notifications when new approvals are requested.

</td><td>

Select one or more approval groups

</td></tr><tr><td>

Exclude approved exception reasons from technical debt

</td><td>

When enabled, findings with approved exception reasons are excluded from technical debt metrics. This does not remove the finding from the system.

</td><td>

Selected or cleared

</td></tr><tr><td>

Upon new finding found \(**er\_finding\_number\_validation**\)

</td><td>

Determines how exception reasons are handled when the same issue is detected again in a subsequent scan.

</td><td>

-   **Auto Accept Existing Reason**
-   **Re-approve Existing Reason**


</td></tr><tr><td>

Upon line number change \(**exception\_reason\_validation**\)

</td><td>

Determines how approved exception reasons are handled when the finding's line number changes in the code.

</td><td>

-   **Auto Accept Existing Reason** \(default\)
-   **Re-approve Existing Reason**


</td></tr></tbody>
</table>
-   **[Configure exception approval behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-exception-reasons-scan-engine.md)**  
Configure how exception reasons are enforced, approved, and re-evaluated when findings are detected using the Scan Engine. Settings control exception behavior.

**Parent Topic:**[Configure Scan Engine parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-scan-engine-properties.md)

