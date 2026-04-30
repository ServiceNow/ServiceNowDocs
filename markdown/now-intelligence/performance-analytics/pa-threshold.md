---
title: Indicator thresholds
description: Thresholds define a normal range of scores for an indicator and alert you when certain events occurs, like when a score reaches an all-time high.Create a threshold to define the range of scores considered normal.Configure which users should receive an email when a threshold is reached.The Check PA Thresholds job triggers the PA threshold reached comment script action, which adds a comment for the indicator that has reached the threshold.Besides the notifications for each indicator, you can also send notifications with an overview of all indicators for which the threshold is reached.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Targets and thresholds, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Indicator thresholds

Thresholds define a normal range of scores for an indicator and alert you when certain events occurs, like when a score reaches an all-time high.

When a threshold is triggered, the instance generates an email notification. This message is associated with the indicator and the message is directly available via the Analytics Hub or KPI Details.

A threshold can be personal or global. A personal threshold is visible only to the user that created it and appears as a light grey dotted line, a global threshold is visible to all users and appears as a dark grey dotted line. Personal thresholds appear only on the Analytics Hub and KPI Details. The matrix of threshold visibility follows:

|Platform Analytics experience feature|Equivalent Core UI feature|Global or Personal targets|
|-------------------------------------|--------------------------|--------------------------|
|[KPI Details](../../par-for-workspace/concept/kpi-details.md)|[Analytics Hub](c_UsePerformanceAnalyticsScorecards.md)|Global and personal|
|[Time series Platform Analytics data visualizations](../../reporting/task/create-dv-time-series-ac.md)|[Time series Performance Analytics widgets](../reference/time-series-widgets.md)|Global|
|[Dashboards in Platform Analytics](../../par-for-workspace/concept/analytics-center-dashboards.md) containing time series data visualizations that show thresholds|[Responsive dashboards](../../dashboards/reference/dashboards-landing-page.md) containing Time series Performance Analytics widgets that show thresholds|Global|
|[Proactive analytics insights cards](../../par-for-workspace/concept/proactive-analytics.md) on Platform Analytics dashboards, which show thresholds being breached|No equivalent|Global|
|UI Builder pages containing time series data visualizations that show thresholds|No equivalent|Global|

Global thresholds can also appear on Performance Analytics [time series widgets](../reference/time-series-widgets.md) and [data visualizations](../../reporting/task/create-dv-time-series-ac.md). Platform Analytics dashboards can alert viewers to events related to thresholds through [proactive analytics insights cards](../../par-for-workspace/concept/proactive-analytics.md).

**Parent Topic:**[Performance Analytics targets and thresholds](pa-targets-thresholds.md)

## Create or edit a threshold

Create a threshold to define the range of scores considered normal.

### Before you begin

Role required: Any role for your own personal thresholds. The pa\_threshold\_admin role or a role containing it \(pa\_power\_user, pa\_admin, or admin\) for global thresholds and for personal thresholds created by other users.

### About this task

Thresholds can be set for any indicator. You can specify a breakdown and element combination and a time series aggregate that a threshold applies to.

### Procedure

1.  Open KPI Details for an indicator.

    If you are not using Platform Analytics, open the Analytics Hub instead.

2.  To limit the threshold to a subset of the scores, select a breakdown and a breakdown element.

    You can also select a 2nd-level breakdown and element. You can select more breakdowns if the indicator has [data snapshots](multi-level-breakdowns.md) enabled.

3.  If the threshold should apply only to a specific aggregation of the data, select a time series aggregation.

4.  Click the threshold icon \(![](../image/Threshold_Icon.png)\).

    The Thresholds panel opens.

5.  In the Thresholds panel, select either a Global or a Personal threshold.

    Personal thresholds are visible only to you, although users with the admin role can edit or delete them Personal thresholds are not visible on widgets.

6.  Either create a new threshold or edit or delete an existing threshold:

    -   To create a threshold, click the plus + sign.
    -   To edit an existing threshold, click it in the Thresholds panel.
    -   To delete an existing threshold in the Analytics Hub, click the delete icon. ![](../image/delete-threshold-ah.png)

        To delete an existing threshold in KPI Details, open it for editing and click **Delete**.

7.  If you are creating or editing a threshold, select the condition that triggers the threshold notification.

    The condition can be when the score reaches an all-time high, or when the score falls lower than a specific value.

8.  Click **Save**.


### What to do next

After you create a threshold, set up threshold notifications.

**Related topics**  


[KPI Details](../../par-for-workspace/concept/kpi-details.md)

## Configure which users receive a threshold notification

Configure which users should receive an email when a threshold is reached.

### Before you begin

Role required: The pa\_threshold\_admin role or a role containing it \(pa\_power\_user, pa\_admin, or admin\)

### About this task

This procedure applies to global thresholds. Notifications for personal thresholds are sent only to the owner of the threshold.

### Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **Indicators** &gt; **Thresholds**.

    If you are not fully migrated to Platform Analytics, the path is **All** &gt; **Performance Analytics** &gt; **Indicators** &gt; **Thresholds**

2.  Open a threshold.

3.  In the **Users** related list, click **Edit**.

4.  In the Edit Members screen, select and add members.

5.  Click **Save**.


### What to do next

Besides the notifications for each indicator, you can also send notifications with an overview of all indicators for which the threshold is reached. For more information, see [Configure threshold overview notifications](pa-threshold.md#).

## Configure the threshold comment

The Check PA Thresholds job triggers the PA threshold reached comment script action, which adds a comment for the indicator that has reached the threshold.

### Before you begin

Role required: admin

### About this task

The comment is displayed when you open KPI Details or the Analytics Hub for the indicator. Configure the threshold comment to display different text.

### Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Events** &gt; **Script Actions**.

2.  Open **PA threshold reached comment**.

3.  Modify the buildMessage function within the script.

4.  Select **Update**.


## Configure threshold overview notifications

Besides the notifications for each indicator, you can also send notifications with an overview of all indicators for which the threshold is reached.

### Before you begin

Role required: admin

### About this task

This procedures describes how to access the summary notification and change the users who receive the notification as well as the content of the notification.

### Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Email** &gt; **Notifications**.

2.  Select **PA Thresholds Notification**.

3.  Add users or groups to the **Who will receive** section by clicking the lock icon for either **Users** or **Groups** and then selecting the appropriate users or groups.

4.  Change the content of the message by modifying the **Message** field.

5.  Click **Update**.


