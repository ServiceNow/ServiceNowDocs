---
title: Improvement opportunities examples
description: The finding definitions use cases are described below.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting improvement opportunities from Classic view, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Improvement opportunities examples

The finding definitions use cases are described below.

Use case 1a: Record bouncing between groups. Analysts often want to identify records that go from a particular group \(for example service desk\), then reassign to another group, and eventually resolved by the initial group again.![record bouncing between groups](../image/use-case-1.png)

In case the initial group is known, use the following finding rule: Message and category.

-   Start condition table config: incident
-   Start condition
    -   Name: group name, for example, Service Desk
    -   Condition type: Field/value condition
    -   Field = Assignment Group
    -   Predicate = Is
    -   Field value = Service Desk
    -   Occurrence\(s\) to match: first only

Relation: eventually followed by

-   End condition table config: incident
-   End condition
    -   Name: group name, for example Service Desk
    -   Condition type: Field/value condition
    -   Field=Assignment group
    -   Predicate= Is
    -   Field value = Service Desk
    -   Occurrence\(s\) to match: last only
    -   Track duration: true

Use case 1b: In case all bouncing records between groups with similar initial group must be identified, use the Message and category finding rule.

-   Start condition table config: incident
-   Start condition
    -   Name: Assignment group is anything
    -   Condition type: Field/value condition
    -   Field = Assignment group
    -   Predicate = Is anything
    -   Occurrence\(s\) to match: first only

Relation: eventually followed by

-   End condition table config: incident
-   End condition
    -   Name: Assignment group is anything
    -   Condition type: Field/value condition
    -   Field=Assignment group
    -   Predicate=Is anything
    -   Occurrence\(s\) to match: all
    -   Track duration: true
    -   Relation constraint: Has the same assignment group

Use case 2: SLA breach. Show all records that were in the state New, while the SLA breach happened.![SLA breach flow](../image/sla-breach-flow.png)

After you give the finding definition a message and category, specify the finding rule as follows.

-   Start condition table config: incident
-   Start condition
    -   Name=state
    -   Condition type: Field/value condition
    -   Field=State
    -   Predicate=Is
    -   Field value=New
    -   Occurrence\(s\) to match=first only
-   Contextual condition:
    -   Name=SLA breach
    -   Finding Def= Add the finding def message
    -   Condition type= Contextual field/value condition
    -   Field=Made SLA \(make sure you have Made SLA defined as activity definition in your project\)
    -   Predicate=is not
    -   Field value=true
-   Relation: directly followed by
-   End condition table config: incident
-   End condition
    -   Name: State
    -   Condition type: Field/value condition
    -   Field=State
    -   Predicate=is
    -   Field value=Work in progress
    -   Occurrence\(s\) to match=first only
-   Contextual condition:
    -   Name=SLA breach
    -   Condition type= Contextual field/value condition
    -   Field=Made SLA \(make sure you have Made SLA defined as activity definition in your project\)
    -   Predicate=is
    -   Field value=true
-   Track duration: true

![SLA breach](../image/sla-breach.png)

Use case 3: Longer than six hours between parent state Work in Progress and task creation. The resolution time or records often depends on the completion of one or more tasks. To improve the solution time of the main record, it’s therefore important to start the tasks as quickly as possible after the main records reached the Work in Progress state. In this example, the user wants to find all records where it took longer than six hours to create the underlying tasks after the main record went into Work in Progress. After giving the Finding definition a message and category, specify the finding rule as follows.

-   Start condition table config: Parent, for example incident
-   Start condition
    -   Name: First occurrence of Work in Progress
    -   Condition type: Field/value condition
    -   Field=State
    -   Predicate=Is
    -   Field value=Work in progress
    -   Occurrence\(s\) to match: first, only
        -   Relation: eventually followed by
        -   End condition table config: incident task
        -   End condition
            -   Name=incident task start
            -   Condition type=Process start
                -   Constraint: Minimum duration is 6 hours
                -   Track duration: true ![finding definition occurrence](../image/finding-condition-occurrence.png)

![finding rule specification](../image/finding-def-sequence.png)

**Parent Topic:**[Setting improvement opportunities from Classic view](impr-opp-classic-project.md)

