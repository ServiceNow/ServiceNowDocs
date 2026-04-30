---
title: Configure the default estimated resolution time
description: The Estimated Time to Resolve a Case regression definition is available by default. You can modify the default values of case fields, the case timeline, and the training frequency.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure settings for estimated time to resolve values, Estimated time to resolve a case, Machine learning solutions, Implement Intelligence, Configure, Customer Service Management]
---

# Configure the default estimated resolution time

The Estimated Time to Resolve a Case regression definition is available by default. You can modify the default values of case fields, the case timeline, and the training frequency.

## Before you begin

Role required: admin, ml\_admin

## About this task

The Estimated Time to Resolve a Case definition is available by default. You can train this available definition to complete a solution and make predictions. You can change some of the default settings such as the fields, a filter, and the training frequency. For more information on creating and training a solution, see the following.

[Create and train a regression solution.](https://www.servicenow.com/docs/access?context=create-regression-solution&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Regression** &gt; **Solution Definitions**.

2.  Click **Estimated Time to Resolve a Case**.

    In the Regression Definition screen, the **Table** field is autopopulated with the Case Report \[sn\_customerservice\_case\_report\] table. The **Output Field** field is autopopulated with the time taken to resolve a case in seconds.

    **Note:** If you have upgraded, you have to run a fix script in order to show the **Time to Resolve Numeric Value** column to display values for older cases. For more information, see [Configure settings for estimated time to resolve values](ettr-upgrade.md).

3.  To edit, add, or delete case attributes, modify the default values in the **Fields** field.

    The default case attributes are Short Description, Category, Assignment group, Assigned to, Priority, Product, Channel, Account, Service, Contact, Contract, and Description. These details are taken from the case record.

4.  Edit the **Filter** field if you want to modify the number of past months of cases to examine.

    The default value is 15 months.

5.  Edit the **Training Frequency** field if you want to modify the frequency of training.

    The default value is every 30 days.

6.  Either update the changes you made or update and retrain the solution.

    -   To update the changes you made, click **Update**.
    -   To update and retrain the solution, click **Update and Retrain**.

