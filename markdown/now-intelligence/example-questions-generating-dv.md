---
title: Guidelines and example questions
description: This section shows guidelines and some typical questions you could ask in the Now Assist panel to generate data visualizations.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Use Analytics Generation, Analytics Generation, Platform Analytics]
---

# Guidelines and example questions

This section shows guidelines and some typical questions you could ask in the Now Assist panel to generate data visualizations.

Follow these guidelines when asking Now Assist to generate a data visualization:

-   **Be precise in your questions**
    -   Use the correct term for the subject of the data you want, such as 'incident' or 'change request.' If you know the name of the table, include that name in the question.
    -   Be as detailed and precise in your conditions as possible. Do not say "all incidents not resolved in 30 days," say "all incidents that were still open 30 days after they were created."
    -   If you want a specific visualization type, say so.
-   **Experiment with questions**

    Save your questions somewhere, including any modified versions. Saving your questions enables easy comparison of results.


When you generate a data visualization, look it over carefully. Check whether it really shows you what you want to know. Keep refining your questions until you are satisfied.

**Note:** Data visualization generation uses the same engine as Analytics Q&amp;A. Therefore, for more information, see the question guidelines in [Analytics Q&amp;A](../../performance-analytics/concept/analytics-q-and-a.md).

## Examples

-   **Show me the number of open incidents by priority**

    Gives you a chart of records on the Incident table grouped according to the Priority column value.

-   **Show task sla as pie**

    Here you are asking for a pie chart of Task SLA records, but you have not specified the field by which to group the records. Now Assist gives you a list of fields to choose from, and then it shows you a pie chart based on your selection.

-   **Show unresolved problems where Assignment group is not empty**

    Gives you a list of records from the Problem \[problem\] table, filtered to show only records with a value in the Assignment group field.

-   **Show me the total number of tasks with high priority**

    Gives you a single score chart with the number of unique records \(Count Distinct aggregation\) on the Task table with a priority of 2 \(High\).

-   **Tasks created this month, grouped by priority**

    Gives you a bar chart of records on the Task table that were created this month, grouped by the value of the Priority field.


**Parent Topic:**[Use Analytics Generation](../task/use-dv-generation.md)

