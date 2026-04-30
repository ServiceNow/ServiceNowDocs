---
title: Setting up Spotlight
description: Set up Spotlight for each set of table records that you want to evaluate and rank by importance. The records must be associated with an indicator.
locale: en-US
release: zurich
product: Spotlight
classification: spotlight
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Setting up Spotlight

Set up Spotlight for each set of table records that you want to evaluate and rank by importance. The records must be associated with an indicator.

Specify the records you want to evaluate by creating a Spotlight group. Create multiple Spotlight criteria and associate them with the group to define how to weight records. In the Spotlight group, you set the sum of the weights of criteria that a record must meet to trigger the creation of a Spotlight.

**Note:** Before you start to work with Spotlight, an administrator must activate a Spotlight plugin.

After creating the Spotlight group and multiple Spotlight criteria, activate the Spotlight group. After the Group is activated, Spotlight scores are collected automatically according to the Spotlight group job schedule. You can also collect Spotlight scores manually at any time for an active group. A Spotlight is automatically created for any records with Spotlight scores that exceed the Spotlight group threshold, allowing you to quickly identify the highest priority work.

-   **[Create a Spotlight group](../task/create-spotlight-group.md#)**  
Create a Spotlight group to define the records to evaluate. In the Spotlight group, you also set the threshold that the score of a record must exceed to trigger the creation of a Spotlight.
-   **[Create Spotlight criteria](../task/create-spotlight-criteria.md)**  
Create Spotlight criteria to define when to weight a record, and the weight to assign.
-   **[Collect Spotlight scores](collect-spotlight-scores.md)**  
To collect Spotlight scores, schedule score collection and activate the Spotlight group. You can also collect scores manually for an active Spotlight group.

**Parent Topic:**[Ranking records with Spotlight](spotlight.md)

**Related topics**  


[Performance Analytics concepts](c_PerformanceAnalytics.md)

