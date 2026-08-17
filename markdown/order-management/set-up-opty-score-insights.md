---
title: Set up ML-based opportunity scoring and insights
description: Give your sales team a win probability score and supporting insights on every open opportunity by training a machine learning \(ML\) model on your closed deals and activating the jobs that score opportunities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/set-up-opty-score-insights.html
release: australia
topic_type: task
last_updated: "2026-08-06"
reading_time_minutes: 5
keywords: [win probability, opportunity scoring, score and insights, predictive intelligence]
breadcrumb: [Opportunity Management, Sales automation apps, Configure, Sales Customer Relationship Management]
---

# Set up ML-based opportunity scoring and insights

Give your sales team a win probability score and supporting insights on every open opportunity by training a machine learning \(ML\) model on your closed deals and activating the jobs that score opportunities.

## Before you begin

You must have installed the ServiceNow Otto for Sales Automation \(sn\_som\_gen\_ai\) application on your ServiceNow instance. This application also installs the following applications that opportunity scoring depends on:

-   Opportunity Management ML \(sn\_opty\_mgmt\_ml\)
-   Opportunity Management AI Features \(com.sn\_opty\_mgmt\_ai\)

If either application is missing from your instance, install it using the Application Manager. For more information, see [Configuring AI capabilities in Sales CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-ai-capabilities-sales-crm.md).

To score and test opportunities without waiting for historical data, select the **Load demo data** option during installation. Demo data populates the Opportunity Feature \[sn\_opty\_ml\_feature\] table with sample opportunities that the model can train on.

The application scope must be set to Opportunity Management ML. You can change the application scope using the application picker \[Omitted image "globe-outline-24.svg"\] Alt text: in the Unified Navigation bar.

Role required: admin

## About this task

Opportunity scoring rates each open opportunity from 0 to 100 based on the patterns that a machine learning model finds in your closed deals. The score comes with plain-language insights that explain the factors behind it, and both appear on the Score and Insights card on the Overview tab of an opportunity record. Each score also maps to a rating that helps sellers triage their pipeline at a glance.

The scheduled jobs that produce these scores are inactive when the application is installed. You must activate and run them in the given order. Each step prepares the data that the next one needs. The jobs fall into the following categories:

-   **One-time setup jobs**

    The backfill, training data, and training jobs run once to build and train the model. Run them again when you switch from demo data to your own closed opportunities, or when enough new deals close to make retraining worthwhile.

-   **Continuous jobs**

    The snapshot job and the inference job run on their own schedules after you activate them, so that the model always has current data and open opportunities keep getting fresh scores.


If you loaded demo data during installation, skip the two steps that build training data from your own opportunities.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    You activate and run the jobs in the next four steps from this list. Search for each job by name.

2.  Back-fill historical snapshots.

    Capture snapshots of the opportunities that closed before you turned on scoring, so that the model can learn from complete deal histories. Skip this step if you loaded demo data during installation. Without a backfill, the model sees opportunity data only from the day you activate the snapshot job, which leaves out the closed deals that training depends on.

    1.  Search for the OpportunitySnapshotBackfillJob scheduled job and select it.

    2.  On the Scheduled Script Execution page, select **Active**.

    3.  Save changes by selecting **Update**.

    4.  Run the scheduled job by selecting **Execute Now**

    Historical snapshots are written to the Opportunity Snapshot \[sn\_opty\_mgmt\_core\_snapshot\] table.

3.  Convert your closed opportunities into the feature rows that the model trains on.

    Skip this step if you loaded demo data during installation, because the Opportunity Feature \[sn\_opty\_ml\_feature\] table is already populated. This job reads closed opportunities from the snapshot data and writes one feature row for each.

    1.  Search for the OpportunityMLTrainingDataJob scheduled job and select it.

    2.  On the Scheduled Script Execution page, select **Active**.

    3.  Save changes by selecting **Update**.

    4.  Run the scheduled job by selecting **Execute Now**

    Feature rows are written to the Opportunity Feature \[sn\_opty\_ml\_feature\] table.

4.  Train the Win Probability model on the feature rows.

    The training job uses Predictive Intelligence to build a classification model that distinguishes won deals from lost ones.

    1.  Search for the OpportunityMLTrainingSolution scheduled job and select it.

    2.  On the Scheduled Script Execution page, select **Active**.

    3.  Save changes by selecting **Update**.

    4.  Run the scheduled job by selecting **Execute Now**

5.  Confirm that training finished before you continue.

    Scores aren't accurate if you point the feature at a solution that is still training.

    1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solutions**.

    2.  Check the state of the solution after each training run.

    3.  Wait until the state is Solution Complete.

6.  Point the scoring feature at the trained solution so that it knows which model to use.

    1.  In the **Solutions** list, search for a string containing `PTC` \(Probability to Close\) and note the name of the solution.

        The solution that you select must have a state of Solution Complete.

    2.  Set the application scope to Opportunity Management Data Model using the application picker \[Omitted image "globe-outline-24.svg"\] Alt text: in the Unified Navigation bar.

    3.  Navigate to **All** &gt; **System Properties**.

    4.  Find and select the **sn\_opty\_mgmt\_core.ml.config** property.

    5.  In the **Value** field, enter the solution name that you noted earlier.

    6.  Select **Update**.

7.  Activate ongoing snapshots so that the model and the scoring job always work with current opportunity data.

    Complete this step whether or not you loaded demo data. The snapshot job takes a point-in-time snapshot of every active opportunity every four hours, and those snapshots feed both model training and scoring.

    1.  Search for the OpportunitySnapshotJob scheduled job and select it.

    2.  On the Scheduled Script Execution page, select **Active**.

    3.  Save changes by selecting **Update**.

    The job starts running on its four-hour schedule. You don't need to run it manually.

8.  Activate scoring so that open opportunities receive a score and insights.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Search for the OpportunityPTCInferenceJob scheduled job.

    3.  On the Scheduled Script Execution page, select **Active**.

    4.  Save changes by selecting **Update**.

    The job scores open opportunities in batches and generates the insights that explain each score.

9.  Verify that scores appear for your sales team.

    1.  Navigate to **Workspaces** &gt; **CRM Workspace**.

    2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

    3.  Navigate to **Opportunity** &gt; **All**.

    4.  Select an opportunity record you want to test.

    5.  Select the **Overview** tab.

    6.  Confirm that the **Score and Insights** card shows a score and insight text.

        If the card is empty, wait for the OpportunityPTCInferenceJob job to complete its first run.


## Result

Open opportunities show a win probability score from 0 to 100. Insights explain the factors working for and against the deal. Favorable and unfavorable factors appear with green and red caret icons respectively, so that sellers can see where to focus.

## What to do next

[View opportunity scores and insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-opty-scores-insights.md)

