---
title: Verify text-based clustering solution
description: Event Management uses Natural Language Processing \(NLP\) algorithms to identify common text patterns in alerts and create alert groups through clustering. This approach not only organizes similar alerts efficiently but also reduces noise and helps focus on significant issues, enhancing overall alert management.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Text-based alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Verify text-based clustering solution

Event Management uses Natural Language Processing \(NLP\) algorithms to identify common text patterns in alerts and create alert groups through clustering. This approach not only organizes similar alerts efficiently but also reduces noise and helps focus on significant issues, enhancing overall alert management.

## Before you begin

Ensure that the Predictive Intelligence plugin \(com.glide.platform\_ml\) is installed.

Ensure the parameter **sa\_analytics.text\_based\_group\_enabled** is set to `true`.

**Note:** If the Predictive Intelligence plugin is not installed, the text-based logic will not execute, even if **sa\_analytics.text\_based\_group\_enabled** is set to true. This is because text-based grouping relies on clustering alerts based on the description, metric name, and CI class. Without the plugin, clustering cannot be performed, and as a result, text-based groups will not be created, regardless of the active status.

Ensure that there are at least 100 alerts in the Alerts table \[em\_alerts\].

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

    The Clustering Definitions page opens.

2.  Select EM ALert Clustering Solution.

3.  Verify that the **Active** check box is selected.

4.  Select **Update &amp; Retrain**.

    For more information on ML solutions, see [Reviewing your ML solution training jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/reviewing-ml-solution-training-jobs.md).


