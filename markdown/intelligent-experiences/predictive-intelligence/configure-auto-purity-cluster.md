---
title: Apply purity on a clustering solution
description: Apply purity to learn details about the composition of each cluster. For example, see what percentage of incidents in a cluster have the same value for Assignment Group. You can specify which fields to focus on, or you can let auto-purity display fields by default.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create and train a clustering solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Apply purity on a clustering solution

Apply purity to learn details about the composition of each cluster. For example, see what percentage of incidents in a cluster have the same value for Assignment Group. You can specify which fields to focus on, or you can let auto-purity display fields by default.

## Before you begin

-   Create a clustering definition solution or use an existing one.
-   Role required: admin or ml\_admin

## About this task

With purity, you can choose field distribution metrics for your clusters to display. The table assigned to your solution determines which fields are available. For more information about purity, see the following articles on ServiceNow Community:

-   [https://www.servicenow.com/community/intelligence-ml-articles/using-purity-fields-to-better-understand-your-clusters/ta-p/2302441](https://www.servicenow.com/community/intelligence-ml-articles/using-purity-fields-to-better-understand-your-clusters/ta-p/2302441)
-   [https://www.servicenow.com/community/intelligence-ml-articles/predictive-intelligence-using-the-cluster-insight-table-to/ta-p/2301006](https://www.servicenow.com/community/intelligence-ml-articles/predictive-intelligence-using-the-cluster-insight-table-to/ta-p/2301006)

If you do not select any fields, auto-purity automatically determines which insights to show based on distribution significance. You can change the default auto-purity selections by editing the ML Auto Purity Configuration \[ml\_autopurity\_config\] table.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

2.  Select a solution definition or create a new one.

3.  Select the **Calculate Purity** check box.![The solution definition form for Clustering solutions, with the Calculate Purity check box highlighted and selected.](../images/calculate_purity_checkbox.png)

4.  Select the **Purity Fields** lock icon and choose the fields that you want displayed in cluster results.

    **Note:** If you don't select any fields, auto-purity displays the most significant fields based on distribution.

    ![Purity Fields selection in the Clustering Definition form.](../images/select_purity_fields.png)

5.  Select **Update** or **Update &amp; Retrain**.


## Result

View your insights by opening the **Cluster Visualization** tab of your retrained solution, then pointing to a cluster. Under **Purity based on**, the format displays as:

field name : value : percent.

For example, the row priority : 5 : 100% means that 100% of the members of this cluster have the value of 5 for the priority field.![Pop up for an individual cluster on the Cluster Visualization view.](../images/purity_insights_cluster.png)

