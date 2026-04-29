---
title: Export trained solutions to production
description: Refine and test your ML solutions iteratively on a non-production instance, and then use update sets to export the changes to your production instance. This practice mitigates the risk of retraining solutions on your live production instance.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Export trained solutions to production

Refine and test your ML solutions iteratively on a non-production instance, and then use update sets to export the changes to your production instance. This practice mitigates the risk of retraining solutions on your live production instance.

## Before you begin

Prior to testing on a test instance, ensure that the instance hosts recently-cloned data from your production instance so that the solutions you train on the test instance remain valid when you export them to production.

Role required: admin or ml\_admin

## About this task

Plan your changes carefully, and remember that update sets match records based on the system ID \[sys-id\] and not the version number. Note that moving solutions to instances can sometimes deliver unpredictable results. If you run into such an issue, retrain the solution again, which takes 5 minutes per solution. For more information on update sets, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=australia&pubname=australia-application-development&ft:locale=en-US) .

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions** or **Predictive Intelligence** &gt; **Similarity** &gt; **Solution Definitions**.

2.  Click the name of your trained ML Solution Definition record to open it.

3.  In the Related Links section, click **Add solutions to the current update set**.

4.  Click **Update**.


## Result

Your trained ML solution artifacts, such as solution definitions, template records, and predictive model statistics, are added to the current update set.

## What to do next

Depending on where you are in your solution testing, schedule your update set for export to another non-production instance for further testing, or on to production.

**Note:** After you export a similarity solution, click **Refresh similarity window \(Required after Solution Import\)** in the Related Links section of the corresponding ML Solution Definition form.

**Parent Topic:**[Configure Predictive Intelligence](configure-predictive-intelligence.md)

