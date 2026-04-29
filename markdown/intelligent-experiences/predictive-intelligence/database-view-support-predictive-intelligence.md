---
title: Database View support for Predictive Intelligence
description: Use database views to join two or more tables as input for your Machine Learning \(ML\) solution.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Database View support for Predictive Intelligence

Use database views to join two or more tables as input for your Machine Learning \(ML\) solution.

## Using database views in an ML solution

Database views help expand the amount of fields your solution can use for training. By using more than one table in your ML solution definition form, you can access more input data to help enrich the solution outcome.

Database views enable you to join two or more tables into one consolidated view. For this to work in an ML solution you must first create the database view. See [Database views](https://www.servicenow.com/docs/access?context=c_DatabaseViews&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Database views are supported in all four of the Predictive Intelligence capability frameworks: classification, similarity, clustering, and regression.

## A database view example for Predictive Intelligence

In the following example scenario, you've created a database view for use in an ML similarity solution. The image below shows the database view record you've created, including its **Name** and **Label**.

![The database view you created so you can use it to enhance the data outcome of a similarity solution you created](../images/database-view-support-predictive-intelligence1.png)

When you click the record **Name**, its content appears, as shown in the image below. Within the database view content, the five Knowledge Base tables you've joined to the view are listed. Most of these tables contain different Knowledge article template types, such as an FAQ or a How To article.

When a database view is used as input to a similarity solution, each of the tables that constitute the view must have at least the required number of records set in the configuration of your ServiceNow instance. The default minimum number required is 10,000. For example, the **Knowledge View** database view has five tables and each table must have 10,000 records. If a table doesn't have 10,000 records, you may not see the results from that table. If you must change that value, contact Customer Support.

![The five tables you included in your database view](../images/database-view-support-predictive-intelligence2.png)

In the image below you can see the similarity solution definition record you've already created, which you plan to associate to your database view. When you click the **Label** for your similarity record, its Similarity Definition form appears.

![The ML similarity solution definition you created.](../images/database-view-support-predictive-intelligence3.png)

Similarity Definition forms compare your existing table records based on their similarity by using a table in the **Table** field and another table in the **Test Table** field.

To use a database view in your similarity solution, instead of selecting a table in the **Table** field, you select the database view you created, which in this example scenario is the **Knowledge View** database view. This configuration increases the number of records your solution uses in training because the system compares and processes five tables of data instead of one.

![Your database view configured to your similarity solution](../images/database-view-support-predictive-intelligence4.png)

**Parent Topic:**[Configure Predictive Intelligence](../task/configure-predictive-intelligence.md)

