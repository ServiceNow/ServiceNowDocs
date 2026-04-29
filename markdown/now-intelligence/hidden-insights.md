---
title: Extended analysis
description: Generate a deeper level of analysis that can reveal new insights, enabling you to make more informed decisions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Questions and responses in an exploration, Use, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Extended analysis

Generate a deeper level of analysis that can reveal new insights, enabling you to make more informed decisions.

Extended analysis involves aggregating the records related to a response in an exploration. It examines the same columns that you see when you view the list of records for the relevant table. It takes a Count of Choice, Reference, and Boolean columns. Therefore, you can influence extended analysis by selecting which fields to view in the relevant tables. The relevant tables include any related tables that Query Generation dot-walks to.

The number of columns that extended analysis examines is set in the system property **sn\_query\_gen.hidden\_insights.groupby.min\_fields**. The default value is 5. If the number of eligible columns that are visible on the record list is lower than this value, the system searches for more fields on the table. The search stops when the total number of fields from both the list view and the table search reaches the value of the system property. If the system can’t find that many fields, it uses the fields it does find.

The search for fields on the table follows this logic:

1.  The system searches for Choice fields on the table.
2.  If the count of located Choice fields and eligible columns on the record list is greater than the value of **sn\_query\_gen.hidden\_insights.groupby.min\_fields**, not all located Choice fields are selected. Instead, the system selects the Choice fields with the highest cardinality, to bring the total count of fields up to the value of the property. The search then stops.
3.  If the system can’t find enough Choice fields to bring the total count of fields up to the value of the property, the system selects the ones it finds, then looks for Reference fields. The same logic that was used for selecting Choice fields applies.
4.  If the system can’t find enough Reference fields to bring the total count of fields up to the value of the property, the system selects the ones it finds, then looks for Boolean fields. The same logic that was used for selecting Choice and Reference fields applies.
5.  Extended analysis insights are generated for however many Choice, Reference, and Boolean fields are found, up to the value of the property. If no fields are found, extended analysis isn’t performed.

While the results of extended analysis usually enrich the responses in an exploration, the analysis takes more time and uses more system resources than a standard analysis. You have to use your judgment on when to employ it.

Sometimes different questions or follow-up questions return the same extended analysis findings. Instead of repeating those findings as insights, the system digs deeper into the underlying reasons for the repetition. As a user, you have three benefits from this approach:

-   Every insight that is generated is unique.
-   You don't need to posit as many follow-up questions to get the insights you need, because the system drills down automatically, directing you to the interesting part of the data to focus on.
-   Results are faster, because extended analysis focuses on an increasingly specific subset of the data.

Extended analysis requires the analytics hidden insight skill from Query Generation to be active. For more information, see [Query Generation skills](../task/enable-query-generation.md).

To turn on extended analysis for an exploration, select it in the **Ask Now Assist a question about data** field. You have the same choice when you launch AI Data Explorer in a data visualization or list.

![Selecting extended or standard analysis.](../image/nowass-expl-extended-vs-standard-analysis.png)

## Standard vs. extended analysis

Consider the following request made in an exploration: "Analyze the incident creation trend over the past 12 months." Using standard analysis, you get the following insights: "Incident creation peaked in July 2025 with 2,441 incidents, while the lowest monthly count was 1,177 incidents in August 2025. The first half of the period \(September 2024 to February 2025\) saw monthly incident counts consistently above 1,700, but the final month dropped by more than 50% compared to the peak."

![Resulting insights from a standard analysis of the request to analyze the incident creation trend over the past 12 months.](../image/nowass-expl-std-analysis.png "Insights from standard analysis")

Making the same request with extended analysis, you get the same insight plus the following information:

-   Incident volume dropped 49.2% from 2,441 in July 2025 to 1,177 in August 2025, indicating a major shift.

-   The largest monthly increase was 28.3% in April 2025, with incidents rising by 512 to 2,321.

-   Incident counts show a consistent downward trend \(slope: -24.22\), which suggests an ongoing reduction in reported issues.

-   Monthly incident counts vary widely \(range: 1,264; standard deviation: 369.24\), indicating unstable operational demand.


![Resulting insights from an extended analysis of the request to analyze the incident creation trend over the past 12 months.](../image/nowass-explr-extd-analysis.png "Insights from extended analysis")

**Parent Topic:**[Questions and responses in an exploration](ask-expl-questions.md)

