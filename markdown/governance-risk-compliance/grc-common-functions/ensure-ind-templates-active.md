---
title: Ensure that all the appropriate indicator templates are activated
description: When you download the GRC: Technology Controls Monitoring Accelerator application, all indicator templates are available, but they are not yet active. Before activating them, you need to ensure that you have the necessary applications activated and can access the tables that are mapped to the indicator templates.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Technology Controls Monitoring Accelerator, GRC use case accelerators, Common GRC features, Governance, Risk, and Compliance]
---

# Ensure that all the appropriate indicator templates are activated

When you download the GRC: Technology Controls Monitoring Accelerator application, all indicator templates are available, but they are not yet active. Before activating them, you need to ensure that you have the necessary applications activated and can access the tables that are mapped to the indicator templates.

## Before you begin

Role required: admin

## About this task

Starting with version 12.0.1 of the Technology Controls Monitoring Accelerator application, several of the indicators that were Manual were converted to either Basic or Scripted. This added automation makes many of the tasks associated with continuous monitoring easier.

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**.

2.  Locate and open **GRC: Update Plugin Activation Status in Indicator-Plugin Mapping table**.

    ![Scheduled Script Execution](../image/sched-job.png "Scheduled Script Execution")

3.  Click **Execute Now**.

    The job scans the Indicator Template to Plugin Mapping table \[sn\_grc\_ind\_template\_plugin\_mapping\_details\] on your instance, and 1\) determines which applications that can use the Technology Controls Monitoring Accelerator for monitoring indicator templates are installed on your instance, and 2\) automatically activates the indicator templates that are mapped to tables in those applications.

    **Note:** You must repeat this process any time you upgrade this application.


**Parent Topic:**[Technology Controls Monitoring Accelerator](../concept/tech-controls-monitoring-accel.md)

