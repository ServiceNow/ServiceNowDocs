---
title: Health Assessment Dashboard
description: View detailed Health Assessment results closer collaboration with the Impact squad to prioritize, review, and address best practice platform health findings.​
locale: en-US
release: australia
product: Impact Health Assessment
classification: impact-health-assessment
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [HealthScan tech KPIs, HealthScan, Platform Health, Using Impact, Impact]
---

# Health Assessment Dashboard

View detailed Health Assessment results closer collaboration with the Impact squad to prioritize, review, and address best practice platform health findings.​

The Health Assessment displays the total number of findings and comparisons against a previous scan. The assessment report addresses the findings across five categories and also the total of the categories.

Navigate to **Impact** &gt; **Platform Health** &gt; **Diagnose**.

View the report by:

-   Total findings: All detailed findings and the counts, comparison against previous scan, and live areas to take action
-   Health Score %: Shows the increase or decrease in statistical score percentage since the previous scan
-   Total findings by products: Breaks the scan findings by specific application on the instance, per category.

<table id="table_i3v_ydw_cbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Category

</td><td>

Each tile depicts an assessment category:-   Overall
-   Manageability
-   Performance
-   Security
-   Upgradeability
-   User Experience

**Note:** Hover over the **i** icon for descriptions.

</td></tr><tr><td>

Current total

</td><td>

The focused number is the total number of best practice violations from the most recent HealthScan.

</td></tr><tr><td>

Previous total

</td><td>

The number with the up or down arrow indicator represents the total number of best practice violations differences from the previous HealthScan for comparison.

</td></tr><tr><td>

Act

</td><td>

Highly recommended to address these findings, generally severity 1 priority issues.

</td></tr><tr><td>

Recommended

</td><td>

Recommended to address these findings next. These are generally a severity 2 priority.

</td></tr><tr><td>

Discuss

</td><td>

Findings that can make improvements, but are not a critical severity.

</td></tr></tbody>
</table>## Views

Select to view the assessment by summary view or list view. Toggle to the list view to show the individual findings records logged from the selected scan.

![Health Assessment Summary View](../image/health-assmt-summary.png "Summary View")

Summary view shows the total of the findings and the breakdown of findings for each category. By default, the Summary View is selected, displaying the assessment information in tiles.

![Shows the Health Assessment dashboard in summary view.](../image/health-assessment-report.png)

![List view.](../image/health-list-view.png "List View")

List view displays the list of individual findings that were logged during a particular scan.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Finding

</td><td>

The unique identifier of the finding record

</td></tr><tr><td>

Short description

</td><td>

The actual issue that was found during the scan

</td></tr><tr><td>

Definition \#

</td><td>

Technical reference number that is searched for during a scan

</td></tr><tr><td>

Details

</td><td>

Provides additional context of the violation occurrence

</td></tr><tr><td>

Occurrences

</td><td>

The total number of occurrences, where the same type of violation can occur across multiple tables and multiple fields**Note:** The occurrences hyperlink will direct you to the instance for access to address the issue.

</td></tr><tr><td>

Best action

</td><td>

Link to KB articles or product documentation regarding how to address the finding

</td></tr></tbody>
</table>![Shows all finding in List view.](../image/health-list-view.png)

**Note:** This feature is available in Impact Guided, Advanced, and Total packages.

