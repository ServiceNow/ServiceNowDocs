---
title: Edit a reliability metric
description: Update a reliability metric to keep it relevant and aligned with your team's goals.
locale: en-US
release: yokohama
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using SLO Management, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Edit a reliability metric

Update a reliability metric to keep it relevant and aligned with your team's goals.

## Before you begin

Role required: srm\_admin, srm\_manager, or srm\_responder

Updating reliability metrics, such as Service Level Objectives \(SLOs\) or Service Level Indicators \(SLIs\), during active measurement periods can result in graph inconsistencies.

## About this task

To help you manage reliability-metric history, Service Reliability Management \(SRM\) follows specific naming conventions. When you edit a reliability metric, SRM does the following:

-   Retires the existing SLO.
-   Creates a copy of the SLO with your edits in a draft state. You can either:
    -   Save the copy as a draft.
    -   Activate the copy.
-   Appends a number to the copy's name, for example, Uptime \(2\) or Uptime \(3\).
-   Displays all SLO versions in the **Reliability metrics** tab.

**Note:** In the **Reliability metrics** tab, SLO headers have two numbers, for example, HTTP response time \(2\) \(3\). The first number is its version. The second is the number of SLIs associated with the SLO.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  Follow these steps to access the **Reliability metrics** tab:

    1.  Select the **Services** page icon \(![services icon](../../service-reliability/image/icon-sr-services.png)\).

    2.  Select the service that uses the reliability metric you want to edit.

    3.  Select the **Reliability metrics** tab.

3.  To edit a reliability metric, select the relevant reliability metric, and then select **Edit** and **Continue to edit**.

4.  To save and implement your changes, select **Activate**.

    Your edited reliability metric appears in the **Reliability metrics** tab. SRM sets the state to running and includes a version number in its name, for example, Uptime \(3\).


## What to do next

Managing SLOs requires ongoing updates to make sure they reflect your reliability goals. You can edit or retire existing SLOs and, if needed, reactivate retired SLOs.

**Note:** If you reactivate a retired SLO, SRM creates and activates a new copy of it. For example: If there are two versions of an SLO, Uptime \(1\) and Uptime \(2\), and you reactivate Uptime \(1\), SRM leaves it in the retired state and creates an active version called Uptime \(3\).

**Parent Topic:**[Using SLO Management](using-service-level-objective-management.md)

