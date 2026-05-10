---
title: View demo data in MetricBase
description: After ServiceNow personnel install the MetricBase and MetricBase Demo plugins, you can use the demo to get familiar with MetricBase.
locale: en-US
release: australia
product: MetricBase
classification: metricbase
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Working with demo data, Configure, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# View demo data in MetricBase

After ServiceNow personnel install the MetricBase and MetricBase Demo plugins, you can use the demo to get familiar with MetricBase.

## Prerequisites

-   MetricBase and the MetricBase demo plugins must be installed by ServiceNow personnel.
-   Role required: admin

1.  Navigate to **MetricBase Demo** &gt; **Drones** to see the name, model, length, width, altitude, and speed for all drones in the fleet. ![Drone metrics](../image/drone-metrics.png)
2.  Select **MetricBase Demo** &gt; **Metrics** to see how the metrics are defined. In the Time Series Metrics list, the column values specify the table where the drone's time-series metrics are stored, the names of all the metrics that are stored for each drone, and the retention policy for each metric. The retention policy specifies how frequently measurements are taken, and how long MetricBase retains that data.

    ![Metric definitions](../image/metric-definitions.png)

    Now that you've seen the drone data and learned how to find it, let's see how the data was collected using a retention policy.

3.  Select a retention policy. The Retention Policy form shows the definition for the policy. In the following example, this metric is measured once a minute for the first 8 days, then once every 10 minutes for the following 94 days, and then once an hour for the following 397 days. After that, the system discards the data.

    ![Retention policy](../image/retention-policy.png)

    See [MetricBase retention policies](metricbase-retention-policies.md).

4.  To see how the data is aggregated during the Retention Durations, select the left arrow \(&lt;\) at the top of the Retention Policy Schedules window to return to the Time Series Metrics list.
5.  Select a table name. The Time Series Metric definition shows the **Retention policy aggregator**. This aggregator summarizes the data as, for example, the average, maximum, or minimum value in the aggregation period. In the following example, the admin clicked the table for the speed metric. The result is that MetricBase stores the speed averages during each sampling period in the MetricBase database.

    ![Data aggregation](../image/data-aggregation.png)

    Now that you understand how the data was collected using retention policies, let's see how to display the data in lists and graphs.

6.  Notice the parameter fields that start with **Display**. In this example, they mean that the speed values that are displayed in the list view of drones are the last speeds recorded in every hour interval for each drone. These **Display** fields control what appears in the list view of the drones only. They have nothing to do with the retention policy.
7.  Display the list view of a table by entering `<table-name>.list` in the **Field navigator** field. For example, `mb_demo_drone.list`. All drone data appears. In the example from the previous step, the speed column would contain the **Last** value of the sampling period.
8.  Select **MetricBase Demo** &gt; **Drones** and look at the speed \(kph\) column. From the previous step, you know that these values are the last speeds recorded for each drone up to an hour ago. The values are the same as you would get by using the `.list` command.
9.  Select the speed value of the first drone. The following graph shows the speed of the drone that was measured hourly.

    ![Speed measured over time](../image/speed-measured-hourly.png)

    **Note:** You might need to select a different **Time Span** field value to get a clearer graph. For example, try **1 Day**. The speed is a sine wave because it's artificially generated. Hover over the sine wave to see the actual measurements.

10. Select the left arrow \(&lt;\) to return to the list of drone metrics, right-click on one drone type \(**Model** column\), and select **Show Matching**. Only the drones of the selected type appear.
11. Select the menu icon next to the Altitude column heading and select **Time Series Chart**. You see a graph that shows the altitude measurements of the Warbler-T7-type drones.

    ![Altitude of all the drones](../image/altitude-drones.png)

    You might like to change the **Time Span** value for a clearer graph.

