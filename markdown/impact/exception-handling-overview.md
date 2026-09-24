---
title: Exception handling in Scan Engine
description: Exception handling enables developers and administrators to manage findings that are out of scope, pre-existing, or acceptable risks. The Scan Engine exception model supports enterprise approval workflows, predictable lifecycle behavior, and reliable governance across all finding levels.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/exception-handling-overview.html
release: brazil
topic_type: concept
last_updated: "2026-08-22"
reading_time_minutes: 5
keywords: [exceptions, exception reasons, exception approval, findings, governance]
breadcrumb: [Prevent technical debt with real-time code fixes, Platform Health, Using Impact, Impact]
---

# Exception handling in Scan Engine

Exception handling enables developers and administrators to manage findings that are out of scope, pre-existing, or acceptable risks. The Scan Engine exception model supports enterprise approval workflows, predictable lifecycle behavior, and reliable governance across all finding levels.

## What are exception reasons

Exception reasons allow developers to request that findings be excluded from technical debt metrics and blocked workflows. When a finding is detected that an organization determines should not be considered an issue, developers can submit an exception request with supporting rationale. After approval by designated administrators, the finding is excluded from technical debt calculations and no longer blocks form submissions.

Exception handling serves several key purposes:

-   Unblock Update Set closure when findings are out of scope or represent acceptable risks
-   Exclude pre-existing or non-blocking issues from technical debt metrics
-   Maintain audit trails showing which findings have been reviewed and approved
-   Support enterprise governance patterns where approvals follow organizational structures

## Exception reason scope

Exception reason scope controls which finding levels can have exception reasons submitted and approved. Administrators configure the scope to match organizational needs. Three scope options are available:

|Scope Option|What it means|
|------------|-------------|
|**Recommend only** \(default\)|Exception reasons can only be submitted for Recommend level findings. Suggest, Review, and Act level findings don't display exception submission options.|
|**Act and Recommend**|Exception reasons can be submitted for both Act and Recommend level findings. Suggest and Review level findings don't display exception submission options.|
|**All levels**|Exception reasons can be submitted for Suggest, Review, Recommend, and Act level findings. All four levels display exception submission options in the Findings panel.|

The exception scope you select determines the user experience in the Findings panel. When exception reasons are enabled for a finding level, developers see a **Create exception** button on the finding card. When exceptions aren't enabled for a finding level, the button won't appear.

## Approval and enforcement

After a developer submits an exception request, designated approval groups review the request and either approve or reject it. Approvers can be different from administrators who configured the exception settings. When an exception is approved, the finding is automatically excluded from technical debt metrics.

Key approval behaviors include:

-   **Approval groups**

    Administrators assign one or more groups that receive exception requests and notifications. Approvers within these groups review and respond to requests.

-   **Auto approval**

    Administrators can configure exception requests to be automatically approved or to require explicit approval.

-   **Enforce rejected validations**

    When enabled, if an exception request is rejected, the linked object is set to read-only until the finding is resolved or a new exception is submitted.

-   **Re-evaluation on new findings**

    Administrators control whether approved exceptions automatically apply when the same issue is detected in a subsequent scan, or whether they require re-approval.

-   **Re-evaluation on line changes**

    Administrators control whether approved exceptions remain valid when the finding's line number changes in the code, for example after a refactor.


## Exception lifecycle

\[Omitted image "exception-lifecycle.png"\] Alt text: The developer lifecycle for submitting an exception.

## Finding levels and exception eligibility

The Scan Engine classifies findings into four levels based on severity and risk:

|Level|Severity|Form blocking and exception behavior|
|-----|--------|------------------------------------|
|Suggest|Low|Doesn't block form submission. Exception reasons can be submitted if the scope is set to All levels.|
|Review|Low-Medium|Doesn't block form submission. Exception reasons can be submitted if the scope is set to All levels.|
|Recommend|Medium-High|Blocks form submission when real-time enforcement is enabled, unless an approved exception reason exists. Exception reasons can be submitted if the scope is set to Recommend only, Act and Recommend, or All levels.|
|Act|Critical|Blocks form submission when real-time enforcement is enabled, unless an approved exception reason exists. Exception reasons can be submitted if the scope is set to Act and Recommend or All levels.|

## Common use cases

-   **Out-of-scope findings**

    A definition triggers on utility functions or platform code that your team intentionally excludes from scanning. Rather than disabling the definition, submit exceptions for out-of-scope matches so the definition remains active for other code contexts.

-   **Pre-existing issues**

    A finding identifies an issue that exists in legacy code. Rather than blocking Update Set closure, submit an exception with a plan to remediate in a future release.

-   **Acceptable risks**

    A finding identifies a pattern that your team has reviewed and determined is acceptable for your use case. Submit an exception to exclude it from technical debt and avoid form blocking.

-   **Update Set closure**

    An Update Set contains a finding at Act level that prevents closure. Developers submit an exception explaining why the change is necessary. Approvers review and approve, allowing the Update Set to proceed.


## Roles and permissions

Exception handling requires specific roles and permissions. Developers can submit exceptions when they have developer roles. Administrators configure exception settings when they have admin or Scan Engine admin roles. Approvers can be any user assigned to an approval group.

See [Roles installed with Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-roles.md) for detailed role descriptions, including roles that manage exception approvals.

## Related tasks

To implement exception handling in your organization, see:

-   [Configure exception approval behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-exception-reasons-scan-engine.md) — Configure the exception reason scope, approval groups, and re-evaluation behavior.
-   [Submit exceptions for Scan Engine findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/submitting-exception-reasons-scan-engine.md) — Submit exception requests for findings that your team has reviewed.
-   [Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/exception-reason-properties.md) — Configure detailed exception reason settings including enforcement and technical debt exclusion.

