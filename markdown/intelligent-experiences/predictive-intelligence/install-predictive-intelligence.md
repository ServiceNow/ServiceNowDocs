---
title: Install Predictive Intelligence
description: Activate Predictive Intelligence on your instance and get started with basic configuration.Implement initial setup and configuration steps for Predictive Intelligence to train a machine-learning \(ML\) algorithm to make predictions based on your past record data.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Predictive Intelligence, Enable AI experiences]
---

# Install Predictive Intelligence

Activate Predictive Intelligence on your instance and get started with basic configuration.

## Before you begin

Role required: admin

## About this task

The Predictive Intelligence plugin \(com.glide.platform\_ml\) is included in the base system, but if necessary you can use the following procedure to activate it.

Other related plugins and store applications are available. For example, Predictive Intelligence for Field Service Management \(com.snc.fsm\_ml\) provides solutions relevant to FSM. Some of these plugins may require a separate license.

When you activate the Predictive Intelligence plugin for the first time on your instance, the system launches a Homepage. The Homepage provides an overview of your solution definitions in the classification, similarity, clustering, and regression frameworks. You can create, train, and test solutions directly on the Homepage. A summary of the latest trained solution is also available.

## Procedure

1.  Navigate to **System Definition** &gt; **Plugins**.

2.  Use the search bar to locate the Predictive Intelligence \(com.glide.platform\_ml\) plugin.

3.  Select **Install** and then in the Activate Plugin dialog box, select **Activate**.

    When you activate a plugin, any dependent plugins are activated automatically.

4.  Confirm that the activation has successfully created a sharedservice.worker user.

    When training your solutions, Predictive Intelligence operates as this user.

    **Note:** The sharedservice.worker user includes the following roles:

    -   platform\_ml\_read
    -   platform\_ml\_write
    -   platform\_ml\_create
    These roles are required to create, train, and view solutions. They are internal roles and not meant to be edited or assigned to other users.


## Implement Predictive Intelligence

Implement initial setup and configuration steps for Predictive Intelligence to train a machine-learning \(ML\) algorithm to make predictions based on your past record data.

### Before you begin

Role required: admin or ml\_admin

### About this task

The training process requires sending record data to a training service in the nearest datacenter. Since every datacenter has its own dedicated training server and the data doesn't leave the datacenter, this service is also available to customers who have data sovereignty requirements. For more information on this process, see [Explore Predictive Intelligence](../concept/predictive-intelligence.md).

For frequently asked questions regarding initial configuration and setup, see [KB0781894](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0781894).

### Procedure

1.  Activate Predictive Intelligence on a non-production instance.

2.  From your production instance, export the records that you want your Predictive Intelligence solutions to process.

    For example, export 12 months of incident records to a non-production instance.

3.  On the non-production instance, import the records you exported.

4.  On the non-production instance, review the default solution definition records to determine if the filter, input fields, and output field are sufficient to predict your incident or task records.

    If necessary, [create a solution definition](create-solution-definition.md) for each record set you want to predict.

5.  On the non-production instance, train the solution definition records.

6.  Test the solution predictions on the non-production instance by either creating test records or importing more records from production.

7.  For classification solutions, review the prediction reports to determine the accuracy and coverage of your solution and individual classes.

8.  For similarity solutions, review the similarity examples to update the similarity score threshold if needed.

9.  If necessary, update the solution definition filter to include more or different training records.

10. Retrain and retest any updated solution definition records.

11. When you are satisfied with your solutions, activate Predictive Intelligence on your production instance.

12. Recreate any custom solution definition records and train the solution, or import the solution from your non-production instance to your production instance.


**Related topics**  


[Create and train a classification solution](create-solution-definition.md)

[Create and train a similarity solution](create-similarity-solution.md)

