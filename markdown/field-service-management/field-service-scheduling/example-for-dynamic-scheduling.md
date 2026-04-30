---
title: Example - Dynamic Scheduling
description: Explore how Dynamic Scheduling prioritizes the best agent for a task, focusing on key matching criteria.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Example - Dynamic Scheduling

Explore how Dynamic Scheduling prioritizes the best agent for a task, focusing on key matching criteria.

Consider a scenario in which all field technicians work in the same region. Since all technicians are going to be the same relative distance from a task, availability to perform a task is the most important criteria, followed by matching part requirements.

This example assumes the following information.

-   Maximum number of hours available in a day: 8
-   Total parts required: 5

Matching Criteria Values are described in the following list. Alice and Mack are Global Teller Systems field technicians.

-   Alice has 5 hours of availability and 2 of the required parts.
-   Mack has 8 hours of availability and 1 of the required parts.
-   **Availability Today** criteria is assigned a weight of **20**, as it is most important.
-   **Agents with most parts** criteria is assigned a weight of **10**, as it should be considered as the next most important criteria.
-   All criteria have a ranking method of **More is better**.

|Alice|Criterion|Weight|Ranking Method|Mack|
|-----|---------|------|--------------|----|
|5|Availability Today|20|More is better|8|
|2|Agents with most parts|10|More is better|1|

Now that we have the matching criteria values, we can calculate the criterion rating.

First, calculate a number for each criterion, based on the sample work order task data provided:

Available today:

Alice: 5 / 8 = 0.625 \(with 8 being the maximum number of hours\).

Mack: 8 / 8 = 1.

Technicians with most parts:

Alice: 2/5 = 0.4 \(with 5 being the total number of parts required\).

Mack: 1 / 5 = 0.2.

|Alice|Criterion|Weight|Ranking Method|Mack|
|-----|---------|------|--------------|----|
|5/8|Availability today|20|More is better|8/8|
|2/5|Technicians with the most parts|10|More is better|1/5|

After we have the matching values and the criterion rating we can calculate the technician ranking for Alice and Mack.

The following is the technician ranking for Alice.

Multiply the number for each criterion by the criterion weight and then divide the result by the total of all criterion weight. Repeat for each criterion and add the results.

Formula: \(Criteria\_1 rating x Criteria\_1 weight\) / total criterion weight + \(Criteria\_2 rating x Criteria\_2 weight\) / total criterion weight +\(Criteria\_3 rating x Criteria\_3 weight\) / total of criterion weight = technician rank/score.

|Criterion|Criterion rating with calculation|Weight|Score|
|---------|---------------------------------|------|-----|
|Availability Today|0.625|20|0.4166|
|Technicians with most parts|0.4|10|0.1333|
|Total| |30|0.5499|

The following is the technician ranking for Mack.

Multiply the number for each criterion by the criterion weight and then divide the result by the total of all criterion weight. Repeat for each criterion and add the results.

Formula: \(Criteria\_1 rating x Criteria\_1 weight\) / total criterion weight + \(Criteria\_2 rating x Criteria\_2 weight\) / total criterion weight +\(Criteria\_3 rating x Criteria\_3 weight\) / total of criterion weight = technician rank/score.

|Criterion|Criterion rating with calculation|Weight|Score|
|---------|---------------------------------|------|-----|
|Availability Today|1|20|0.6667|
|Technicians with most parts|0.2|10|0.0667|
|Total| |30|0.7334|

Result: Mack \(0.7334\) has a higher ranking score than Alice \(0.5599\), therefore Mack is assigned the task.

## Consider distance from task in addition to matching criteria

Consider how the calculation would change if the field agents were not all in the same, small region. When distance matters, the **Current Distance From Task** or **Distance From Task** matching criteria can be used. These distance from task criteria are unlike the other criteria because the closer the field agent is to the task, the better. Therefore, unlike the other criteria, a lower number here is better than a higher number. The less is better adjustment is necessary to make a true comparison of the resulting scores. An adjustment is made by subtracting the score from one \(1\) for any criterion using the ranking method Less is better.

**Note:** **Distance From Task** calculation occurs in the **LocationFromTask** Script Includes and **Current Distance From Task** calculation occurs in the **CurrentLocationFromTask** Script Includes. This calculation takes the task latitude and longitude and compares it to the agent's latitude and longitude, as expressed in miles.

**Related topics**  


[Configure dynamic scheduling](../task/create-dynamic-scheduling-config.md#)

