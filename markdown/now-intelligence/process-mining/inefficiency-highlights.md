---
title: Process inefficiency highlights
description: After identifying the areas that cause the inefficiency, you need to know what exactly the issue is and how to fix it. To do this manually is very time-consuming. The process inefficiency highlights provide the insight into the exact issues for the identified improvement opportunities.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-09-03"
reading_time_minutes: 3
breadcrumb: [Opportunity details page, Process details page, Process Mining workspace, Exploring Process Mining, Process Mining, Platform Analytics]
---

# Process inefficiency highlights

After identifying the areas that cause the inefficiency, you need to know what exactly the issue is and how to fix it. To do this manually is very time-consuming. The process inefficiency highlights provide the insight into the exact issues for the identified improvement opportunities.

The highlights are displayed after identifying the records that show the inefficiency and comparing it with the records that do not show the inefficiency.

For example, if a project has 100 records, the records matching the improvement opportunity are identified. For this example, let us consider that 20 records match the improvement opportunity. Now, each of the 12 metrics is compared for these 20 records with that of the remaining 80 records.

<table id="table_jwj_3nm_ngc"><thead><tr><th>

Metrics

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Process variability

</td><td>

Determines whether there are any exceptional number of different resolution paths in the process. The group of records that include the inefficient process pattern is compared with one of the group of records that doesn’t include the inefficient process pattern.

</td></tr><tr><td>

Mean Time to Completion \(MTTC\)

</td><td>

Determines whether the process has any extreme outliers in resolution times. The duration of the resolution time is compared with the threshold resolution time. The group of records that include the inefficient process pattern is compared with one of the group of records that doesn’t include the inefficient process pattern.

</td></tr><tr><td>

Time To Completion \(TTC\) standard deviation

</td><td>

Determines the TTC standard deviation of the group of records that include the inefficient process pattern and compares it with one of the group of records that doesn’t include the inefficient process pattern.

</td></tr><tr><td>

Mean step duration

</td><td>

Determines whether there are any steps in the process that take extremely long time \(for example, if a step has taken longer than a predetermined time threshold\).

</td></tr><tr><td>

Mean responsibility resolution

</td><td>

Determines the difference in responsibility time between provider, requester, and an external process.For example, when the state is “New,” it means that the process is on the provider, who has the assignment responsibility. If the state is “Awaiting user information,” the responsibility is on the requester. If the laptop at issue is sourced by an external vendor, then it’s an external process responsibility.

The responsibility time that has been taken by each of the provider, requester, and an external process is compared with the group of records that does not include the inefficient process pattern.

</td></tr><tr><td>

Mean idle time

</td><td>

Determines whether the process includes a high level of idle time. For example, when a record stays with an assignment group without being assigned to an agent. It’s highlighted when the idle time differs largely for the group of records that include the inefficient process pattern compared to the group of records that doesn’t include the inefficient process pattern.

</td></tr><tr><td>

Touch points

</td><td>

Determines whether the process had a very large number of manual tasks causing the delay. If a lot of people or groups were involved, this may have caused the delay and inefficiency. The number of touch points for the group of records that have an inefficient process pattern is compared with the number of touch points for the group of records that don’t include the inefficient process pattern.

</td></tr><tr><td>

Over-represented activities

</td><td>

Determines whether there are any steps that are frequently occurring compared to the process without this inefficiency.

</td></tr><tr><td>

Under-represented activities

</td><td>

Determines if a step has been skipped or missed compared to the regular process. For example, if the process includes an inefficient process pattern and the “approval” step is under-represented \(that is, the “approval” step is skipped frequently\), then the under-represented step that has caused the inefficient process pattern is identified.

</td></tr><tr><td>

Reassignments

</td><td>

Determines whether there are two or more than two reassignments in the inefficient process pattern compared to the records that don’t have this pattern.

</td></tr><tr><td>

Over-represented breakdowns

</td><td>

Determines if there’s any breakdowns slowing down the process.

</td></tr><tr><td>

Service-level agreement \(SLA\) breach rate

</td><td>

Determines if there’s a high probability for SLA breach to occur in the inefficient process pattern compared to the records that don’t have this pattern.

</td></tr></tbody>
</table>**Parent Topic:**[Opportunity details page](opportunity-details.md)

