---
title: Preserve ML solutions during a system clone
description: Save your trained machine-learning \(ML\) solution data during a system clone.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Preserve ML solutions during a system clone

Save your trained machine-learning \(ML\) solution data during a system clone.

## Before you begin

Role required: clone\_admin or admin

## About this task

The system stores trained ML solutions as Attachment records. These records include your solution artifacts, such as solution definitions, template records, and predictive model statistics, all of which are required components of the Predictive Intelligence prediction functionality. To preserve these records, follow the high-level steps below each time you run a system clone.

**Note:**

For troubleshooting common issues with cloning solutions, see the [Predictive Intelligence Common issues \[KB0781893\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0781893) article in the Now Support Knowledge Base.

## Procedure

1.  Enter `sys_properties.list` in the application navigator to access the System Properties list.

2.  Ensure the **glide.platform\_ml.clone\_artifacts** system property is set to **True**.

3.  If you want to preserve only the ML solution records and not the numerous other records in the sys\_attachments table, exclude the sys\_attachments table from your clone run.

4.  Request a system clone.

    The system preserves your ML solution records during the system clone.


