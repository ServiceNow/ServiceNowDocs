---
title: Create a database index for the Cloud Events table
description: Create a database index from the specified columns of the Cloud Events \[sn\_cmp\_cloud\_event\] table to improve the AWS cloud event processing performance.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [AWS events-driven discovery, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a database index for the Cloud Events table

Create a database index from the specified columns of the Cloud Events \[sn\_cmp\_cloud\_event\] table to improve the AWS cloud event processing performance.

## Before you begin

Ensure that the scope is set to Cloud Provisioning and Governance.

Role required: admin

## About this task

After upgrading Cloud Provisioning and Governance to the Utah release, create a database index from the specified columns of the Cloud Events \[sn\_cmp\_cloud\_event\] table. The database index helps to improve the Amazon Web Services \(AWS\) event processing performance of the instance. If you've started using Cloud Provisioning and Governance with the Utah release, the database index is automatically created on application installation.

Instead of manually creating the database index, you can use a scheduled job to create it. For more information, see [ServiceNow® events-driven discovery: Create a database index for the Cloud Events table \(KB1207069\).](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1207069)

You can also Scale the cloud event schedulers to improve the Amazon Web Services \(AWS\) event processing rate of the ServiceNow instance. For more information, see [Scale the AWS cloud event schedulers](scale-aws-cloud-event-schedulers.md).

## Procedure

1.  Navigate to `https://<instance name>.service-now.com/sn_cmp_cloud_event_list.do`

2.  Select **Column options** &gt; **Configure** &gt; **Table**.

3.  Select the **Database Indexes** related list.

4.  Select **New**.

5.  From the available columns list, select the following columns in the stated order.

    1.  **State**
    2.  **Process Id**
    3.  **Resource ID**
6.  Select **Create Index**.

7.  Select an option to specify whether you want to receive a notification on index creation.

8.  Select **OK**.

9.  Rename the new index for easy identification.


