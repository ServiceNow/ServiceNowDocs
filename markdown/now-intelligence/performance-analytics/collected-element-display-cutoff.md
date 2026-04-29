---
title: Collected scores and com.snc.pa.breakdown\_element\_cutoff
description: The elements of a breakdown that the Analytics Hub and KPI Details display for a selected date depend on the number of elements and the value of com.snc.pa.breakdown\_element\_cutoff.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Properties, Reference, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Collected scores and com.snc.pa.breakdown\_element\_cutoff

The elements of a breakdown that the Analytics Hub and KPI Details display for a selected date depend on the number of elements and the value of **com.snc.pa.breakdown\_element\_cutoff**.

In general, when the number of elements for a breakdown exceeds **com.snc.pa.breakdown\_element\_cutoff**, the Analytics Hub and KPI Details display only the elements that have ever had a score.

For a formula indicator, the elements that have ever had a score for all the contributing automated indicators are displayed. These scores do not need to be on the same date. The requirement is only that for each [contributing indicator](performance-analytics-glossary.md#), on some date, there was a score for the element.

For collected scores of an automated indicator—that is, for all scores other than real-time scores—there are two behaviors:

-   If the number of elements that have ever had a score is less than the limit set in **com.snc.pa.breakdown\_element\_cutoff**, all of these elements are listed for any selected date. Elements that do not have a score for the selected date are still listed for that date. This behavior is the same as the behavior for real-time scores.
-   If the number of elements that have ever had a score is greater than the limit set in **com.snc.pa.breakdown\_element\_cutoff**, only elements that have a score or a Change value for a selected date are listed for that date. Elements that do not have a score or Change value for that date are not listed regardless of whether they have a score for any other date.

**Tip:**

To prevent elements with null scores appearing in the Analytics Hub or KPI Details for automated indicators, consider setting a low value for **com.snc.pa.breakdown\_element\_cutoff**, such as 0 or 1. Elements with null scores may still appear however for real-time scores and formula indicators.

## Scores appearing for automated indicators with different values of com.snc.pa.breakdown\_element\_cutoff

This example uses KPI Details to explore the Assignment Group breakdown for the "Number of open incidents" indicator. The Assignment Group breakdown on the instance used in the example has just under 50 elements.

First is the default case, where **com.snc.pa.breakdown\_element\_cutoff**=50. This value is higher than the number of elements of Assignment Group. Therefore, for any selected date, all elements of the breakdown group are displayed.

![All elements of the Assignment Group breakdown being displayed.](../image/element-display-all.gif "All elements of Assignment Group shown in KPI Details")

The next case is where **com.snc.pa.breakdown\_element\_cutoff**=10. The number of elements in the Assignment Group breakdown far exceeds this value. However, only six elements have ever had a score. This number is less than the cutoff value of 10, so for any date, all six elements are shown, even when null.

![All elements of Assignment Group that ever had a score being displayed.](../image/element-display-all-ever-not-null.png "All elements shown that were never null")

Finally, there is the case where **com.snc.pa.breakdown\_element\_cutoff**=5. This number is less than the number of elements that have ever had a score. Now only the elements with a non-null value or a change value on the selected date are shown on that date. Different elements are thus shown for different dates. If there is a null value for the collection period after one with a value, a value of zero and a change symbol appears for that day.

![Scoresheet for Number of Open Incidents showing which null scores are shown as 0 with a change symbol and which are not shown at all.](../image/scoresheet-limited-breakdowns.png "Scoresheet for Number of Open Incidents showing which null scores are shown as 0 with a change icon and which are not shown at all")

On March 18, six elements are shown. The Hardware element, which has a null value, shows a value of 0 and a symbol that it declined.

![Assignment groups shown on March 18.](../image/element-display-mar-18.png "Assignment Group elements shown on March 18")

On March 19, five elements are shown. Hardware is not shown, because it has had a null value for two days running. The Network element, which now has a null value, shows a value of 0 and a symbol that it declined.

![Assignment Group elements shown on March 19.](../image/element-display-mar-19.png "Assignment Group elements shown on March 19")

On March 20, five different elements are shown. Network is not shown, because it has had a null value for two days running. The Openspace element, which now has a null value, shows a value of 0 and a symbol that it declined.

![Assignment Group elements shown on March 20](../image/element-display-mar-20.png "Assignment Group elements shown on March 20")

On March 21, five different elements are shown. Network now has a value and is shown. Openspace has had a null value for two days running, so is not shown.

![Assignment Groups shown on March 21.](../image/element-display-mar-21.png "Assignment Group elements shown on March 21")

On March 22, six elements are shown. Openspace now has a non-null value so is shown again.

![Assignment Group elements shown on March 22](../image/element-display-mar-22.png "Assignment Group elements shown on March 22")

**Parent Topic:**[Performance Analytics properties](../reference/pa-properties.md)

