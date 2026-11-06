---
title: Configure exception approval behavior
description: Configure how exception reasons are enforced, approved, and re-evaluated when findings are detected using the Scan Engine. Settings control exception behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/configure-exception-reasons-scan-engine.html
release: australia
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 1
breadcrumb: [Configure exception reason properties, Configure Scan Engine properties, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Configure exception approval behavior

Configure how exception reasons are enforced, approved, and re-evaluated when findings are detected using the Scan Engine. Settings control exception behavior.

## Before you begin

All instances must be registered in My SN Instances before configuring approval settings. See [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md) for details.

Role required: Scan Engine admin \(sn\_se.scan\_engine\_admin\)

## About this task

This task sets the exception reason options in order. For what each setting does and the values it accepts, see [Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/exception-reason-properties.md). For an overview of exception reasons and the approval lifecycle, see [Exception handling in Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/exception-handling-overview.md).

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** and select the **Exception Reason** tab.

    The exception reason settings are displayed.

2.  Select or clear **Enforce rejected exception reason validations**.

3.  Select the **Exception reason scope**: **Recommend only**, **Act and Recommend**, or **All levels**.

4.  On each non-production instance where you want exceptions approved in production, select **Enable approvals in production**.

5.  On the production instance, in the **Approval group\(s\)** field, select the group or groups that approve or reject exception reasons.

6.  Select or clear **Exclude approved exception reasons from technical debt**.

7.  Control re-evaluation behavior.

    1.  For **Upon new finding found**, select **Auto Accept Existing Reason** or **Re-approve Existing Reason**.

    2.  For **Upon line number change**, select **Auto Accept Existing Reason** or **Re-approve Existing Reason**.

8.  Select **Save**.


**Parent Topic:**[Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/exception-reason-properties.md)

