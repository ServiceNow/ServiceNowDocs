---
title: Archive certificate tasks
description: In Version 1.1.7 Certificate Inventory and Management, the Data Archiver \[com.glide.auxdb\] plug-in performs daily operations to transfer data that is no longer required from primary tables to a designated set of archive tables.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manual flow for certificate requests, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Archive certificate tasks

In Version 1.1.7 Certificate Inventory and Management, the Data Archiver \[com.glide.auxdb\] plug-in performs daily operations to transfer data that is no longer required from primary tables to a designated set of archive tables.

## Before you begin

Role required: pki\_user or pki\_admin

## About this task

Certificate Inventory and Management actively checks and archives certificate tasks that surpass one year in age. To facilitate this, the corresponding plug-in must be enabled and activated for the scheduled archival tasks to execute. It's important to note that the Certificate Task Archive rule, which is included with the Certificate Inventory and Management application, is inactive by default.

## Procedure

1.  Activate **Certificate Task Rule**.

2.  Navigate to **Archive Rules** &gt; **Certificate Task Archive**.

3.  Select the **Active** check box.


## Result

Upon activation, this rule archives data from the Certificate Task table \[sn\_disco\_certmgmt\_certificate\_task\] under the following conditions:

-   State is Closed Complete
-   Last update occurred more than twelve months ago

