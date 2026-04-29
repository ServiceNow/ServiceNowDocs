---
title: Trigger bulk remediation from Insights
description: Trigger a remedial action on multiple devices simultaneously from the Insights page.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitor, Digital End-User Experience, IT Service Management]
---

# Trigger bulk remediation from Insights

Trigger a remedial action on multiple devices simultaneously from the Insights page.

## About this task

Trigger remedial actions on a single device or multiple devices simultaneously from the **Insights** page. You can perform the following functions.

-   Filter devices by operating system or by remedial action status within a selected time range.
-   View available remedial actions.
-   Select an action from the Action Library.
-   Monitor the execution status from the playbook experience.

Filtering devices by operating system before selecting them ensures that only compatible devices are included.

Bulk remediation enables you to trigger a remedial action on multiple devices at the same time. DEX already supports bulk remediation for alerts. Bulk remediation from insights extends this capability to all insights pages, including Query Builder. You can initiate bulk remediation from any insights page such as Battery health, File management, System performance, and others.

## Before you begin

Role required: sn\_dex.admin, sn\_dex.engineer

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation pane, select **Insights****&gt; Battery health**.

3.  Filter the devices by operating system and apply the filter.

    **Note:** All devices must use the same operating system to trigger bulk remediation. Selecting the operating system filter is required on all insights pages except Windows Registry and File Management, which are Windows only.

4.  In the filter bar, select **Operating system** and select **Apply**.

    You can also filter by Remedial Action, Operator, and Timeframe. For example, to check whether the same action was already run on devices within the last 24 hours, select a timeframe. These filters are optional.

5.  Select one or more devices, then select **View remedial actions**.

    The Action Library opens, displaying available remedial actions for the selected operating system. Run remediation on a single device by selecting the device. To run bulk remediation, select multiple devices.

    **Note:** You can also select the action library icon \(![](../image/icon-action-library.png)\) on the screen to access the remedial actions.

6.  Select the remedial action and select **Run action**.

    **Note:** You can trigger a remedial action on a maximum of 1000 devices at a time.

7.  Review the skipped devices and select **Submit**.

    **Note:** Devices that don't meet the requirements for the selected action are listed as skipped. Review the list before submitting the action.


## Result

The playbook experience opens. In the **Current** tab, the action appears as in-progress. Select **View List** to see the status of the action on each device.

-   You can select View all to view all the remedial action executions.
-   The content playbook displays current actions and execution history. The History tab lists all the details.
-   The Device list on each card provides the details of the remedial action execution. It lists all successful, failed, and cancelled remedial actions.
-   The **Failed** tab lists the errors in different categories \(Business, Configuration, Technical, and others\).
-   The **Retry action** option is available only for the devices that failed due to Business error.

|Error category|Description|
|--------------|-----------|
|Business|Failures caused by invalid input, unsupported resource types, or unavailable required resources.|
|Configuration|Failures caused by missing or incomplete configuration on the endpoint or at the system level, such as a non-configured sudo setting.|
|Technical|Failures caused by unexpected code-level issues that aren't related to configuration.|
|Others|All the other generic errors categorized under others.|

To view all remedial action executions, access **DEX Administration** &gt; **Remedial Action Executions**. The administration view shows all in-progress or completed remedial actions.

