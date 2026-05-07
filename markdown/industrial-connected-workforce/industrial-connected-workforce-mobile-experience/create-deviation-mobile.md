---
title: Create a deviation in the Industrial Connected Workforce Mobile application
description: Create a deviation in the mobile app to report an issue that deviates from standard operations, such as an equipment malfunction. This way the issue can be tracked, investigated, and resolved.
locale: en-US
release: australia
product: Industrial Connected Workforce Mobile Experience
classification: industrial-connected-workforce-mobile-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Industrial Connected Workforce Mobile Experience, Industrial Connected Workforce]
---

# Create a deviation in the Industrial Connected Workforce Mobile application

Create a deviation in the mobile app to report an issue that deviates from standard operations, such as an equipment malfunction. This way the issue can be tracked, investigated, and resolved.

## Before you begin

Role required: sn\_icw.deviation\_user or sn\_icw.deviation\_expert

## About this task

A deviation is any type of equipment or work anomaly that has an impact on work safety, performance, or quality. Creating a deviation means reporting an issue that deviates from the expected standard of operation and starting the resolution process needed to address the issue.

## Procedure

1.  Navigate to **Home page**.

2.  From the Actions menu, select **New deviation**.

    ![New deviation menu option](../image/actions-icw-mobile.png)

3.  On the Deviation form, fill in the fields.

    For a description of the field values, see [Deviation form](../reference/deviation-form-mobile.md).

4.  Select **Next**.

5.  On the Deviation form, fill in the fields.

    For a description of the field values, see [Deviation form](../reference/deviation-form-mobile.md).

6.  Select **Next**.

7.  If applicable, select the origin.

8.  Select the active material that relates to the deviation.

9.  If applicable, select a resolution code.

    The resolution code can be one of the following:

    -   None
    -   Not fixed
    -   Fixed by operator
    -   Fixed by maintenance
10. Select **Submit**.


## Result

The deviation is displayed in the list of industrial tasks and can be viewed or edited. If a resolution code is provided while creating a deviation, the deviation is created in the Closed state by default. In all other cases, the deviation is created in the Found state.

The opened deviation can be:

-   Edited
-   Scheduled for a different time
-   Delayed
-   Fixed
-   Closed
-   Canceled

**Note:** The actions Close, Cancel, and Reopen are restricted to users with the sn\_icw.deviation\_expert role. Other actions are supported for both the sn\_icw.deviation\_user and sn\_icw.deviation\_expert role.

-   **[Contextualize an external document using AI Enhanced recommended actions for ICW Mobile](use-ai-enhanced-ra-icw-mobile.md)**  
With the AI Enhanced recommended actions for Industrial Connected Workforce Mobile Experience, you can contextualize an external document to get an explanation of why the document is relevant to a deviation.
-   **[Generate an action plan using AI Enhanced recommended actions for ICW Mobile](generate-action-plan-ai-enhanced-ra-icw-mobile.md)**  
Generate an action plan to document and track remediation steps for an Industrial Connected Workforce Mobile Experience \(ICW Mobile\) deviation. Action plans help you organize tasks, assign responsibilities, and monitor progress toward resolution.

**Parent Topic:**[Using the Industrial Connected Workforce Mobile Experience](../concept/using-icw-mobile-experience.md)

