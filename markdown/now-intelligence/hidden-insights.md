---
title: Extended analysis
description: Generate a deeper level of analysis that can reveal new insights, enabling you to make more informed decisions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/hidden-insights.html
release: zurich
topic_type: concept
last_updated: "2025-09-16"
reading_time_minutes: 8
breadcrumb: [Questions and responses in an exploration, Use, AI Data Explorer, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# Extended analysis

Generate a deeper level of analysis that can reveal new insights, enabling you to make more informed decisions.

Extended analysis requires the analytics hidden insight skill from Query Generation to be active. For more information, see [Query Generation skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/enable-query-generation.md).

To turn on extended analysis for an exploration, select it in the **Ask Now Assist a question about data** field. You have the same choice when you launch AI Data Explorer in a data visualization or list.

\[Omitted image "nowass-expl-extended-vs-standard-analysis.png"\] Alt text: Selecting extended or standard analysis.

While the results of extended analysis usually enrich the responses in an exploration, the analysis takes more time and uses more system resources than a standard analysis. You have to use your judgment on when to employ it.

## Extended analysis of indicators

When you view an indicator, Extended analysis automatically analyzes the following data:

-   **Breakdown distributions**

    How indicator values are distributed across dimensions such as Priority, Category, and Status

-   **Cross-dimensional correlations**

    Relationships between breakdowns, such as how Priority correlates with Category

-   **Temporal trends**

    How the indicator has changed over timeand whether this change is in the desired direction

-   **Prior-period comparisons**

    How current performance compares to a previous period

-   **Target status**

    Current target value, difference between current score and target value, and the likely impact of this gap


In the response, Extended analysis provides a formatted summary that includes the following information:

-   Overall score for the current view
-   Distribution breakdowns showing individual values and their counts \(for example, "Critical: 42 incidents"\) and the percentage of total for each value \(for example, "35% of total"\)
-   Cross-dimensional analysis \(for example, "Critical + Software: 18 incidents, 43% of Priority=Critical"\)
-   Temporal trend table showing historical scores by period \(monthly, daily, and so on\) and period-to-period changes

The data that Extended analysis returns also depends on the breakdowns and Group By values that are applied in the data visualization in the response.

|Current view|Data returned|
|------------|-------------|
|No breakdown or grouping \(overall view of indicator\)|All breakdowns for the indicator that have values, along with their distributions and temporal trends|
|Grouped by one breakdown \(for example, grouped by Priority\)|The current grouping, other available breakdowns cross-tabulated with it, and their temporal trends|
|Filtered to a specific element \(for example, Priority = High\)|The filtered view, the same element across all instances, the overall baseline for comparison, and temporal trend|

Extended analysis also automatically expands the time window to provide broader context. For example, if you are viewing the last 3 months, it analyzes 6 months to show a prior-period comparison. The analysis stops expanding at 2 breakdowns to keep results focused.

Breakdowns are returned in the following priority order:

1.  Currently applied breakdowns \(what you are already viewing\)
2.  Top 50 distinct values per breakdown, ranked by score \(highest values first\)
3.  Cross-dimensional combinations — breakdowns are paired to show correlations with the current view
4.  Other available breakdowns, if the data budget allows

**Note:** The default limit is top 50 values per breakdown, sorted by score in descending order. This limit is configurable.

## Extended analysis of table data

For table data,[Extended analysis]() involves aggregating the records related to a response in an [exploration](). It examines the same columns that you see when you view the list of records for the relevant table. It takes a Count of Choice, Reference, Glide List, and Boolean columns. Therefore, you can influence extended analysis by selecting which fields to view in the relevant tables. The relevant tables include any related tables that Query Generation dot-walks to.

The number of columns that extended analysis examines is set in the system property **sn\_query\_gen.hidden\_insights.groupby.min\_fields**. The default value is 5. If the number of eligible columns that are visible on the record list is lower than this value, the system searches for more fields on the table. The search stops when the total number of fields from both the list view and the table search reaches the value of the system property. If the system can’t find that many fields, it uses the fields it does find.

The search for fields on the table follows this logic:

1.  The system searches for Choice fields on the table.
2.  If the count of located Choice fields and eligible columns on the record list is greater than the value of **sn\_query\_gen.hidden\_insights.groupby.min\_fields**, not all located Choice fields are selected. Instead, the system selects the Choice fields with the highest cardinality, to bring the total count of fields up to the value of the property. The search then stops.
3.  Sometimes the system can’t find enough Choice fields to bring the total count of fields up to the value of the property. In this case, the system first selects the ones it finds. Then it looks for Reference fields. The same logic that was used for selecting Choice fields applies.
4.  Sometimes the system can’t find enough Reference fields to bring the total count of fields up to the value of the property. In this case, the system first selects the ones it finds. Then it looks for Boolean fields. The same logic that was used for selecting Choice and Reference fields applies.
5.  Extended analysis insights are generated for however many Choice, Reference, and Boolean fields are found, up to the value of the property. If no fields are found, extended analysis isn’t performed.

Sometimes different questions or follow-up questions return the same extended analysis findings. For table data, instead of repeating those findings as insights, the system digs deeper into the underlying reasons for the repetition. As a user, you have three benefits from this approach:

-   Every insight that is generated is unique.
-   You don't need to posit as many follow-up questions to get the insights you need. The system drills down automatically, directing you to the interesting part of the data to focus on.
-   Results are faster, because extended analysis focuses on an increasingly specific subset of the data.

## Standard vs. extended analysis of table data

Consider the following request made in an exploration: "Analyze the incident creation trend over the past 12 months." Using standard analysis, you get the following insights: `Incident creation peaked in July 2025 with 2,441 incidents, while the lowest monthly count was 1,177 incidents in August 2025. The first half of the period (September 2024 to February 2025) saw monthly incident counts consistently above 1,700, but the final month dropped by more than 50% compared to the peak.`

\[Omitted image "nowass-expl-std-analysis.png"\] Alt text: Resulting insights from a standard analysis of the request to analyze the incident creation trend over the past 12 months.

Making the same request with extended analysis, you get the same insight plus the following information:

-   Incident volume dropped 49.2% from 2,441 in July 2025 to 1,177 in August 2025, indicating a major shift.

-   The largest monthly increase was 28.3% in April 2025, with incidents rising by 512 to 2,321.

-   Incident counts show a consistent downward trend \(slope: -24.22\), which suggests an ongoing reduction in reported issues.

-   Monthly incident counts vary widely \(range: 1,264; standard deviation: 369.24\), indicating unstable operational demand.


\[Omitted image "nowass-explr-extd-analysis.png"\] Alt text: Resulting insights from an extended analysis of the request to analyze the incident creation trend over the past 12 months.

## Standard vs extended analysis of indicator scores

Consider the following request in an exploration: "How many open incidents with Critical priority have there been over the last three months, grouped by category?" Using standard analysis, you get the following insights: `Based on data collected through July 8, 2026, Hardware had the most open critical incidents at 26, far ahead of Inquiry / Help at 6 and Network at 5. Hardware accounts for about 62% of the 42 open critical incidents shown, while the top three categories together make up about 88% of the total.` This answer addresses only what was directly asked in the question.

\[Omitted image "ext-insights-std-indicator.png"\] Alt text: Standard analysis of indicator scores.

Making the same request with extended analysis, you get the same insight plus the following information, along with suggested actions to take:

-   Hardware drives the backlog with **62% \(26/42\)** of open incidents, over **4x** Inquiry / Help at **14% \(6/42\)**; prioritize hardware-specific resolution capacity.

-   Lower-severity work dominates open incidents: **65% \(653/1006\)** are Planning, while only **4% \(45/1006\)** are Critical; separate queues to prevent routine work delaying urgent response.

-   High-urgency exposure remains material: **16% \(161/1006\)** of open incidents are High or Critical, indicating meaningful operational risk; accelerate escalation and aging reviews.

-   Category concentration is extreme: the top two categories, Hardware and Inquiry / Help, account for **76% \(32/42\)** of open incidents; focus root-cause reduction there first.

-   Cloud Management is a clear low-volume outlier at **2% \(1/42\)** of category incidents versus Hardware’s **62% \(26/42\)**; review whether demand is genuinely low or underreported.


\[Omitted image "ext-insights-extended.png"\] Alt text: Extended analysis of indicator scores.

If a target is set on the indicator, extended analysis can return the target value and the gap between that target and the latest score. Consider the following request: "Number of open incidents over the last 9 months, based on indicator score, and compared to target, including target gaps." In reply, you get a basic description of the trends in the returned time series data visualization and the following additional insights on the target gap: "Open incidents climbed from 2 on October 10, 2025 to 1,214 by July 9, 2026, far above the 300 target; launch backlog-reduction immediately."

\[Omitted image "ext-insights-extended-target.png"\] Alt text: Extended analysis of indicator scores including target gap.

**Tip:** Sometimes making it explicit that you want indicator data including target gap helps make sure that data is in the response.

**Parent Topic:**[Questions and responses in an exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/ask-expl-questions.md)

