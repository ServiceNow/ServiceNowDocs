---
title: View matrix report in landing page and record page of Audit Workspace
description: View the Matrix report in the Audit Workspace that presents the data in a structured format.
locale: en-US
release: xanadu
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2025-01-21"
reading_time_minutes: 2
breadcrumb: [Matrix report in Audit Workspace, Audit Workspace for the Auditor, Audit Workspace, Audit Management, Governance, Risk, and Compliance]
---

# View matrix report in landing page and record page of Audit Workspace

View the Matrix report in the Audit Workspace that presents the data in a structured format.

## Before you begin

Role required: sn\_audit\_ws.auditor

## About this task

As an admin you have completed the matrix report registry, relationship configuration, and column configurations. As a user you can see the report in the Audit Workspace.

The report helps to analyze relationships between different objects such as assessing risks and controls. You can assess and document risks and the internal controls designed to mitigate those risks through the Risk and Controls Matrix.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**.

2.  Select the matrix report icon \(![Matrix report icon.](../image/matrix-report-icon.png)\) and click the matrix report that you configured.

3.  For the landing page display type matrix configuration, you can view the Matrix report in the Audit Workspace.

4.  Select the view related information icon \(![View related information.](../image/view-related-info-icon.png)\) to get a complete tabular view of the matrix report.

    The source record details are displayed on the left pane for the top two orders. The target table fields that you configured are displayed as column heads on the right pane.

    ![Landing page display type of the Risk and Control Matrix report in the Audit Workspace.](../image/matrix-report-audit-workspace.png)

    Since risk is the base source table, all the risk-related fields are displayed on the left pane. Level 0 is the risk, which is the default base table. All the data that are fetched from the risk record are Level 1.

    For example, in the preceding illustration, for the **Loss of Availability** risk listed on the left pane you can view all the risk-related details that you configured from the target tables on the right pane. The control details that are retrieved from the Control table, the test plans for the control, the issues related to the control, and the issues related to the risk are all displayed in separate tabs that come from the configuration on the right pane.

    For the record page display type matrix configuration, you can view the matrix report in the List view of the Audit Workspace.

5.  Select the list icon \(![List icon](../image/ListsIcon.jpg)\) of the Audit Workspace.

6.  Select any record from the configured table of the Matrix report configuration.

    For example, if it’s an engagement record, then select the record from **All engagements** in the **Execution** list.

7.  Select the record from the list of records on the right pane.

    The **Overview** page of the selected record opens up.

8.  Select the **Matrix report** tab to view the report in the record page.

    ![Record page display type of Risk and Control Matrix report in the List view of the Audit Workspace.](../image/matrix-report-record-audit-ws.png)


