---
title: Create custom recommendation criteria
description: Define recommendation criteria that policies can use to rank or evaluate tasks for agents.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Intelligent Task Recommendations, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create custom recommendation criteria

Define recommendation criteria that policies can use to rank or evaluate tasks for agents.

## Before you begin

Role required: admin

## About this task

Some predefined recommendation criteria are provided for you. For more information, see [Predefined recommendation criteria](../reference/fsm-task-recommendation-components.md#).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Task Recommendation Administration** &gt; **Recommendation Criteria**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Display Name|Display name of the recommendation criterion.|
    |Name|Name of the recommendation criterion.|
    |Prefetched table|The prefetched table selected for the recommendation criterion.|
    |Prefetched fields|Supporting prefetched fields from the prefetched table.|
    |Type|Type of the criterion, either filter or rank.|
    |Application|The application containing this record.|
    |Application module|The default value is Field Service Management.|

4.  In the **Script** field, enter the script that you want to run when recommending tasks to the agent.

    For example, the following script calculates the distance between the agent's current location and the task location.

    ```
    var distanceRule = new TaskRecommendationDistanceRuleProcessor(args); 
    var ruleProcessResult = distanceRule.processRule(user, tasks, timeStart, timeEnd, 'ranking'); 
    ruleResult = TaskRecommendationFSMUtil.parseRuleResult(ruleProcessResult, "Distance from task");
    ```

    For information about custom script requirements, see [Providing a script for custom task recommendation criteria](../reference/script-guidelines-recommendation-criteria.md).

5.  Click **Submit**.


## Result

The recommendation criterion is created successfully, and sorted into either the Filtering Constraints or Ranking Criteria group based on the selected type.

**Parent Topic:**[Setting up Intelligent Task Recommendations](../concept/administer-task-recommendations.md)

