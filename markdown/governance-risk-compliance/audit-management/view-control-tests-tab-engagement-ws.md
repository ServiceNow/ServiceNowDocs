---
title: View control tests in a grid on an engagement
description: Use the Control tests tab on an engagement record to view, manage, and request evidence for all control tests in a single grid.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/view-control-tests-tab-engagement-ws.html
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 3
breadcrumb: [Audit Task Management, Audit Supervisor Workspace, Audit Workspace Overview, Audit Management, Governance, Risk, and Compliance]
---

# View control tests in a grid on an engagement

Use the Control tests tab on an engagement record to view, manage, and request evidence for all control tests in a single grid.

## Before you begin

Role required: sn\_audit.manager, sn\_audit\_ws.supervisor

## About this task

The Control tests tab lists every control test associated with the engagement in a single view, so you don't need to open each control test record individually. The tab offers two view options:

-   List view \(default\): Displays control tests in a simple list format with key details
-   Hierarchical view: Displays control tests and their associated test steps in a hierarchical view. You can edit some fields on the control test records. When you select the hierarchical view, you can switch to the grid view.

Both views show control test details including number, name, assigned auditor, design effectiveness, design results, operating effectiveness, and operational results. You can personalize columns to show additional fields such as Reference and Implementation Statement.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**, and open an engagement record.

2.  Select the **Control tests** tab.

    The list shows each control test's number, name, status, assigned auditor, design effectiveness, operating effectiveness, and results.

    \[Omitted image "ct-list-view.png"\] Alt text: List view.

3.  Use **New**, **Delete**, and **Refresh** to manage rows.

    If a control test has related Assessment procedures, selecting **Delete** displays a confirmation that lists the related records that will also be deleted.

4.  Switch to the Hierarchical view to see control tests organized in a hierarchical view.

    The Hierarchical view displays control tests and their associated test steps in a hierarchical manner. This allows you to:

    -   View test step details without opening individual control test records
    -   See the relationship between control tests and their test steps
    -   Edit applicable fields \(Design effectiveness, Operating effectiveness, Design results, and Operational results\) directly in the hierarchical view
    -   Access additional columns such as Reference and State
    \[Omitted image "h-view-test-steps.png"\] Alt text: Hierarchical view with Test steps.

    The list displays the following columns by default:

    -   Control test: Unique identifier and control test name
    -   Design Test: Design Effectiveness and Design results
    -   Operational Test: Operating Effectiveness and Operational results
    -   Test steps: Number and step details. Note: Design results and Operational results are editable only by the user assigned to the control test. All other fields are view-only from the grid.
    To show or hide additional columns, complete the steps:

    1.  Select the menu icon \(⋮\) in a column header.
    2.  Select Personalize columns.
    3.  Use Search columns to find specific fields.
    4.  Check or clear columns to display or hide them.
    Available columns include Reference, Implementation Statement, and others.

5.  Select **Request evidence** on a row to request evidence for that control test directly from the grid.

    This enables efficient evidence collection across multiple control tests.

    Editable fields: Design effectiveness, Operating effectiveness, Design results, and Operational results are editable only by the user assigned to the control test.

    Inline editing in Hierarchical view: In the Hierarchical view, you can edit applicable fields directly in the hierarchical view without navigating to individual control test records. This capability makes it more efficient to manage multiple control tests and their test steps.


**Related topics**  


[Create a control test from an engagement in Audit Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/create-control-test-engagement-ws.md)

[Create a control test from an engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/t_CreateControlTest.md)

