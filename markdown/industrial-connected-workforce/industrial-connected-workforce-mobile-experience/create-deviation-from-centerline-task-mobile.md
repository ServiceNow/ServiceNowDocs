---
title: Create a deviation from a centerline task
description: When you submit a centerline audit task with parameters that are outside specified values, a deviation is automatically created for each non-compliant parameter. Issues are tracked immediately, with no manual deviation entry required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/create-deviation-from-centerline-task-mobile.html
release: australia
product: Industrial Connected Workforce Mobile Experience
classification: industrial-connected-workforce-mobile-experience
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 2
keywords: [deviation, non-compliant, centerline audit, out of specification]
breadcrumb: [Use, Industrial Connected Workforce Mobile Experience, Industrial Connected Workforce]
---

# Create a deviation from a centerline task

When you submit a centerline audit task with parameters that are outside specified values, a deviation is automatically created for each non-compliant parameter. Issues are tracked immediately, with no manual deviation entry required.

## Before you begin

Role required: icw\_operator

## About this task

When you mark a parameter as out of specification and submit the centerline audit task, a deviation is created automatically in the background. You do not need to take any additional action to log the non-compliance. The deviation is linked back to both the originating centerline task and the specific parameter it was created from, so issues are fully traceable.

**Note:** The system creates one deviation per non-compliant parameter result. If you correct a value from non-compliant to compliant before submitting, a deviation is not created for that parameter.

## Procedure

1.  Execute the centerline audit task.

    For the full execution procedure, see [Execute a centerline audit task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/execute-centerline-audit-task-mobile.md).

2.  When you have entered all parameter values, select **Submit**.

    For any parameter marked as out of specification, the system automatically creates a deviation.

3.  Open the **Related** tab on the centerline audit task.

    The related deviations are listed. Each deviation is linked to the specific non-compliant parameter that triggered it.


## Result

Each automatically created deviation contains the following information from the originating centerline task and parameter:

-   Short description prefixed with **\[CL Not compliant\]** followed by the setting definition name
-   Setting name, setting description, confirmed value, specification value, all limits and targets, equipment name, and functional location name in the description
-   Equipment and functional location fields populated from the originating task
-   Active material from the originating task
-   Creator populated from the operator who submitted the task
-   Origin set to **Centerline Task**
-   Category set to **Other**

## What to do next

To view or update the deviation record, see [Create a deviation in the Industrial Connected Workforce Mobile application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/create-deviation-mobile.md).

**Parent Topic:**[Using the Industrial Connected Workforce Mobile Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/industrial-connected-workforce-mobile-experience/using-icw-mobile-experience.md)

