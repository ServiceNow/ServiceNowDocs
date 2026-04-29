---
title: Create and train a clustering solution
description: Group similar records into clusters so you can address them collectively or identify patterns.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Create and train a clustering solution

Group similar records into clusters so you can address them collectively or identify patterns.

## Before you begin

Role required: ml\_admin or admin

**Important:** In the Australia release, models in the classification, clustering, and similarity frameworks use Workflow solutions. These are pre-trained, so a word corpus isn't needed for your new solutions. When your existing solutions with a word corpus are re-trained after upgrading, they become Workflow solutions, and the Word Corpus field is removed from the form.

## About this task

In this example procedure, you're creating a solution to identify a major incident by grouping similar incidents that have occurred recently.

For information on using encrypted training data, see [Data Encryption in Predictive Intelligence](../reference/predictive-intelligence-encryption.md).

## Procedure

1.  Ensure that you are in the application scope that you want for your solution definition, then navigate to **All** &gt; **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

2.  On the Clustering Definitions list, select **New**.

3.  On the Clustering Definition form, configure the fields according to the following guidance.

<table id="table_gtt_kdh_3hb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Enter a unique name for your clustering solution. For example, in this use case you could enter `Group Incidents to a Major Incident.`

</td></tr><tr><td>

Name

</td><td>

As you enter your solution Label, this field automatically populates with a system-assigned name based on your Label value.

</td></tr><tr><td>

Word Corpus

</td><td>

If you have a legacy clustering solution, you can select a relevant word corpus from the **Word Corpus** field in the definition form.

 **Note:** With the Australia release, a word corpus is not required, because a pre-trained model is used instead. The **Word Corpus** field is not visible in the definition form for pre-trained models.

 For more information, see [Create a word corpus](create-word-corpus.md).

</td></tr><tr><td>

Table

</td><td>

Select the table that contains record types that you want to group into one or more clusters. For example, in this use case you select the **Incident \[incident\]** table as it contains incident records you want to group together for a major incident analysis.

 When you assign a table value, a link appears in the form that shows the number of records that match your current conditions.

</td></tr><tr><td>

Fields

</td><td>

Select one or more input fields types that help the system identify the records you want to include in your cluster. In this use case, use **Short description**.**Note:** When selecting a reference type field, you must dot-walk to the field's property name. For example, instead of `short_description`, enter `short_description.name`.

</td></tr><tr><td>

Use Group By

</td><td>

Select this check box only if you want to group input records by a field before creating clusters.**Note:** Selecting this check box activates the **Group By** list. If you don't select the check box, all the table records are grouped into clusters.

</td></tr><tr><td>

Group By

</td><td>

Selecting a value from this list is optional. If you do so, the system groups records into one or more clusters based on your selection.

</td></tr><tr><td>

Purity Fields

</td><td>

Choose fields from your table that can help the system identify the class that is most frequent in the cluster. In this example scenario, select **Category** and **Assignment group.Name**.

</td></tr><tr><td>

Filter

</td><td>

Add filter conditions to apply to the input field records that you want to include in your clusters.-   The maximum number of records for clustering is limited to 300,000.
-   For best results, aim for at least 2000 records as a minimum.
 **Note:** Script includes can't be referenced from the Filter. Use database views as an alternative.

</td></tr><tr><td>

Processing Language

</td><td>

Select the dominant language of the dataset you're training on the solution definition. If the dataset language is Italian, choose **Italian**. Also, English processing is applied to all datasets by default. For example, if you select Italian, the system processes the data in both English and Italian.**Note:** The term processing indicates some of the language-specific steps used as part of training a solution. For example, tokenizing words, removing stop words, and stemming.

</td></tr><tr><td>

Stopwords

</td><td>

When you select your processing language, the system automatically adds a Stopwords list in that language. For example, if your processing language is Italian, the **Default Italian Stopwords** list appears. The **Default English Stopwords** list is also included. If you create a custom stopwords list, you can select it from the Stopwords field to add to your solution.

</td></tr><tr><td>

Update Frequency

</td><td>

Select how often you want the system to update your clusters with new and updated records.

