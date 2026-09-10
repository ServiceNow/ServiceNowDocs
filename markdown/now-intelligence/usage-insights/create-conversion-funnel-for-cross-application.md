---
title: Create cross-application conversion funnels
description: Conversion funnels outline a sequence of steps to measure user progression, identify drop-off points, and track the time taken for each transition. The cross-application capability eliminates the requirement for every step to be in the same application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/usage-insights/create-conversion-funnel-for-cross-application.html
release: australia
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 2
keywords: [cross application funnel]
breadcrumb: [Create a conversion funnel, Conversion funnels, Using Usage Insights, Usage Insights, Platform Analytics]
---

# Create cross-application conversion funnels

Conversion funnels outline a sequence of steps to measure user progression, identify drop-off points, and track the time taken for each transition. The cross-application capability eliminates the requirement for every step to be in the same application.

## Before you begin

Role required: none

## About this task

Each funnel step has its own application picker, which is what makes a cross-application journey possible. A step can target all applications or one specific application, so consecutive steps can follow a user from one application into another.

The scope of the funnel is set by the first step:

-   **Session based**

    Counts only users who completed the subsequent steps within the same session. Use this scope to answer questions such as how many users who opened the Service Operations Workspace home page discovered a new feature in that same session.

-   **User based**

    Counts users who completed the subsequent steps at any time, with no single-session constraint. Use this scope for journeys that span multiple visits, such as how many users completed a training course after visiting the learning portal.


## Procedure

1.  Navigate to **All** &gt; **User Experience Analytics**

2.  Select **All Applications** from the application picker dropdown.

3.  In the left navigation, select **Conversion funnel**.

    The cross-application **Overview** page opens.

4.  Select the scope of the funnel.

    -   To require that all steps occur within one session, select the session-based option.
    -   To allow the steps to occur across multiple sessions, select the user-based option.
5.  Create a conversion funnel.

    \[Omitted image "usage-create-cross-app-funnel.png"\] Alt text: Create a cross-application funnel

    The **New Funnel** dialog box opens on the **Overview** step.

6.  Complete the **Overview** step, and then continue to the **Steps** step.

7.  In **Step Type**, select the type of activity that the step represents.

    Available types include **Session Start \(1st\)** and **Session Start \(any\)** to anchor the journey, and **Page View** and **Event Trigger** to capture a specific page or action, including chat events.

8.  Select the page or event for the step.

    \[Omitted image "usage-create-croos-funnel-steps.png"\] Alt text: Steps to create cross-app funnel

9.  Add the next step, and configure it against a different application.

10. Repeat the previous step to add further steps to the journey.

11. Save the funnel.


## Result

The funnel reports the number of users who reached each step and the drop-off between steps, across the applications that the steps target.

## Tip

Select **Session Start \(any\)** for the first step when you want the funnel to begin from any visit. Then, add **Page View** or **Event Trigger** steps to measure what users do next, in one application or across several.

**Parent Topic:**[Create a conversion funnel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/usage-insights/create-funnel.md)

