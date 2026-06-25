---
title: Configure Connect Component algorithm and Levenshtein Distance method for a clustering solution
description: Apply Configure Connect Component and Levenshtein Distance method encoding to optimize the training for your clustering solutions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/predictive-intelligence/configure-connect-component-levenshtein-distance-for-clustering.html
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Configure Connect Component algorithm and Levenshtein Distance method for a clustering solution

Apply Configure Connect Component and Levenshtein Distance method encoding to optimize the training for your clustering solutions.

## Before you begin

Role required: admin or ml\_admin

**Note:** Configuring advanced settings on your ML solutions is optional. If you choose to configure any of these settings, make sure you're well informed regarding the technology you're enabling in the solution, and that your use case benefits from what the technology offers. For more information, see the [Dive deeper with Clustering Advanced Parameters](https://www.servicenow.com/community/intelligence-ml-articles/dive-deeper-with-clustering-advanced-parameters/ta-p/2695847) article on ServiceNow Community.

-   Create and train a clustering solution definition or use an existing one.
-   Role required: admin or ml\_admin

## About this task

When training clustering solutions, you have the following three options.

-   Use the default k-means algorithm.
-   Use the optional DBSCAN solution parameter with the Euclidean distance method as a metric.
-   Use the optional DBSCAN, Minimum Neighbors, and Levenshtein Distance solution parameters. Connect Component is enabled by DBSCAN and Minimum Neighbors, and supports both Paragraph Vector-based text and Levenshtein Distance-based text. If you train your solution using the Levenshtein Distance method, you don't need to use a word corpus in your clustering solution.

In this example scenario, you train your solution definition by using the third option referenced above.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Clustering** &gt; **Solution Definitions**.

2.  Open a trained clustering solution definition form.

3.  On the Advanced Solution Settings tab in the Related Links section of the form, select **New**.

    \[Omitted image "tf-idf-similarity-solution2.png"\] Alt text: This image shows how to select the Solution Parameters option for creating the parameter.

4.  Create a parameter record.

    1.  In the **Solution Parameters** field, select the search icon.

    2.  In the ML Solution Parameters screen, select **Levenshtein Distance**.

    \[Omitted image "configure-connect-component-levenshtein-distance-for-clustering1.png"\] Alt text: How to create the parameter record by selecting the Search button, and then selecting the Levenshtein Distance key's Short Description.

5.  Select **Submit**.

    The Advanced Solution Setting record screen refreshes.

    \[Omitted image "configure-connect-component-levenshtein-distance-for-clustering2.png"\] Alt text: The new Solution Parameter record you create from the values you just assigned.

6.  Select **Submit**.

    **Result:** Levenshtein Distance is configured for your clustering solution. Its solution parameter appears on the Advanced Solution Settings tab of your clustering definition form.

    \[Omitted image "configure-connect-component-levenshtein-distance-for-clustering3.png"\] Alt text: When you submit the record you created, the Levenshtein Distance solution parameter appears on your clustering solution definition form.

7.  Repeat steps 1-6 from the previous Levenshtein Distance example, except this time you're creating the **Minimum Neighbors** and **DBSCAN** solution parameters, which together enable the Connect Component feature.

    \[Omitted image "configure-connect-component-levenshtein-distance-for-clustering4.png"\] Alt text: The two remaining solution parameters you need to add to your clustering solution. These two final parameters enable the Connect Component feature.

    When you select, configure, and submit the **Minimum Neighbors** solution parameter, be sure to set the **User Inputs** field with a value of `1`. Only some parameters have a User Inputs field.

    \[Omitted image "configure-connect-component-levenshtein-distance-for-clustering4a.png"\] Alt text: How to add a value to the User Inputs field for the Minimum Neighbors parameter. In this scenario, you enter a value of 1.

    **Result:**

    Connect Component is configured for your clustering solution. Its two solution parameters appear on the Advanced Solution Settings tab of your clustering definition form, alongside the Levenshtein Distance parameter you configured in steps 1-6 of this procedure.

    \[Omitted image "configure-connect-component-levenshtein-distance-for-clustering5.png"\] Alt text: The three solution parameters you configured on the Advanced Solution Settings section of your clustering solution.


**Parent Topic:**[Configuring advanced settings for your ML solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/configuring-advanced-settings-ml-solutions.md)

**Related topics**  


[Create and train a clustering solution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/create-clustering-solution.md)

