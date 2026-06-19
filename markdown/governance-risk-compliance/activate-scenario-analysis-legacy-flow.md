---
title: Enable the legacy scenario analysis flow
description: Complete admin procedure to activate the legacy scenario analysis flow \(sn\_oper\_res\_scenario\_analysis\) across the four entry-point surfaces in the Operational Resilience Workspace. Deactivate the advanced flow when you want to continue using the legacy scenario analysis flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/activate-scenario-analysis-legacy-flow.html
release: australia
topic_type: task
last_updated: "2026-05-14"
reading_time_minutes: 3
keywords: [Scenario Analysis, Operational Resilience, legacy flow, activate, sn\_oper\_res\_scenario\_analysis, entry points]
breadcrumb: [Legacy scenario analysis, Scenario analysis, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Enable the legacy scenario analysis flow

Complete admin procedure to activate the legacy scenario analysis flow \(sn\_oper\_res\_scenario\_analysis\) across the four entry-point surfaces in the Operational Resilience Workspace. Deactivate the advanced flow when you want to continue using the legacy scenario analysis flow.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

Complete each step in the order shown. Each step covers one of the four entry-point surfaces: List, Home Page Widget, Vertical Page Layout, and Dropdown. After you complete all four steps, the legacy scenario analysis flow is available to users in the Operational Resilience Workspace.

**Note:** Only one flow \(advanced or legacy\) must be active at a time on each surface. Complete all four steps described in this topic to fully switch to the legacy scenario analysis flow.

## Procedure

1.  To activate the legacy list, navigate to **System Definition** &gt; **sys\_ux\_list.list**.

    1.  Open the **Scenario analysis \(Legacy\)** record.

    2.  Select the **Active** check box.

        \[Omitted image "scenario-analysis-legacy-ux-list-record.png"\] Alt text: Active check box selected on the Scenario analysis \(legacy\) UX list record.

    3.  Find the All scenario analysis record \(points to \[sn\_oper\_res\_scenario\_analysis\_advance\]\) and clear **Active**.

    4.  Select **Update**.

        |UI Component|Description|
        |------------|-----------|
        |All scenario analysis|Active by default. Sources sn\_oper\_res\_scenario\_analysis\_advance.|
        |Scenario analysis \(Legacy\)|Inactive by default. Sources sn\_oper\_res\_scenario\_analysis.|

        The legacy list is available to users in the Operational Resilience Workspace.

        **Note:** The active list determines which table the Scenario Analyses list view sources records from. Only one list record should be active at a time.

2.  Complete the following steps to swap the Home page widget and reports.

    1.  Open the **Advanced Dashboards** in the UI Builder and open the **Operational Resilience** overview dashboard.

    2.  In the page tree, select **scenario\_analysis\_progress** and enable **Hide** to hide the widget.

    3.  Select **scenario\_analysis\_legacy\_progress** and clear **Hide** to display the legacy widget.

    4.  Select **Save**.

    5.  Navigate to **Platform Analytics &gt; Data visualizations** \(pa\_visualization\_list table\).

    6.  Activate the two legacy records: **Scenario analysis \(legacy\) in progress** and **Scenario analysis \(legacy\) completed**.

    7.  Set the two advanced report records \(**Scenario analysis in progress** and **Scenario analysis completed**\) to inactive.

        The Operational Resilience overview dashboard displays progress data for the legacy scenario analysis flow.

    The Data visualization report states are shown in the table.

    |Report|State|
    |------|-----|
    |Scenario analysis in progress|Active|
    |Scenario analysis completed|Active|
    |Scenario analysis \(legacy\) in progress|Inactive|
    |Scenario analysis \(legacy\) completed|Inactive|

    |UI Component|Description|
    |------------|-----------|
    |scenario\_analysis\_progress|Widget that displays progress data for the advanced scenario analysis flow. It is visible on the Operational Resilience Home page by default.|
    |Data visualization reports \(advanced flow\)|Two report records that source the **scenario\_analysis\_progress** widget. It is Active by default.|
    |scenario\_analysis\_legacy\_progress|Widget that displays progress data for the legacy scenario analysis flow. It is hidden on the Operational Resilience Home page by default.|
    |Data visualization reports \(legacy flow\)|Two report records that source the **scenario\_analysis\_legacy\_progress** widget. It is Inactive by default.|

    \[Omitted image "scenario-analysis-legacy-dashboard-uib.png"\] Alt text: Operational Resilience overview dashboard in UI Builder with the legacy progress widget unhidden.

3.  In the Vertical Page Layout entry point, swap the Program Activities related list shown on Business Service, Service, and Offering records.

    1.  Open the **Operational Resilience** &gt; **Admin** &gt; **Record View Configuration**.

    2.  Open the **Operational resilience workspace configuration** record.

    3.  In the Vertical Page Layout, locate the **Program Activities** related list for **Business Service**, **Service**, and **Offering**.

    4.  Find the related list that points to the **sn\_oper\_res\_scenario\_analysis\_advance** table and set to Inactive.

    5.  Activate the related list that points to the **sn\_oper\_res\_scenario\_analysis** table by setting it to Active.

        The Business Service, Service, and Offering records show the legacy Program Activities related list.

    \[Omitted image "scenario-analysis-program-activities-old-vs-new.png"\] Alt text: Service Offering record with the new Program Activities related list next to the legacy related list.

4.  Activate the legacy choice on the Operational vulnerability source field in the Drop-down entry point.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Choice Lists**.

    2.  Filter the list to **Table** = **sn\_oper\_res\_vulnerability** and **Element** = **source**.

    3.  Open the **Scenario analysis \(legacy\)** choice.

    4.  Select the **Active** check box.

    5.  Select **Update**.

        The **Scenario analysis \(legacy\)** choice is available in the **Source** drop-down on Operational vulnerability records.

    \[Omitted image "scenario-analysis-source-choice-list.png"\] Alt text: Choices list filtered to sn\_oper\_res\_vulnerability.source with the Scenario analysis \(legacy\) entry visible.


## Result

The legacy scenario analysis flow is active on all four entry-point surfaces in the Operational Resilience Workspace.

For information on creating a legacy scenario analysis, see [Create a legacy scenario analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-scenario-analysis-in-ws.md).

