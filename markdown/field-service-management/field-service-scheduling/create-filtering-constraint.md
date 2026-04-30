---
title: Create a filter constraint or a ranking criteria for a task recommendation policy
description: Define a filtering constraints or a ranking criteria for a task recommendation policy. Filter the best matched tasks for the agent based on the filter ordering rules.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create Task Recommendation Policies, Set up Intelligent Task Recommendations, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create a filter constraint or a ranking criteria for a task recommendation policy

Define a filtering constraints or a ranking criteria for a task recommendation policy. Filter the best matched tasks for the agent based on the filter ordering rules.

## Before you begin

Role required: admin, wm\_admin

## Procedure

1.  Navigate to **Field Service** &gt; **Task Recommendation Administration** &gt; **Task Recommendation Policies**.

2.  Open a policy from the list.

3.  To create either a filter constraint or a ranking criteria, do one of the following:

    -   To create a filter constraint, click **New** in the Filtering Constraints related list.
    -   To create a rating criteria, click **New** in the Ranking Criteria related list.
4.  On the form, fill in the fields.

<table id="table_bfh_tx2_cqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Task recommendation policy

</td><td>

Name of the task recommendation policy for which you are defining the criteria.

</td></tr><tr><td>

Recommendation criteria

</td><td>

Recommendation criteria for which this criteria acts as an input.

</td></tr><tr><td>

Order

</td><td>

Order in which this criteria is evaluated.

</td></tr><tr><td>

Application

</td><td>

Name of the application.

</td></tr><tr><td>

Weight

</td><td>

Weight for the filtering constraint. Assign a higher weight to the criteria that are more important.

</td></tr><tr><td>

Ranking method

</td><td>

Method for ranking the criteria. Choices are as follows:-   **More is better:** When setting the ranking, a higher value is better. For example, more skills availability is better when determining the task ranking.
-   **Less is better:** When setting the ranking, a lower value is better. For example, less travel time is better when determining the task ranking.


</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

The task recommendation policy-related criterion is created successfully. The criterion is added to the appropriate related list: Filtering Constraint or Ranking Criteria.

