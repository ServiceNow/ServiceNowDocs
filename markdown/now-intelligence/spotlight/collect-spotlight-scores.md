---
title: Collect Spotlight scores
description: To collect Spotlight scores, schedule score collection and activate the Spotlight group. You can also collect scores manually for an active Spotlight group.
locale: en-US
release: australia
product: Spotlight
classification: spotlight
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up Spotlight, Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Collect Spotlight scores

To collect Spotlight scores, schedule score collection and activate the Spotlight group. You can also collect scores manually for an active Spotlight group.

## Before you begin

1.  [Create a Spotlight group](../task/create-spotlight-group.md#)
2.  [Create Spotlight criteria](../task/create-spotlight-criteria.md)

Role required: pa\_spotlight or admin

## About this task

When Spotlight collects scores, Spotlight also deletes all older Spotlight records for the associated Spotlight group, without exception.

## Procedure

1.  Open the Spotlight group that you want to collect scores for.

2.  If it is not already selected, select **Active** in the check box and save the Spotlight group form.

    New Spotlight groups are active by default.

    You can now execute the Spotlight job using the **Execute Now** button. ![Execute Now button on an active Spotlight group form](../image/spotlight-execute-now.png)

3.  To collect scores immediately, click **Execute Now**.

4.  Go to the **Schedule** section and in the **Run** field, select the frequency at which to collect Spotlight scores.

5.  Fill in any specific information about when the Spotlight scores will be collected.

    The required information depends on the period you choose in the **Run** field. For example, if you choose to run **Daily**, you have to fill in the time of day to run. If you choose **Monthly**, you have to fill in the day of the month and the time of day to run.

6.  If you are using domain separation, specify a user in the **Run as** field.

    If you do not specify a **Run As** user, scores are evaluated for the Global domain. In this case, Spotlight scoring is performed for all matching records in all domains.

    For more information, see [Domain separation with Spotlight](domain-separation-spotlight.md).


## Result

Spotlight starts collecting scores according to the schedule you set. You can also collect scores manually at any time by clicking **Execute Now**. Administrators who need to troubleshoot scheduling can read [Schedule Item \[sys\_trigger\] records for Spotlight](activating-spotlight-group.md).

## What to do next

You can see the details of the criteria that contribute to a Spotlight score. For more information, read [See Spotlight score details](../task/view-details-of-a-spotlight.md). You can also see and share an [interactive analysis](spotlight-interactive-analysis.md) of the results.

**Parent Topic:**[Setting up Spotlight](setting-up-spotlight.md)

