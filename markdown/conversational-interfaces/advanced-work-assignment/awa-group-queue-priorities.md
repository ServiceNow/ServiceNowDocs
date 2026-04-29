---
title: AWA group queue priorities
description: Use the group queue priority feature to set a queue or work item preference for a given group of agents. For a given group or agent with limited capacity, this feature controls which queues should be preferred if matching work items are found in both.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# AWA group queue priorities

Use the group queue priority feature to set a queue or work item preference for a given group of agents. For a given group or agent with limited capacity, this feature controls which queues should be preferred if matching work items are found in both.

For each group defined across the eligibility pools for a given queue, a corresponding group queue priority record will automatically be created for that group and queue combination, with the order set to a default of 100.

## Example

The admin has configured two AWA queues: chat queue and P1 chat queue.

-   Chat queue has one eligibility pool with two groups: Spanish agent group and English agent group.
-   P1 chat queue has one eligibility pool with one group: English agent group.

The admin creates three group queue priority records, each with the default order of 100:

|Group|Queue|Order|
|-----|-----|-----|
|Spanish agent group|Chat queue|100|
|English agent group|Chat queue|100|
|English agent group|P1 chat queue|100|

Since both group queue priority records for the English agent groups have the same order of 100, work items across both queues are equally considered during assignment.

If the admin then changes the order of one of the group queue priority records to 200:

|Group|Queue|Order|
|-----|-----|-----|
|Spanish agent group|Chat queue|100|
|English agent group|Chat queue|200|
|English agent group|P1 chat queue|100|

The English agent group now has a group queue priority hierarchy of two levels:

1.  Level 1: Work items in the P1 chat queue
2.  Level 2: Work items in the chat queue

With the above hierarchy, agents in the English agent group will prefer work items in the P1 chat queue over the chat queue. The assignment engine will try to assign all work items under the P1 chat queue to the English agent group, before trying to assign any work items under chat queue to that same group \(assuming some agents still have free capacity\).

## Group queue priority processing: tiers

AWA uses tiers as a series of assignment rounds. In each round, AWA expands the pool of eligible agents based on group queue priority tiers. Each tier represents a set of groups at the same level and indicates how those groups prioritize a queue relative to other queues they qualify for.

|Group|Queue|Order|
|-----|-----|-----|
|Spanish agent group|Chat queue|100|
|English agent group|Chat queue|200|
|English agent group|P1 chat queue|100|

For the above group queue priority configuration, the tiers are organized as follows:

1.  Tier 1:
    1.  Consider English agent group for P1 chat queue
    2.  Consider Spanish agent group for chat queue
2.  Tier 2: Consider English agent group for chat queue

The ordering within each tier is negligible since all work items across queues in the same tier are equally considered.

The above tier ordering translates into the following rounds of assignment:

1.  Assignment run \#1
    1.  Assign work items in P1 chat queue, with agents from English agent group
    2.  Assign work items in chat queue, with agents from Spanish agent group
2.  Assignment run \#2: Assign work items in chat queue, with agents from English agent group

## Side effect of tier organization

A side effect of the tier setup is that the Spanish agent group may receive more work items under the chat queue, since they will be considered earlier during the first run of assignment. Since agents from English agent group may have been assigned work items in the P1 chat queue in the first assignment run, they will have less capacity to handle work items assigned in the second assignment run. Both factors influence the likelihood of groups in later tiers in receiving work items.

These side effects are important as this implies that the group queue priority setup hierarchy across different groups could also affect the distribution of work items within a queue.

Consider a more complex scenario where three groups are all eligible for three different queues, with the following group queue priority setup:

|Group|Queue|Order|
|-----|-----|-----|
|1|A|10|
|1|B|20|
|1|C|30|
|2|A|300|
|2|B|100|
|2|C|200|
|3|A|2|
|3|B|3|
|3|C|1|

The assignment process is organized into three tiers, since the maximum hierarchy across all three groups is three levels. There will be three runs of assignment:

1.  Assignment Run \#1
    1.  Queue A, with agents from group 1
    2.  Queue B, with agents from group 2
    3.  Queue C, with agents from group 3
2.  Assignment Run \#2
    1.  Queue A, with agents from group 3
    2.  Queue B, with agents from group 1
    3.  Queue C, with agents from group 2
3.  Assignment Run \#3
    1.  Queue A, with agents from group 2
    2.  Queue B, with agents from group 3
    3.  Queue C, with agents from group 1

If each group has one agent having capacity 2, where agent 1 is in group 1, agent 2 is in group 2, and agent 3 is in group 3, then assignments are made in the following manner:

<table id="table_ebx_41z_23c"><thead><tr><th>

Scenario

</th><th>

Outcome

</th></tr></thead><tbody><tr><td>

2 work items in each queue

</td><td>

-   Agent 1 gets two items from Queue A
-   Agent 2 gets two items from Queue B
-   Agent 3 gets two items from Queue C

</td></tr><tr><td>

3 items in Queue A and 3 items in Queue B

</td><td>

-   Agent 1 gets two items from Queue A
-   Agent 2 gets two items from Queue B
-   Agent 3 gets the last item from Queue A
-   Agent 1 gets the last item from Queue B

</td></tr><tr><td>

6 items only in Queue C

</td><td>

-   Agent 3 gets the first two items from Queue C
-   Agent 2 gets the next two items from Queue C
-   Agent 1 gets the last two items from Queue C

</td></tr></tbody>
</table>