**Note:** The system pulls records based on the Group By filter conditions that you set on your clustering solution, if any.

 For example, if you select **Every 15 minutes**, the system identifies which records have arrived within that time frame. The system tries to assign them to the existing clusters, or creates a new cluster if possible.

 In this example, 20 new records arrive. If 16 of those records make it into an existing cluster and 4 don't, the system forms a new cluster for the four unassigned records.

 You can also choose not to update your clusters at all.

</td></tr><tr><td>

Training Frequency

</td><td>

Select how often you want the system to discard all previous cluster results and recreate clusters from the beginning. Your options range from daily, every third day, every seven days, or monthly. You can also choose to train your cluster once.**Note:** The ML scheduler limits the number of trainings an instance can commit to 50 new ML training requests per instance within a 24-hour window. The limit excludes scheduled retraining requests. In addition, clustering and similarity updates are also excluded from this limit, even if the new training requests exceed 50 within a 24-hour window.

</td></tr><tr><td>

Minimum number of records per cluster

</td><td>

Enter the minimum number of records you want a cluster to contain. The value you enter must be 2 or higher.

</td></tr></tbody>
</table>4.  Select the appropriate context menu option or button for your solution definition.

    |Option|Description|
    |------|-----------|
    |**Save or Save &amp; Train**|Save your solution definition record so you can return to it later, or save and submit it for training.|
    |**Submit or Submit &amp; Train**|Create your solution definition record and submit it, or submit and train it.|

5.  If you submitted the solution for training, select **OK** on the Training Activation window to confirm.


## Result

The system trains the solution and notifies you in real time when the training completes.

A treemap plot appears on the Cluster Visualization tab of your Clustering Solution Definition form. The plot shows the clusters the system formed for your solution in descending order from the top-left corner to the bottom-right corner. The treemap node labels are the Cluster Concept, which is created by the top words from the cluster, and helps you see the most prominent content found in each cluster.

**Note:** The Cluster Concept displays the top words from the processed input data, in the data's language. Depending on the language, the Cluster Concept may display words in their root form and so appear truncated.

Each node is colored from red to green depending on the cluster quality for that node. The Select Group filter appears only when you select the **Use Group By** and **Group By** fields on your Clustering Definition form. When you point to a cluster, you can see its Groupby value, Cluster Count, and Records in Groupby.

![Cluster Visualization tab of your Clustering Solution Definition form. It shows the clusters the system formed for your solution in descending order.](../images/predict-intel-clustering-treemap1.png "Cluster visualization example")

To open a cluster, you can click it, or select it from the Show All Groups filter.

Inside the cluster grouping, you can filter the results further by using the two slide bars for cluster size and cluster quality, respectively. You can also navigate backward by clicking the Back button, which only appears when a clustering hierarchy is present. When you point to a cluster at this level, the Purity field percentile values appear along with the Cluster Concept, Quality, and Size values.

![Cluster group. You can filter for cluster size and cluster quality. When you point to a cluster at this level, the Purity field values appear.](../images/predict-intel-clustering-treemap3.png "Cluster group example")

When you click a cluster node, its ML cluster details appear in a list view format.

![The ML Cluster Detail table contains the record IDs for the clustering solution, Groupby node, ML solution name, and ranking percentage are shown in a list view format.](../images/predict-intel-clustering-treemap4.png "Cluster details page")

## What to do next

-   Review the solution output on the Solution Statistics tab of your solution. If you aren't satisfied with your clustering solution results, reconfigure the values you've set to your solution and retrain it until the results are to your satisfaction.

-   Review the Cluster Summary tab for a list view of the cluster IDs, quality size, and Groupby values.

    ![The Cluster Summary table shows all clusters are listed by cluster ID,quality, size, and groupby value.](../images/predict-intel-clustering-treemap5.png "Cluster Summary example")

-   On the Cluster Updates tab, review the summary of changes to clusters for each cluster update interval you configured in the solution definition.

    ![The Cluster Updates tab shows records assigned to other clusters, newly created, and how many records have been assigned to new clusters, and the total number of records clustered.](../images/predict-intel-clustering-treemap6.png "Cluster updates example")


