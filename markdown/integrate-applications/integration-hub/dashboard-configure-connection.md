---
title: Configure a connection in the Connections dashboard
description: Configure a connection through the Connections dashboard.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using the Connections dashboard, Manage connections, Integration Hub, Workflow Data Fabric]
---

# Configure a connection in the Connections dashboard

Configure a connection through the Connections dashboard.

## Before you begin

Role required: connection\_admin or admin

## About this task

When you transfer an alias or promote it to production, its underlying connection information doesn't get transferred with it. In this situation, the connection is in an unconfigured state and must be reconfigured before you can use it.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer** &gt; **** and click the **Connections** tab.

2.  Locate the alias that you want to add a connection to and click **View Details**.

3.  In the detailed view, locate the connection that you want to configure and click **Configure**.

4.  On the Configure Connection form, fill in the fields.

    The fields that appear on the form depend on which configuration template the parent alias has. For details on each specific template, see [Connection and Credential configuration templates](https://www.servicenow.com/docs/access?context=spoke-configuration-template&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    Configuring a connection through the dashboard requires the parent alias to have a configuration template. If yours doesn't, clicking **Configure** opens the Connection and Credential Alias record for your alias instead of the Configure Connection form. For more information about configuring your connection in the Connection and Credential Alias record, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

5.  To submit the form, click **Configure**.


## Result

The detailed view displays the new connection in the Connections list.

