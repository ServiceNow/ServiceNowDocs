---
title: Create Ignore automation
description: Ignore automation streamlines the process of disregarding irrelevant or false-positive alerts from monitoring systems, efficiently managing alert fatigue by filtering out unnecessary notifications. As a result, teams can prioritize and resolve critical issues more effectively.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Alert automation in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Create Ignore automation

Ignore automation streamlines the process of disregarding irrelevant or false-positive alerts from monitoring systems, efficiently managing alert fatigue by filtering out unnecessary notifications. As a result, teams can prioritize and resolve critical issues more effectively.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_team\_operator, or srm\_responder

## About this task

Ignore automations filter out alerts from source monitoring systems that match specific conditions. Separately, Event Management ignores alerts that have a duplicated message key field or where the severity is **Clear**.

For users familiar with the classic Event Management experience, ignore automations provide a simpler interface with enhanced team support for the event filter section of event rules.

**Note:** Ignoring alerts before enriching them improves performance and simplifies the processing flow. The condition filter in ignore automations applies only to the original event, not the enriched one. Enrich automations do not run if **Don't run other enrich alert automations** is set to false, and another enrich automation with a lower order, the same source, and matching filter conditions already applies. To avoid conflicts, consider the enrich automation order, source, and filter conditions when creating enrichments or event rules.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../../health-log-analytics-admin/image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  On the ITOM AIOps configuration center page, under the Optimize section, select **Ignore alerts**.

    The Ignore alerts page is displayed.

    ![Alert automations page with option to create automation to enrich, group, or escalate and notify.](../image/automations-page-itom.png "Automations page")

4.  Select **Create automation**.

    ![Ignore automation creation page](../image/ignore-automation-creation-page.png)

5.  In the **Automation name** field, enter the name of the automation for ignoring alerts.

6.  Activate the automation by enabling the **Active** toggle switch.

7.  In the **If these conditions are met, don't add an alert in ServiceNow** section, set up filter criteria to identify the events you want to capture.

    1.  From the **Assignment group** field menu, select the assignment group to determine which team’s alerts trigger the automation.

        The **Assignment group** represents a specific team responsible for handling certain alerts. By selecting an assignment group, you ensure that only the alerts assigned to that a particular team trigger the automation. This way, the automation is targeted and only activates for relevant alerts associated with the selected team.

        **Note:**

        -   If you’re logged in to the instance with the administrator role \(evt\_mgmt\_admin\), all assignment groups are available. Additionally, you can also select **All groups** to generate alerts for any available group.
        -   If you’re an operator, only the group you’re a part of is available.
        -   Only members of the selected group or administrators can update or delete the automation.
    2.  From the **Source** field menu, select the monitoring tool from where the alert is generated.
    3.  Set up the conditions by selecting the field, operator, and field value. Then, add more conditions using OR or AND operators.

        To add another set of conditions, select **+ New condition set**. If you don’t see an additional info field, you can manually it in the drop-down list.

8.  To verify that you’re ignoring the correct events or to see examples of fields that can be used to set the conditions, select **Load past events**.

    You can preview the details of some past events.

9.  In the **Automation details** section, provide an order and automation description.

    ![Ignore automation details section.](../image/ignore-automation-details.png)

    1.  In the **Order** field, enter the automation order.

        **Note:** Automations run in order from the lowest to the highest.

        The **Automation is managed by** field displays the team or assignment group who owns, edits, and can delete this automation. The assignment group is the same as the one defined in the **If these conditions are met** section.

    2.  In the **Automation description** field, enter a brief description of the automation.
10. Select **Save automation**.

    A notification appears when the automation is successfully saved. Otherwise, an error message is displayed. The ignore automation that you created appears on the **Ignore alerts** page where you can view, edit, or delete the existing automation.


## What to do next

You can transform raw events into an understandable format by creating [Create Enrich automation](enrich-alert-sow-itom.md).

