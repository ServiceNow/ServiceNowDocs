---
title: Configure exception reasons for Scan Engine
description: Configure how exception reasons are enforced, approved, and re-evaluated when findings are detected using the ServiceNow Scan Engine.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-13"
reading_time_minutes: 1
breadcrumb: [Real-time prevention monitoring for Scan Engine, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure exception reasons for Scan Engine

Configure how exception reasons are enforced, approved, and re-evaluated when findings are detected using the ServiceNow Scan Engine.

## Before you begin

When real-time enforcement is on, Warning and Error level findings require an approved exception reason before the form can be saved. Recommend and Review level findings do not block form submission.

Role required: Scan Engine admin \(sn\_se.scan\_engine\_admin\)

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Scan Engine** &gt; **Administration** &gt; **Properties** &gt; **Exception reasons**.

    Configuration options for Exception Reasons displays.

2.  Set **Enforce rejected exception reason validations** to set enforcement behavior.

    When enabled and an exception reason is rejected, the linked object becomes read-only until the finding is resolved or a new exception reason is submitted.

    **Important:** Enable this option for production instances.

3.  Approval settings
4.  Set **Enable approvals in production**.

    Controls whether exceptions can be approved in the production instance, or only in the environment where they were raised.

    **Note:** This setting applies to production instances only. If set to false, exceptions raised in production must be approved in the originating development or non-production instance.

5.  Configure **Approval groups**.

    Add the group or groups that will approve or reject exception reason requests and receive notifications when new requests are submitted.

    In the **Approval group\(s\)** field, select your lab approval group.

6.  Enable technical debt exclusion
7.  Set **Exclude approved exception reasons from technical debt**.

    When enabled, findings with an approved exception reason are excluded from technical debt metrics. The finding remains in the system — it is not deleted.

    **Note:** Enable this option.

8.  Control re-evaluation behavior
9.  Set **Upon new finding found**.

    Determines how an existing approved exception reason is handled when the same issue is detected in a subsequent scan.

    |Auto Accept Existing Reason|Re-approve Existing Reason|
    |---------------------------|--------------------------|
    |The existing approved reason carries forward automatically. No re-approval required.|The existing reason is suspended and must be re-reviewed before it takes effect again.|

10. Set **Upon line number change**.

    Determines how an approved exception reason is handled when the finding's line number changes in the code — for example, after a refactor.

    |Auto Accept Existing Reason \(default\)|Re-approve Existing Reason|
    |---------------------------------------|--------------------------|
    |The exception reason stays approved even if the line number shifts. Use when minor code movement is expected.|Any line number change requires re-review. Use when line position is meaningful to the exception context.|

11. Select **Save**.


