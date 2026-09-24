---
title: Configure exception approval behavior
description: Configure how exception reasons are enforced, approved, and re-evaluated when findings are detected using the Scan Engine. Settings control exception behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-exception-reasons-scan-engine.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure exception reason properties, Configure Scan Engine parameters, Activate Scan Engine and review settings, Impact Guided Setup, Configuring Impact, Impact]
---

# Configure exception approval behavior

Configure how exception reasons are enforced, approved, and re-evaluated when findings are detected using the Scan Engine. Settings control exception behavior.

## Before you begin

When real-time enforcement is enabled, Act and Recommend level findings require an approved exception reason before the form can be saved. Suggest and Review level findings don't block form submission. All four finding levels, Suggest, Review, Recommend, and Act, can have exception reasons configured when the Exception Reasons feature is enabled.

All instances must be registered in My SN Instances before configuring approval settings. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/register-your-instance.md) for details.

See [Understand scan results and findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/understand-scan-engine-results-findings.md) for additional information on finding levels.

Role required: Scan Engine admin \(sn\_se.scan\_engine\_admin\)

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health** &gt; **Configuration** &gt; **Scan Engine Properties** &gt; **Exception reasons**.

    Configuration options for Exception Reasons displays.

2.  Set **Enforce rejected exception reason validations** to set enforcement behavior.

    When enabled and an exception reason is rejected, the linked object becomes read-only until the finding is resolved or a new exception reason is submitted.

3.  Configure exception reason scope to control which finding levels can be submitted for exceptions.

    Exception reason scope determines which finding levels can have exception reasons submitted and approved. Three scope options are available:

    -   **Recommend only** - Exception reasons can only be submitted for Recommend level findings.
    -   **Act and Recommend** - Exception reasons can be submitted for both Act and Recommend level findings.
    -   **All levels** - Exception reasons can be submitted for Suggest, Review, Recommend, and Act level findings.
    1.  Set **Enable approvals in production**.

        Controls whether exceptions can be approved in the production instance, or only in the environment where they were raised.

    2.  Configure **Approval groups**.

        Add the group or groups that will approve or reject exception reason requests and receive notifications when new requests are submitted.

        In the **Approval group\(s\)** field, select your lab approval group.

4.  Set **Exclude approved exception reasons from technical debt**.

    When enabled, findings with an approved exception reason are excluded from technical debt metrics. The finding remains in the system.

5.  Control re-evaluation behavior.

    1.  Set **Upon new finding found**.

        Determines how an existing approved exception reason is handled when the same issue is detected in a subsequent scan.

        |Auto Accept Existing Reason|Re-approve Existing Reason|
        |---------------------------|--------------------------|
        |The existing approved reason carries forward automatically. No re-approval required.|The existing reason is suspended and must be re-reviewed before it takes effect again.|

    2.  Set **Upon line number change**.

        Determines how an approved exception reason is handled when the finding's line number changes in the code — for example, after a refactor.

        |Auto Accept Existing Reason \(default\)|Re-approve Existing Reason|
        |---------------------------------------|--------------------------|
        |The exception reason stays approved even if the line number shifts. Use when minor code movement is expected.|Any line number change requires re-review. Use when line position is meaningful to the exception context.|

6.  Select **Save**.


**Parent Topic:**[Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/exception-reason-properties.md)

