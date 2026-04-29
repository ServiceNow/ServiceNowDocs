---
title: Edit a reliability metric
description: Update a reliability metric to keep it relevant and aligned with your team's goals.
locale: en-US
release: australia
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using SLO Management, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Edit a reliability metric

Update a reliability metric to keep it relevant and aligned with your team's goals.

## Before you begin

Updating reliability metrics, such as Service Level Objectives \(SLOs\) or Service Level Indicators \(SLIs\), during active measurement periods can result in graph inconsistencies.

Role required: srm\_admin, srm\_manager, or srm\_responder

## About this task

To help you manage reliability-metric history, Service Reliability Management \(SRM\) follows specific naming conventions. When you edit a reliability metric, SRM does the following:

-   Retires the existing SLO.
-   Creates a copy of the SLO with your edits in a draft state, which you can either save as a draft or activate.
-   Appends a number to the copy name, for example, Uptime \(2\) or Uptime \(3\).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Follow these steps to access the **Reliability metrics** tab:

    1.  Select the **Services** page icon \(![services icon](../../service-reliability/image/icon-sr-services.png)\).

    2.  Select the service that uses the reliability metric you want to edit.

    3.  Select the **Reliability metrics** tab.

3.  To edit a reliability metric, select the relevant reliability metric, and then select **Edit** and **Continue to edit**.

4.  Make your changes in the Details, Service level indicators, or Error budget policies tabs.

    **Note:** If you change the SLI data source, all existing SLIs for the SLO are removed and you must create new ones. An SLO can use only one data source type, and each data source has unique settings that can’t be preserved or automatically converted.

    While you can’t recover the removed SLIs while editing the SLO, you can view the earlier versions in the Reliability metrics tab.

5.  To save and implement your changes, select **Activate**.

    Your edited reliability metric appears in the Reliability metrics tab. SRM sets the state to running and includes a version number in its name, for example, Uptime \(3\).

    The Activity panel on the Details tab records changes, providing a history of updates to the reliability metric.


## What to do next

Managing SLOs requires ongoing updates to make sure that they reflect your reliability goals. You can edit or retire existing SLOs and, if needed, reactivate retired SLOs.

**Note:** If you reactivate a retired SLO, SRM creates and activates a new copy of it. For example: If there are two versions of an SLO, Uptime \(1\) and Uptime \(2\), and you reactivate Uptime \(1\), SRM creates an active version called Uptime \(3\).

**Parent Topic:**[Using SLO Management](using-service-level-objective-management.md)

