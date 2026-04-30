---
title: Accessing Analytics Dashboards
description: Access the Analytics Dashboards to view detailed information relating to Scan Engine findings, both pending and resolved.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 1
breadcrumb: [Analytics Dashboards, Scan Engine, Platform Health, Using Impact, Impact]
---

# Accessing Analytics Dashboards

Access the Analytics Dashboards to view detailed information relating to Scan Engine findings, both pending and resolved.

## Before you begin

Make sure you have been assigned the correct persona for your role.

Role required: Executive, Platform Owner, Team Lead, or Developer.

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Analytics Dashboard**.

    Your assigned role is listed at the top left, which determines which dashboard view you can access.

2.  If you have been assigned to more than one role, select which dashboard to view.

    The date listed is the last completed scan date to let you know whether the charts in the dashboard are up-to-date.​

    **Note:** All dashboard metrics fluctuate as the scan progresses and will stabilize once it completes.

3.  On the **Options** list, select one of the following:

    -   **Scan progress**: Display the full scan progress page for complete metrics of any currently running or previously run scan.
    -   **Property configuration**: Open the Scan Engine properties page.
4.  To sort and view a chart or table, select **Option**, and then select one of the following:

    -   **Cost**: Cost is calculated by multiplying the Average development rate \(configured in the Scan Engine properties\) by the estimated time to resolve the finding \(as set in the finding’s associated definition\).
    -   **Count**: The total number of findings.
    -   **Time**: Each definition includes an estimated time to resolve based on expert-driven recommendations. These estimates serve as practical guidelines to help teams estimate how long an issue should take to fix on average, promoting better planning and prioritization.
5.  On Executive  and  Team Lead  dashboards, select a date range for trend chart data:

    -   Pre-defined range
    -   ​Custom  range: Select start and end dates. Enter  the start and end dates directly into the range textbox, then select **Apply**.
    **Note:** The amount of historical data stored and displayed in these metrics varies depending on the data restrictions associated with your Platform Analytics package.

6.  On Team Lead and Developer dashboards, select the download button to save a CSV file of the currently displayed data in a table.

    Blue text within table cells are hyperlinks to other modals or new tabs. Blue table column headers are sortable \(select the header to sort\). In sorted tables, the sorted column will have a small caret next to its name.


