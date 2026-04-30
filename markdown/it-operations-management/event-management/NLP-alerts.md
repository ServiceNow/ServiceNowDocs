---
title: Verify text-based clustering solution
description: Event Management uses Natural Language Processing \(NLP\) algorithms to identify common text patterns in alerts and create alert groups such as clustering algorithm.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Text-based alert grouping, Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Verify text-based clustering solution

Event Management uses Natural Language Processing \(NLP\) algorithms to identify common text patterns in alerts and create alert groups such as clustering algorithm.

## Before you begin

Ensure that the Predictive Intelligence plugin is installed.

Ensure the parameter **sa\_analytics.text\_based\_group\_enabled** is set to `true`.

**Note:** If the Predictive Intelligence plugin is not installed, then the text-based logic will not be executed, even if **sa\_analytics.text\_based\_group\_enabled** is set to true. This is because in text-based grouping, alerts are clustered based on the description, metric name, and CI class. Even if the Predictive Intelligence is active, if the clustering is not performed, the text-based groups will not be created.

Ensure that there are at least 100 alerts in the Alerts table \[em\_alerts\].

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

    The Clustering Definitions page opens.

2.  Select EM ALert Clustering Solution.

3.  Verify that the **Active** check box is selected.

4.  Select **Submit &amp; Train**.

    For details on ML solutions, see [Reviewing your ML solution training jobs](https://www.servicenow.com/docs/access?context=reviewing-ml-solution-training-jobs&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).


