---
title: Configure exception reason properties
description: When real-time enforcement, enforce\_real\_time\_validation, is enabled, exception reasons can be configured for Suggest, Review, Recommend, and Act level findings based on the exception reason scope. The scope controls which finding levels can have exceptions. It doesn't decide which findings block a save.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/exception-reason-properties.html
release: australia
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 3
breadcrumb: [Configure Scan Engine properties, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Configure exception reason properties

When real-time enforcement, `enforce_real_time_validation`, is enabled, exception reasons can be configured for Suggest, Review, Recommend, and Act level findings based on the exception reason scope. The scope controls which finding levels can have exceptions. It doesn't decide which findings block a save.

## Before you begin

Role required: sn\_se.scan\_engine\_admin, sn\_se.scan\_engine\_read\_user, or sn\_se.internal\_rest\_integration

## About this task

This topic is the reference for each exception reason setting and its values. For an overview of exception reasons and the approval lifecycle, see [Exception handling in Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/exception-handling-overview.md). For setting the options in order, see [Configure exception approval behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-exception-reasons-scan-engine.md).

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** and select the **Exception Reason** tab.

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

-   **Recommend only** \(default\): Exception reasons can only be submitted for Recommend level findings. The other levels don't display exception submission options.
-   **Act and Recommend**: Exception reasons can be submitted for both Act and Recommend level findings. Suggest and Review level findings don't display exception submission options.
-   **All levels**: Exception reasons can be submitted for Suggest, Review, Recommend, and Act level findings. All four levels display exception submission options in the Findings panel.


</td></tr><tr><td>

Enforce rejected exception reason validations

</td><td>

-   When enabled and an exception reason is rejected, the object linked to that reason is set to read-only.
-   Users can't make additional changes until the finding message is resolved or a new exception reason is submitted.
-   This confirms strict conformance with validation rules and prevents inconsistent or unauthorized updates while an exception is unresolved.
-   The setting applies to production and non-production instances.


</td><td>

Selected or cleared

</td></tr><tr><td>

Enable approvals in production \(**enable\_exception\_reason\_approvals\_in\_production**\)

</td><td>

-   Controls whether exceptions can be approved in production instances or only in development environments.
-   When disabled, exceptions can only be approved in the instances in which they are raised.
-   Select this setting on each non-production instance where you want exceptions approved in production.
    -   The setting is read-only on production and doesn't sync between instances.
    -   It is available after the instance is registered in My SN Instances. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md).


</td><td>

Selected or cleared

</td></tr><tr><td>

Approval group\(s\)

</td><td>

-   The group or groups that approve or reject exception reasons and receive notifications when new approvals are requested.
-   Set the approval groups on the production instance, as they don't sync between instances.


</td><td>

Select one or more approval groups

</td></tr><tr><td>

Exclude approved exception reasons from technical debt

</td><td>

-   When enabled, findings with approved exception reasons are excluded from technical debt metrics.
-   This does not remove the finding from the system.


</td><td>

Selected or cleared

</td></tr><tr><td>

Upon new finding found \(**er\_finding\_number\_validation**\)

</td><td>

Determines how an existing approved exception reason is handled when the same issue is detected again in a subsequent scan.

</td><td>

-   **Auto Accept Existing Reason**: The existing approved reason carries forward automatically, and no re-approval is required.
-   **Re-approve Existing Reason**: The existing reason is suspended and must be re-reviewed before it takes effect again.


</td></tr><tr><td>

Upon line number change \(**exception\_reason\_validation**\)

</td><td>

Determines how an approved exception reason is handled when the finding's line number changes in the code, for example after a refactor.

</td><td>

-   **Auto Accept Existing Reason** \(default\): The exception reason stays approved even if the line number shifts. Use this when minor code movement is expected.
-   **Re-approve Existing Reason**: Any line number change requires re-review. Use this when line position is meaningful to the exception context.


</td></tr></tbody>
</table>
## Result

The system decides who can approve or reject an exception as follows. When **Enable approvals in production** is selected, the system checks whether the user is in an approval group. If so, the user can approve or reject the exception. If not, the system checks whether the user has the Scan Engine exception approver role, sn\_se.scan\_engine\_exception\_approver. When the setting is cleared, approval or rejection happens only in the instance where the exception was raised, and the system checks for the approver role.

-   **[Configure exception approval behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-exception-reasons-scan-engine.md)**  
Configure how exception reasons are enforced, approved, and re-evaluated when findings are detected using the Scan Engine. Settings control exception behavior.

**Parent Topic:**[Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-scan-engine-properties.md)

