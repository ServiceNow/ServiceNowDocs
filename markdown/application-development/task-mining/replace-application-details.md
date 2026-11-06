---
title: Create event filters to capture or exclude activity
description: Set up event filters before starting a Task Mining project to capture specific application activity or exclude sensitive data. If no filters are active, all activity is captured.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/task-mining/replace-application-details.html
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 1
breadcrumb: [Configure, Task Mining, Discover, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Create event filters to capture or exclude activity

Set up event filters before starting a Task Mining project to capture specific application activity or exclude sensitive data. If no filters are active, all activity is captured.

## Before you begin

Role required: sn\_tm\_core.power\_user, sn\_tm\_core.admin

## About this task

An event filter uses conditions based on application name, URL, or window name to identify what activity to capture. Filters support multiple conditions combined with `AND` or `OR` logic.

You can add exceptions to exclude specific screens or pages within captured applications, for example, to avoid collecting data from password fields or payroll screens.

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the Event filters icon \[Omitted image "event-filters-icon-tm.png"\].

3.  Select **Create event filter**.

    \[Omitted image "event-filter-tm1.png"\] Alt text: Create event filters button on the Event filters page.

4.  Create the event filter to capture activity.

    1.  Enter an **Event filter name**.

    2.  Complete the filter rule to select the applications to capture based on **Application**, **Window name**, or **URL**.

        Supported operators are **Equals**, **Contains**, **Starts with**, **Ends with**, and **Is any**.

    3.  Select **Add condition set** to add another application to the filter, and select **and** or **or** to combine them.

    4.  Select **Next**.

        \[Omitted image "event-filter-tm2.png"\] Alt text: Applications interface on the Applications to capture page.

5.  Add exceptions to exclude specific activity, for example, a password screen.

    Excluded activities are discarded on workstations and never stored.

    1.  Select **Add exception**.

    2.  Enter an **Exception name**.

    3.  Complete the filter rule to select the applications to exclude from the filter based on application, window name, or URL.

    4.  Select **Add condition set** to add another application to the exclusion list, and select **and** or **or** to combine them.

    5.  Select **Next**.

        \[Omitted image "event-filter-tm3.png"\] Alt text: Exceptions interface on the Exceptions to exclude page.

6.  Review what the filter captures and excludes.

7.  Select **Activate this filter** to turn on the filter immediately.

    If no filters are active, all activity is captured.

    \[Omitted image "event-filter-tm4.png"\] Alt text: Activation toggle on the Review page.

8.  Select **Create event filter**.


