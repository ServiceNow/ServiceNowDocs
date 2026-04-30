---
title: Create an email notification for indicators
description: Performance Analytics can automatically generate an email with the score, change %, target, and score-target gap % of one or more indicators.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Performance Analytics indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create an email notification for indicators

Performance Analytics can automatically generate an email with the score, change %, target, and score-target gap % of one or more indicators.

## Before you begin

Enable and configure email notifications before you can use email summaries.

Role required: pa\_admin or admin

## Procedure

1.  Expand **All** and enter `sysauto_indicator_notifications_list.do` into the navigator Search field, then press **Enter**.

2.  Click **New**.

3.  Enter a **Name** and a **Description** for the email summary.

4.  Select the **Active** check box to run a scheduled job that creates the email summary.

5.  Select when the job should run.

    -   Daily
    -   Weekly
    -   Monthly
    -   Periodically
    -   Once
    -   On Demand
6.  Set the time to run the job by changing the hours, minutes, and seconds \(using 24-hour notation\).

    By default, the job runs at midnight.

7.  Select the indicators to include in the summary, either dynamically or manually.

    -   **Dynamically**

        Select the **By Condition** check box. Use the condition builder to define the conditions that determine which indicators the email summary includes. For example, you can select all key indicators by setting the condition to \[Key\] \[is\] \[true\].

    -   **Manually**

        Clear the **By Condition** check box. After you save the Scheduled Email Summary form, select individual indicators to include in the summary in the **Indicators** related list.

8.  Right-click the form header and select **Save**.

    The related lists become available.

9.  Select any number of users in the **Users** related list.

10. If you are selecting indicators manually, select them in the **Indicators** related list.


## Result

The email summary job runs based on the schedule you configured. You can also run the job manually by clicking **Execute Now**.

**Related topics**  


[Email and SMS notifications](https://www.servicenow.com/docs/access?context=c_EmailNotifications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

