---
title: Configure Proactive Customer Service Operations
description: Configure various aspects of Proactive Customer Service Operations based on the specific requirements of your organization.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Extend capabilities, Configure, Customer Service Management]
---

# Configure Proactive Customer Service Operations

Configure various aspects of Proactive Customer Service Operations based on the specific requirements of your organization.

## Before you begin

Role required: csm\_guided\_setup\_user or admin

## About this task

There are a sequence of tasks that enable you to configure Proactive Customer Service Operations. You can perform these tasks based on which plugin or application you have installed. This is noted at the top of each task.

**Note:** To use integration with Event Management, install the Proactive Customer Service Operations with Event Management plugin and the Event Management application from the ServiceNow store.

Event Management integration is only available if you are using the CSM Agent Workspace or the ServiceNow AI Platform interface.

To configure Proactive Customer Service Operations, use the Customer Service guided setup. The guided setup takes you through the entire setup and configuration process.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup**.

2.  On the Getting Started page of the guided setup, click **Get Started**

3.  In the Proactive Customer Service Operations category, view the list of tasks to configure the feature.

<table id="table_pz1_qqv_llb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate Proactive Customer Service Operations plugin \(com.snc.proactive\_cs\_ops\).**Note:** This is a ServiceNow Store plugin. You must install this plugin separately from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

Activate the Proactive Customer Service plugin to use Proactive Customer Service Operations.

</td></tr><tr><td>

Activate Proactive Customer Service Operations with Event Management plugin \(com.snc.proactive\_cs\_itom\).**Note:** This is a ServiceNow Store plugin. You must install this plugin separately from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td><td>

Activate the Proactive Customer Service Operations with Event Management plugin to enable integration with Event Management. This plugin automatically installs the Proactive Customer Service Operations plugin.

</td></tr><tr><td>

Install the Event Management application.

</td><td>

Install the Event Management application from the ServiceNow store.

</td></tr><tr><td>

Configure form views

</td><td>

Configure the form layout and related lists for the different views of the Case, Install Base Item, and Account forms to display the fields you require.

</td></tr><tr><td>

Activate an alert rule to automatically create a proactive case from an alert

</td><td>

Configure an alert rule to automatically create a proactive case when an incident is created from an alert that has one or more affected install base items.**Note:** This task is only applicable if you are using the integration with Event Management.

</td></tr><tr><td>

Configure proactive case flows

</td><td>

Automate workflows for proactive case creation to improve your operational efficiency and respond to customer issues faster.**Note:** This task is only applicable if you are using the integration with Event Management.

</td></tr></tbody>
</table>4.  To perform a task, click **Configure**.

    This button opens the page in your instance where the configuration is completed.


**Related topics**  


[Using Proactive Customer Service Operations](../task/use-pcso.md)

[View install base information from the Customer Service Portal](../task/view-install-base-info.md)

[Create a case for install base from the Customer Service homepage](../task/create-case-install-base.md)

[View the install base in CSM Configurable Workspace](../task/install-base-aw-csm.md)

[View sold product information in CSM Configurable Workspace](../task/view-sold-product-info-workspace.md)

