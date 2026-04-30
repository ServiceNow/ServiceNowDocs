---
title: Analytics Dashboards
description: Analytics Dashboards provide a graphical way to view detailed information relating to findings, both pending and resolved, with the Scan Engine. The dashboards are role-based, allowing for persona-based views of information. They display  key metrics,  charts, and  trend analysis.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-08-28"
reading_time_minutes: 3
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Analytics Dashboards

Analytics Dashboards provide a graphical way to view detailed information relating to findings, both pending and resolved, with the Scan Engine. The dashboards are role-based, allowing for persona-based views of information. They display  key metrics,  charts, and  trend analysis.

Analytics Dashboards vary depending on your ServiceNow role. As each role has specific needs and responsibilities, the dashboard is tailored to provide relevant insights and metrics per role.

Each dashboard role has a correlative relationship with its corresponding dashboard view. Users will only be able to access dashboard views associated to the roles their account has been granted.

<table id="table_z2w_4vz_chc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Executive`sn_impact_common.Impact Executive`

</td><td>

Provides executives a high-level view of platform health and AI remediation impact. It focuses on strategic indicators such as technical debt, compliance risk, and overall cost and time savings from Platform Health fixes. The view is designed to help leadership understand business value and make informed decisions about investments and priorities without diving into technical details.

</td></tr><tr><td>

Platform Owner`sn_impact_common.Impact Platform Owner`

</td><td>

Provides visibility into scan results, remediation progress, and technical debt across instances. This view is designed for operational oversight. It helps owners manage risk, enforce governance, and ensure workflows are running efficiently.

</td></tr><tr><td>

Team Lead`sn_impact_common.Impact Development Team Lead`

</td><td>

Highlights assigned findings and team performance metrics. This view is centered on delivery and resource management. It helps team leads balance workloads, track progress, and keep remediation aligned with project timelines, ensuring smooth execution without disrupting other deliverables.

</td></tr><tr><td>

Developer`sn_impact_common.Impact Developer`

</td><td>

Provides hands-on, task-focused information such as developer assignments, detailed findings, and outstanding exception reasons. Developers can quickly act on issues, provide feedback, and streamline remediation work, reducing manual effort while maintaining code quality. 

</td></tr></tbody>
</table>## Accessing Analytics Dashboards

Access the Analytics Dashboards to view detailed information relating to Scan Engine findings, both pending and resolved.

Make sure you have been assigned the correct role for your persona.

Role required: Executive, Platform Owner, Team Lead, or Developer

1.  Navigate to **ALL** &gt; **Impact** &gt; **Platform Health** &gt; **Analytics Dashboard**.

    Your assigned role is listed at the top left, which determines which dashboard view you can access.

2.  If you have been assigned to more than one role, select which dashboard to view.

    The date listed is the last completed scan date to let you know whether the charts in the dashboard are up-to-date.​

    **Note:** All dashboard metrics fluctuate as the scan progresses and will stabilize once it completes.

3.  On the **Options** list, select one of the following:
    -   **Scan progress**: Display the full scan progress page for complete metrics of any currently running or previously run scan.
    -   **Property configuration**: Open the Scan Engine properties page.
4.  To sort and view a chart or table, select **Option**, and then select one of the following:
    -   **Cost**: Cost is calculated by multiplying the Average development rate \(configured in the Scan Engine properties\) by the estimated time to resolve the finding \(as set in the finding’s associated definition\).
    -   **Count**: The total number of findings.
    -   **Time**: Each definition includes an estimated time to resolve based on expert-driven recommendations. These estimates serve as practical guidelines to help teams estimate how long an issue should take to fix on average, promoting better planning and prioritization.
5.  Select a date range for trend chart data:
    -   Pre-defined range
    -   ​Custom  range: Select start and end dates. Enter  the start and end dates directly into the range textbox, then select **Apply**.

        **Note:** The amount of historical data stored and displayed in these metrics varies depending on the data restrictions associated with your Platform Analytics package.

6.  Select the download button to save a CSV or Excel file of the currently displayed data in a table.

    Blue text within table cells are hyperlinks to other modals or new tabs. Blue table column headers are sortable \(select the header to sort\). In sorted tables, the sorted column will have a small caret next to its name.


