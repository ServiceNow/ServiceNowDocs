---
title: Add a connection in the Connections dashboard
description: Add a connection through the Connections dashboard.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using the Connections dashboard, Manage connections, Integration Hub, Workflow Data Fabric]
---

# Add a connection in the Connections dashboard

Add a connection through the Connections dashboard.

## Before you begin

Role required: connection\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer** and click the **Connections** tab.

2.  Locate the alias you want to add a connection to and select **Add Connection**.

    If there isn't an **Add Connection** option, the alias doesn't have a configuration template. To add a connection through the dashboard, the parent alias must have a template. Not all aliases have templates. Templates were first introduced in the Orlando release, so aliases from previous versions may not have them yet. If yours doesn't, you can set up your alias through the platform user interface instead. Select the **Advanced Setup** option to get started. For more information, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US). To learn more about templates, see [Connection and Credential configuration templates](https://www.servicenow.com/docs/access?context=spoke-configuration-template&version=australia&pubname=australia-platform-security&ft:locale=en-US).

3.  On the form, fill in the fields.

    The fields that appear on the form depend on which configuration template the parent alias has. For details on each specific template, visit [Connection and Credential configuration templates](https://www.servicenow.com/docs/access?context=spoke-configuration-template&version=australia&pubname=australia-platform-security&ft:locale=en-US).

4.  To submit the form, click **Create Connection**.


## Result

The alias card displays the new connection under the Connections list.

