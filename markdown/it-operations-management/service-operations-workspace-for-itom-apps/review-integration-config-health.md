---
title: Review integration and configuration health
description: Review your events to ensure alerts are created as intended. Start this process by checking the health status of your integration. This provides useful statistics to highlight where you can make improvements to enrich alerts with relevant business context, group them for better noise reduction, escalate critical alerts promptly, and notify your team for swift response and resolution.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 6
breadcrumb: [Integrations Launchpad in Service Operations Workspace for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Review integration and configuration health

Review your events to ensure alerts are created as intended. Start this process by checking the health status of your integration. This provides useful statistics to highlight where you can make improvements to enrich alerts with relevant business context, group them for better noise reduction, escalate critical alerts promptly, and notify your team for swift response and resolution.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## About this task

Health state metrics indicate how effectively alert automations add context and reduce noise, helping operators lower the Mean Time to Repair \(MTTR\). When adding a new integration, review these metrics, assess the rates, and develop new rules to further enhance noise reduction and improve overall system performance.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../../health-log-analytics-admin/image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  On the ITOM AIOps configuration center page, under the **Setup** &gt; **Integrations** section, select **Manage Installed integrations**.

4.  In the **Browse Integrations** tab, select the **All integrations** drop-down list and select **Pull** or **Push** as required.

5.  Select a pull, push, or a custom connector type tile.

    If a pop-up menu opens, select the data to track from that connector and select **Continue**.

6.  Select the **Events** tab.

    ![Health state of a connector](../image/connector-related-events.png)

7.  In the Health state section, view the data for alerts and their associated attributes.

<table id="table_ogg_3fw_mbc"><thead><tr><th>

Alert attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Alert Suppression

</td><td>

The suppression ratio indicates the proportion of alerts created to events received. Reducing unwanted alerts can be achieved by de-duplicating or ignoring them.

 -   De-duplication: The **message\_key** field is a unique identifier for an alert in the source monitoring system. It is used for de-duplication and alert flapping detection purposes. If the source event does not provide reliable unique values, you can use the default value or create your own.

If the message key is not defined, the default message key will be &lt;Source + Node + Type + Resource + Metric Name&gt;. The guideline is for the event source to automatically populate the &lt;Source + Node + Type + Resource + Metric Name&gt; fields and generate the message key. This practice facilitates better distribution of event processing across instance workers and nodes.

If the source event does not provide values for these fields, ensure they are populated using transform rules. This action, which does not impact event processing, is essential for de-duplication. Populate as many of these fields as possible before sending the event to the instance. Doing so enhances the distribution of events across processor workers, resulting in improved throughput and scalability.

To learn more about de-duplication, see [Event Management configuration preferences](../../event-management/reference/r_EMBestPractice.md). To set the message key in your custom connector integration, see [Configure an event custom connector](custom-connector.md).

-   Ignore alert event rules: Filter out low-quality alerts by creating an [ignore automation](create-ignore-automation-sow-itom.md).


</td></tr><tr><td>

Alert compression rate

</td><td>

When you group alerts, a high compression rate is desirable because it means fewer alerts remain for your operations team to review and act on. This can lead to improved team efficiency. The compression rate is calculated as 1 – \(the number of alert groups + the number of ungrouped alerts\) / total alerts.

 To learn about alert aggregation, see [Alert grouping](../../event-management/concept/c_ServiceAnalyticsOverview.md). One way to improve your alert compression rate is by defining a new grouping automation.

</td></tr><tr><td>

CI Binding

</td><td>

The percentage of alerts successfully bound to a Configuration Item \(CI\) in your CMDB is crucial. Aim for this number to be at or near 100% to enhance alert grouping, root cause analysis, assignment, and more.

 To bind a host, machine, or any device with an IP, populate the **Node** field with a unique hostname, FQDN, IP, or MAC address. This can be done within the integration itself or by creating an enrich automation. For more complex scenarios, you can override node-based binding using event rules. For more information on CI binding, see [Binding alerts to CIs](../../event-management/concept/ci-binding-alert.md).

</td></tr><tr><td>

Metric name configured

</td><td>

Shows the percentage of alerts that have a metric name defined. It's crucial to aim for near 100% because it's used by default in our automated correlation algorithm. This can be achieved within the integration itself or by creating an [enrich automation](enrich-alert-sow-itom.md).

</td></tr><tr><td>

Suggested tags

</td><td>

Provides suggested alert tags based on the integration payload. Alert tags are structured fields that you can define to facilitate easier filtering and grouping of alerts.

 The tags are stored in **sn\_itom\_integ\_app\_recommendation\_tags\_suggestion**, and only the top 5 most popular tags are displayed. In case you prefer to refine the results of suggestion mechanism, you can use property **sn\_itom\_integ\_app.evt\_mgmt\_tag\_suggestion\_ignore\_keys**, which displays a list of lowercase field names or keywords, separated by commas, to be ignored when scanning additional alert info for tag suggestions. Default value is time.

</td></tr></tbody>
</table>8.  In the Events section, ensure that your events are generating alerts as expected.

    Verify that alert fields and tags are populated correctly to make the alerts easier to read and filter in Express List. Confirm that severity values align with your operations team's expectations and that fields and tags follow a standardized format across sources for easier grouping.

    By verifying alert generation, you can be confident that your system is properly configured to detect and notify you of noteworthy occurrences. For information on the fields in the Events section, see [Integration and configuration health event fields](../reference/integration-config-health-event-fields.md).


## What to do next

Now that you've confirmed alerts from the events, you can initiate the alert automation process by selecting **Add automation**. This takes you to the ignore automation step, where you can disregard irrelevant or false-positive alerts. Following that, proceed to enrich, group, and automate responses. This process involves transforming raw alerts into a format understandable by ServiceNow, grouping the alerts, and escalating an alert to ensure an immediate response from the appropriate team or individual. For more information on alert automation, see [Alert automation in Service Operations Workspace for ITOM](../concept/sow-itom-alert-automation.md).

