---
title: Configure record categorization
description: Activate the required plugins, import training data, and create and train a model to predict field values for case and interaction records.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Task Intelligence for Customer Service, Task Intelligence for Customer Service, Machine learning solutions for Customer Service Management, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Configure record categorization

Activate the required plugins, import training data, and create and train a model to predict field values for case and interaction records.

<table id="table_ih2_hfc_5rb"><thead><tr><th>

Step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ensure that your instance is set up for Predictive Intelligence \(PI\).

</td><td>

Predictive Intelligence is a ServiceNow platform feature that provides a layer of artificial intelligence, which serves as a framework for machine learning models. For more information, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

Activate the Task Intelligence for Customer Service application \(com.snc.csm\_ml\_task\).

</td><td>

The Task Intelligence for Customer Service application enables customers to create and train categorization machine learning models. This application automatically activates the following plugins:

-   Predictive Intelligence for Customer Service Management \(com.snc.csm\_ml\)
-   Customer Service \(com.sn\_customerservice\)
-   Skills Management \(com.snc.skills\_management\)
-   Dynamic Translation \(com.glide.dynamic\_translation\)
-   ServiceNow Language Detection Service Spoke \(com.glide.language\_detection\_spoke\)
-   Predictive Intelligence - Task Intelligence \(com.glide.platform\_ml\_task\)
-   Admin Center for Task Intelligence \(com.sn\_ti\_admin\)

</td></tr><tr><td>

Import a training data set.

</td><td>

You can use the record categorization feature with the Case table \[sn\_customerservice\_case\], tables that extend the Case table, and the Interaction table \[interaction\].

 It is recommended that you import a training data set into the desired table to support the initial training of a categorization model.

**Note:** This data should include case types if you have tables that extend the Case table.

 The training data set should be tailored to the fields that you want to predict. It should also include additional records that have the correct labels \(for example, the expected field values\) for the fields being predicted.

 Creating a training data set enables you to leverage your own data to train the algorithm to predict on the fields you select.

1.  Identify the table and the fields that you want your model to predict.
2.  Select the table and records for training the model.
3.  Identify the fields in the selected table as the input values to be used for training the model.

</td></tr><tr><td>

Set up and deploy at least one categorization model.

</td><td>

For details, see [Create a model to predict record fields](csm-task-intel-create-cat-solution.md).

</td></tr></tbody>
</table>**Related topics**  


[Record categorization](case-categorization-overview.md)