12. Select the left arrow \(&lt;\) to return to the list of drone metrics.
13. Click the menu icon next to the Altitude column heading and select **Time Series Chart Designer** to see another way of visualizing the data. ![Create a report](../image/create-a-report.png)
14. In the Create a Report page that displays in the Reporting application, vary the graph parameters.

    **Note:** In the following steps, to stay on the same page, select **Run**. To advance to the next page when designing the graph, select **Next**.

    1.  In the Type pane, select the kind of graph to display, and then click **Next**. ![Graph type](../image/type-of-graph.png)
    2.  In the Configure pane, try changing the parameters. Click **Run** to view the results with each change.
        -   Change the **Report Title** to Warbler Altitude.
        -   Apply a condition to filter the view. For example, **\[Model\] \[is\] \[Warbler T7\]**.
        -   Change the **Last** value to **1** day.
        -   Select **Envelope** in the **Transform** list. You see the minimum and maximum \(envelope\) altitudes for the fleet of Warbler T7 drones over time.
        -   select the time line to display on the graph using the **Time range** list.

            **Note:** **Relative** uses the **Last** timespan relative to the present time. For example, if **Last** is 1 hour, the time line in the graph always spans the previous hour. You can add this report to your dashboard to show the metrics in the previous hour.

    3.  In the Style pane, change the **Chart color** value, and then click **Run**. ![Style pane](../image/style-pane.png)

        You've displayed drone data in lists and graphs. Now, let's define a trigger that executes when data that you monitor reaches a threshold value.

15. Select **MetricBase Demo** &gt; **Trigger Definitions**. The MetricBase Trigger Definitions list shows the name \(**Name**\) of the trigger, the metric \(**Metric**\) the trigger monitors, the table \(**Table name**\) the metric that it is in, the trigger description, and whether the trigger is active. Triggers kick off flows when metrics meet trigger thresholds. An example is when a drone flies too low. For more information about triggers, see [Trigger Workflows](../concept/metricbase-triggers.md).![Trigger definitions](../image/trigger-definitions.png)
16. Select **Low-Battery Drone**. The MetricBase Linear Predictor trigger form displays the definition of the Low-Battery Drone trigger.![Linear trigger](../image/trigger-example-low-altitude.png)

    In this example, the trigger monitors the **Remaining Battery \(%\)** metric \(**Metric**\) in the Drone table \(**Table name**\) every 10 minutes \(**Window**\). If the battery life is trending downward \(**Trend**\) and is 80% likely \(**Confidence Level**\) to reach 20% \(**Threshold**\) within 20 minutes \(under **Window** for **Level** 1\), the trigger executes. Although it fires, nothing happens until you associate this trigger with a flow. The flow defines the actions to take.

17. Select **MetricBase** &gt; **Trigger Flows**.
18. Select **New flow** to associate a trigger that is defined in the system to a flow.
19. In the **Flow name** field, name the flow and select **Submit**. ![Flow Properties dialog box](../image/flow-dialog-box.png)
20. Click **Add a Trigger** and select **MetricBase** in the list. ![Flow definition page](../image/flow-definition.png)
21. In **MetricBase Trigger**, select a trigger that already exists and select **Done**. Alternately, select the plus sign to the right of **MetricBase Trigger** to create a new trigger. ![Choose a MetricBase trigger](../image/flow-mb-trigger-selection.png)
22. Select **Add an Action, Flow Logic, or Subflow**.
23. Select **Action** to specify the actions to take when the trigger fires. The Action dialog box appears.

    ![Define an action](../image/flow-action.png)

24. Select a domain of actions from the left column and the specific action to take in the right column.
25. Select **Save** and **Activate**. The flow doesn't execute unless it is activated. For more information about Workflow Studio, see [Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/workflow-studio.md).

The following table summarizes the modules in the MetricBase demo.

|Module|Description|
|------|-----------|
|Drones|Table that keeps metrics on drones, such as speed and altitude. Each record is a different drone. You can add records.|
|Fleets|Table that maintains metrics about groups of drones. Each record is a different fleet. You can add records.|
|Data Generators|Table that defines how data is created for the drone records. This field is provided for informational purposes. You cannot change or add records.|
|Metrics|List of metrics that are defined in the system. This list is the same table as **MetricBase** &gt; **Time Series Metrics**. You can add metric fields.|
|Scheduled Jobs|Scheduled job that is created for the demonstration application. The job runs every five minutes to add data to the demo tables in the MetricBase database. You can change the schedule.|
|Trigger Definitions|List of triggers that are defined in the demo. This list is the same table as **MetricBase** &gt; **MetricBase Triggers** &gt; **Trigger Definitions**. You can create additional triggers.|
|Anomaly Logs|List of logs that result from triggers firing. The **Low-Flying Drone** trigger creates the anomaly logs.|
|Data Explorer|Widget that enables you to experiment with MetricBase JavaScript APIs using the demonstration application data. See [Get Familiar with MetricBase APIs](../task/metricbase-data-explorer.md) for more information.|

**Parent Topic:**[Working with MetricBase demo data](../concept/working-with-metricbase-demo-data.md)

