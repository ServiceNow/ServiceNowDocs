---
title: Configure exception reason properties
description: When real-time enforcement, enforce\_real\_time\_validation is set to true, Warning and Error level findings, without approved exception reasons, require users to provide one before the form can be saved. Recommend and Review level findings do not block form submission.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Configure Scan Engine properties, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure exception reason properties

When real-time enforcement, `enforce_real_time_validation` is set to `true`, Warning and Error level findings, without approved exception reasons, require users to provide one before the form can be saved. Recommend and Review level findings do not block form submission.

## Before you begin

Role required: Scan Engine Admin \(`sn_se.scan_engine_admin`\).

## Procedure

1.  Select whether to **Enforce rejected exception reason validations**.

    When enabled, and if an exception reason is rejected, the object linked to that reason becomes read-only. Users cannot make additional changes until either:

    -   The Recommend level message is resolved.
    -   A new exception reason is submitted.
    This ensures strict compliance with validation rules and prevents inconsistent or unauthorized updates while an exception is unresolved.

2.  Select whether to **Enable approvals in production**.

    If `enable_exception_reason_approvals_in_production` is set to `false`, exceptions can only be approved in the instances in which they are raised.

3.  Approval groups will approve or reject exception requests and receive notifications.

    -   Use the`Enable approvals in production` setting to control whether exceptions can be approved in production instances or only in development environments.
    -   Approval group\(s\) displays the group or groups that will approve or reject exception reasons and also receive notifications when new approvals are requested.
    **Note:** This setting is only applicable to development instances.

4.  Select whether to **Exclude approved exception reasons from technical debt**.

    When enabled, findings with approved exception reasons will be excluded from technical debt metrics.

    **Note:** This does not remove the finding from the system.

5.  **Upon new finding found**, `er_finding_number_validation` , determines how exception reasons are handled when the same issue is detected again in a subsequent scan.

    Options are: **Auto Accept Existing Reason** and **Re-approve Existing Reason**.

6.  **Upon line number change**, `exception_reason_validation`

    -   ``Determines how approved exception reasons are handled when the finding's line number changes in the code.
    -   Options are **Auto Accept Existing Reason** \(default\) and **Re-approve Existing Reason**.
    Choose whether to automatically accept the existing reason.


