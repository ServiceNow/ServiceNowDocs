---
title: Centerline audit tasks in the Industrial Connected Workforce Mobile Experience
description: Use centerline audit tasks in the Industrial Connected Workforce Mobile Experience to measure process parameters against published standards and record results directly from your mobile device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/centerline-audit-task-mobile.html
release: australia
product: Industrial Connected Workforce Mobile Experience
classification: industrial-connected-workforce-mobile-experience
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 2
keywords: [centerline audit, centerline task, mobile execution]
breadcrumb: [Explore, Industrial Connected Workforce Mobile Experience, Industrial Connected Workforce]
---

# Centerline audit tasks in the Industrial Connected Workforce Mobile Experience

Use centerline audit tasks in the Industrial Connected Workforce Mobile Experience to measure process parameters against published standards and record results directly from your mobile device.

Centerline audits help maintain process parameters within published standards. Without mobile support, operators record audit results on paper or skip them entirely, which creates compliance gaps and delays the detection of parameter drift. Centerline audit tasks bring the audit directly to the shop floor: you open the task on your mobile device, enter measured values, and receive immediate visual feedback on whether each parameter is within specification.

## What you can do with centerline audit tasks

From a centerline audit task on mobile, you can:

-   Navigate non-sequentially through setting groups organized as separate sections
-   View and edit task details, including the active material, before starting
-   Enter measured values for each parameter and receive immediate in-specification or out-of-specification feedback
-   Open the full setting definition for any parameter to access its complete specification
-   Automatically create a deviation for any parameter result outside specification limits when you submit the task

## Task lifecycle states

A centerline audit task moves through the following states:

-   **Ready**

    The task is available and waiting to be started. You can view and edit task details, including the active material, while the task is in this state.

-   **Work in progress**

    The task has been started. Parameter values are being entered. The active material field becomes read-only after the task leaves the **Ready** state.

-   **Submitted**

    All parameter values have been entered and the task has been submitted. The system automatically creates a deviation for each out-of-specification parameter when you submit the task.

-   **Closed complete**

    The task is complete and all required parameter results have been recorded.


## Finding centerline audit tasks

Centerline audit tasks appear in the task lists on the **Tasks** tab and on the home page carousels. For information about task list segments and filtering, see [Exploring Industrial Connected Workforce Mobile Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/exploring-icw-mobile-experience.md).

## Automatic deviations for non-compliant parameters

When you submit a centerline audit task with one or more parameters marked as out of specification, the system automatically creates a deviation for each non-compliant parameter. You do not need to create the deviation manually. For more information, see [Create a deviation from a centerline task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/create-deviation-from-centerline-task-mobile.md).

**Parent Topic:**[Exploring Industrial Connected Workforce Mobile Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/exploring-icw-mobile-experience.md)

