---
title: Configure supervisor lists for service channels
description: Configure supervisor lists in a service channel to view the list of active work items across service channels and queues.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Channels in Workforce Optimization for ITSM, Channels in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Configure supervisor lists for service channels

Configure supervisor lists in a service channel to view the list of active work items across service channels and queues.

## Before you begin

Role required: sn\_channel\_mgmt.admin

## About this task

A database view that defines table joins is used for generating reports for a supervisor list. For example, you can create a database view that can join the Incident table to the Interaction and Metric tables. When you use this database view, and create a supervisor list to report on the active work items, you may include fields from any of these three tables. For more information, see [Working with database views for reporting](https://www.servicenow.com/docs/access?context=c_DatabaseViews&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

**Note:** You can configure three supervisor lists for each service channel. The first three lists with the lowest order number appear in Channel Management.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Channel Management** &gt; **Service Channels**.

2.  Select the service channel to which you want to add a supervisor list.

3.  Click the **Supervisor Lists** tab.

    **Note:** If you do not see the **Supervisor Lists** tab, you must [configure the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and the Reports related list.

4.  Click **New**.

5.  On the form, fill in the fields:

<table id="table_u41_bmm_1fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List Title

</td><td>

Display name for the list.

</td></tr><tr><td>

Tab Title

</td><td>

Title for the tab that appears in the manager workspace.

</td></tr><tr><td>

Service Channel

</td><td>

Service channel in which the list appears.

</td></tr><tr><td>

View Name

</td><td>

Database view for the service channel.

</td></tr><tr><td>

Order

</td><td>

Number that displays the order.**Note:** The first three lists with the lowest order number appear in Channel Management.

</td></tr></tbody>
</table>6.  Click **Submit**.

    The supervisor list is added to the service channels and appears in the Channels module in Manager Workspace.


**Parent Topic:**[Setting up Channels in Workforce Optimization for ITSM](../concept/setup-channels-configurable-workforce-optimization-itsm.md)

