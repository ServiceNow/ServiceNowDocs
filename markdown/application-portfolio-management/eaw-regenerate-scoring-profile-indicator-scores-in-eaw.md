---
title: Regenerate scoring profile indicator scores on-demand in Enterprise Architecture Workspace
description: You can update the scoring profile indicator scores on-demand. Updating the scoring profile indicators scores is necessary when the scoring profile is updated with new indicators.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure scoring profiles, Work with the Setup page in the Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Regenerate scoring profile indicator scores on-demand in Enterprise Architecture Workspace

You can update the scoring profile indicator scores on-demand. Updating the scoring profile indicators scores is necessary when the scoring profile is updated with new indicators.

## Before you begin

Role required: sn\_apm.apm\_admin

## About this task

On-demand generation of the indicator scores is more efficient than running scheduled jobs, when immediate results for the updated data and conditions, if necessary.

## Procedure

1.  Navigate to **Workspace** &gt; **Enterprise Architecture Workspace**.

2.  Open the Setup page by selecting the Setup icon ![Setup icon](../../image/eaw-image/setup-icon.png).

3.  Select the expand row icon \(![Expand Row icon.](../../image/ExpandIcon.png)\) next to **Scoring Profiles**.

4.  Select **All**.

5.  Select the scoring profile that you want to generate the indicator score for.

6.  Select **Regenerate indicator score**.

    The **Regenerate scores** pop-up window appears.

7.  In the **Fiscal Period** box, enter the fiscal period that you want to generate the indicator score for.

    You can also select the lookup using list icon ![Lookup using list icon.](../../image/eaw-image/lookup-using-list-icon.png) to view the list of available fiscal periods.

8.  Select **OK**.

    This action doesn’t update the existing capability indicator scores but deletes them and generates new scores.


**Parent Topic:**[Configure scoring profiles](../../concept/eaw-concept/eaw-configure-scoring-profiles.md)

