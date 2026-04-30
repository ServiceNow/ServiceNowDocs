---
title: Intent Discovery
description: Use the Intent Discovery application to help identify opportunities for incident deflection. For example, you can use it to identify which Virtual Agent conversations to activate next.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# Intent Discovery

Use the Intent Discovery application to help identify opportunities for incident deflection. For example, you can use it to identify which Virtual Agent conversations to activate next.

## Summary usage

For applications that consume NLU, such as Virtual Agent and AI Search, Intent Discovery helps you to better understand which prebuilt intents you can benefit from, and which custom intents would be useful to create.

Intent Discovery provides an analysis that you run on historic incident data or other task data. You can also group the run’s remaining records into different clusters so you can manually add utterances to NLU intents. In addition, you can use specific clusters to create new intents in a model.

In this example scenario, you're using Intent Discovery to identify the top intents in your instance, and how much coverage they can provide across your historic incident records.

## Installation

Intent Discovery is available from the ServiceNow Store. For more information, see [Install Intent Discovery](../task/install-intent-discovery.md).

After Intent Discovery is installed and activated, it appears under **All** &gt; **NLU Workbench** &gt; **NLU Advanced Features**.

**Note:** Although organized under NLU Advanced Features in the navigation pane, Intent Discovery is a separate application that is not included when installing NLU Workbench - Advanced Features.

## Intent Discovery report details

-   When **Taxonomy** is selected, the generated report contains intent recommendations against the selected taxonomy. A taxonomy is a prebuilt library of intents in a specific domain. While you don't have access to the underlying intents, when you run Intent Discovery against a specific taxonomy, data that maps to any intent in the taxonomy will be identified.
-   **Unmatched records** are the utterances which couldn't match to any intent in the taxonomy.
-   **Recommended intents** are the intents which are found from utterances that data was run on.
-   The percentage of **Unmatched records \(clustered\)** are the records that aren't classified \(records that don't belong to any of the recommended intents\).
-   The percentage of unmatched records and the number of recommended intents don't need to match. It's a coincidence if they match.

## Creating an Intent Discovery report

1. Using the admin or nlu\_admin role, navigate to **All** &gt; **NLU Workbench** &gt; **NLU Advanced Features** &gt; **Intent Discovery**.

2. Select either **Run analysis** or **Find recommendations**.

![On the Intent Discovery landing page, buttons for Run analysis and Find recommendations are highlighted.](../images/intent-discovery1w.png "Intent Discovery landing page")

## Running an analysis on the report

1. For this example report, you configure the following fields on the Intent Discovery &gt; Create new screen.

-   Data Source: Select the **Incident \(incident\)** table.
-   Filter by: **\[Created\] \[on\] \[This quarter\]**
-   Field to analyze: **Short description \(short\_description\)**. You choose Short description because it's a highly used string field that references words that can help the system identify an intent.
-   Taxonomy: Select **ITSM**. This field tells the system to run classification processing on your ITSM incident records. It has 3 options: Classification, ITSM, or blank, which defaults as Classification.
-   Cluster unmapped utterances by keywords... : Select the **check box**. When you check this box, the system groups your incident records that weren't classified into clusters.
-   Report name: The field automatically defaults to **Incident &lt;month/day/year&gt;**. You can edit the name if you prefer. In this example scenario, you enter `Incident 12/16/2020 - SF Test`.

2. Select **Run analysis**.

![The Intent Discovery > Create New screen and the fields you need to configure before you select Run Analysis](../images/intent-discovery2.png "Selecting data sources in Intent Discovery for a run analysis")

**Result**: Your report appears on the Intent Discovery screen, showing its status as the analysis begins. The subsequent status values appear in the following order during the analysis: Preparing to run, Work in progress, Clustering, and Done. This can take from 5 minutes to 30 minutes to complete. The fewer the records you have in a cluster, the less time it takes. Turning clustering off can also speed up the process.

![Your report appears on the Intent Discovery screen where the analysis shows its ongoing status as its job begins and ends](../images/intent-discovery3.png "An ongoing run analysis")

When the analysis is complete, the column values on the screen appear, with the **Status** column value set to **Done**, as shown in the image below.

**Note:** If you want to delete the report and start over, point to the right of the Status column to invoke the **Delete report** icon.

3. Select the **Name** of your report.

![The report column values have appeared, as the analysis is complete and its status value is set to Done](../images/intent-discovery4.png "A completed run analysis")

