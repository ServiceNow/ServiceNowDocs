---
title: Configure TF-IDF for solutions
description: Apply Term Frequency–Inverse Document Frequency \(TF-IDF\) encoding to classification, clustering, or similarity solutions for Predictive Intelligence.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Configure TF-IDF for solutions

Apply Term Frequency–Inverse Document Frequency \(TF-IDF\) encoding to classification, clustering, or similarity solutions for Predictive Intelligence.

## Before you begin

**Note:** Configuring advanced settings on your ML solutions is optional. If you choose to configure any of these settings, make sure you're well informed regarding the technology you're enabling in the solution, and that you have a use case that benefits from what the technology offers. For more information, see [https://www.servicenow.com/community/intelligence-ml-articles/dive-deeper-with-clustering-advanced-parameters/ta-p/2695847](https://www.servicenow.com/community/intelligence-ml-articles/dive-deeper-with-clustering-advanced-parameters/ta-p/2695847).

-   Create a classification, clustering, or similarity solution definition or use an existing one.
-   Role required: admin or ml\_admin

## About this task

Predictive Intelligence uses paragraph vector word embedding by default in its classification and similarity frameworks, which is highly effective for processing data comprised of primarily human-readable content. However, TF-IDF might return better prediction results for records that have machine-generated content, such as alerts and error messages for log files. Choose advanced settings that are appropriate for the kind of data your solution is processing.

**Note:** The steps for configuring TF-IDF are the same for all model frameworks, but TF-IDF support for clustering solution definitions is applicable only if you have a Professional subscription.

## Procedure

1.  Navigate to a **Solution Definition**, such as **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  Open a solution definition form.

    In this example scenario, you use a CMDB similarity definition form.

    ![An example similarity solution definition on which you apply the TF-IDF parameter.](../images/tf-idf-similarity-solution1.png)

3.  On the Advanced Solution Settings tab in the Related Links section of the form, click **New**.

    ![How to select the Solution Parameters option for creating the parameter.](../images/tf-idf-similarity-solution2.png)

4.  Create a parameter record.

    1.  In the **Solution Parameters** field, click the search icon.

    2.  In the ML Solution Parameters screen, select **Use tf-idf to generate vectors**.

    ![How to create the parameter record by selecting the Search button, and then selecting the TF-IDF key Short Description.](../images/tf-idf-similarity-solution3.png)

5.  Click **Submit**.

    The Advanced Solution Setting record screen refreshes.

    ![See the new Advanced Solution Setting record you created.](../images/tf-idf-similarity-solution5.png)

6.  Click **Submit**.

    **Result:** TF-IDF is configured for your similarity solution. Its solution parameter appears on the Advanced Solution Settings tab of your similarity definition form.

    ![This image shows the Advanced Solution Setting record for TF-IDF.](../images/tf-idf-similarity-solution6.png)


**Related topics**  


[Create and train a classification solution](create-solution-definition.md)

[Create and train a similarity solution](create-similarity-solution.md)

[Create and train a regression solution](create-regression-solution.md)

[Create and train a clustering solution](create-clustering-solution.md)