**Result**: The screen refreshes, showing the analyzed incident records and the remaining incident records that were not classified.

## Importing recommended intents to new or existing custom models

Before importing intents to an NLU model, ensure that you are in the same application scope as the model. For more information, see [Select an application from the application picker](https://www.servicenow.com/docs/access?context=t_SelectAnAppFromTheAppPicker&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

1. On the Records covered by recommendations section of the screen, select the caret icon on a recommended intent you want to add to a custom model.

![Instructions to click the caret button which opens to reveal the details of the recommended intent](../images/intent-discovery5.png "Reviewing a recommended intent")

**Result**: The details of the recommended intent appear so you can review them, as shown in the image below.

2. Select **Add to Model**.

![The recommended intent details are shown with an instruction to add them to a model](../images/intent-discovery6.png "Adding a recommended intent to a model")

3. On the Select a destination model screen that appears, choose a model you want to add the recommended intent to. If you can't find an appropriate model, create a new one, return to the report, and add the new model.

**Note:** The model you choose must have the same application scope as your current scope.

4. Select **Save**.

![The model you choose to associate to the recommended intent is followed by an instruction to select the Save button](../images/intent-discovery7.png "Saving a recommended intent to a model")

**Result**: A banner appears on the screen, confirming the intent is added to the target model.

![A banner that confirms the recommended intent you chose has been successfully added to the target model](../images/intent-discovery8.png "Confirmation of adding a recommended intent to a target model")

The recommended intent also appears on the Model screen of the target model, as shown in the image below.

![The recommended intent is now visible in the Model screen of the target model](../images/intent-discovery9.png "View a recommended intent in the target model")

## Adding clustered utterances to an intent and its model

1. On the Remaining records section of the intent discovery records screen, select and open a cluster of utterance and short description data that you want to add to an intent and its associated model.

As you continue to build out new intents from these clusters, you can click the **Ignore** icon to remove any unwanted intents from the report.

There's also a **Show Additional** filter you can use to show or hide the added intents, and the ignored intents as well.

2. Select **Add to intent**.

![The cluster you chose to add to an intent. Select the Add to Intent button or choose the Ignore button if you want to remove the cluster from the report](../images/intent-discovery10.png "Adding a cluster to an intent")

3. In the Add this cluster to an intent and model screen, select an intent and model pair you want to associate to this cluster.

![How to add an a cluster to an intent and its model](../images/intent-discovery11.png "Adding a cluster to an intent and model")

4. Enter a few utterance examples into the open text field. Select **Add** each time you complete your entry to save it in the system. Use the pencil icon or the trash can icon respectively to edit or delete your entry.

5. Select **Save**.

![Instruction to add and save paraphrased utterances to an intent](../images/intent-discovery12.png "Adding paraphrased utterances to an intent")

**Result**: The records screen appears, showing a banner confirming you added two new utterances to the target intent and its associated model. The model and intent pair appears in the **Added To** column, as shown in the image below.

![A banner that confirms the utterances you added to the intent are successfully added](../images/intent-discovery13.png "Confirmation of adding paraphrased utterances to an intent")

Use the **Show Additional** filter if you want to show or hide the clusters that have added intents, and the clusters that are ignored.

![How to show or hide clusters that have added intents, and those that you have marked as ignored](../images/intent-discovery13a.png "Viewing or hiding clusters and ignored clusters")

## Running another analysis on your Intent Discovery report

1. Select **Run Again**.

![Instruction to choose the version of the analysis you want to run](../images/intent-discovery14.png "Selecting the version of the analysis to run")

**Result**: The new run begins. When it's in progress, the option to cancel the run appears, as shown in the image below.

![An image that shows the Cancel Run option is available during the first few minutes of the In Progress phase of the run](../images/intent-discovery15.png "The Cancel Run option")

When the run is complete, a new banner appears that states you have a new version of the report.

2. Select the new version, then select **Run Again**.

![How to select the new version of the report.](../images/intent-discovery16.png "Selecting the new version of the report")

**Result**: The time stamp you selected for the most recent run appears in the **Run date** column of the Intent Discovery screen.

![The new time stamp of the Intent Discovery report](../images/intent-discovery17.png "View the new time stamp of the Intent Discovery report")

-   **[Install Intent Discovery](../task/install-intent-discovery.md)**  
You can install the Intent Discovery application \(sn\_nlu\_discovery\) if you have the admin role.

**Parent Topic:**[NLU Workbench - Advanced Features](nlu-workbench-advanced-features.md)

