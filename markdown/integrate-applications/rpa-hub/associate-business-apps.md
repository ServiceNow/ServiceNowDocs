---
title: Assign a business application to a bot process in RPA Hub
description: Assign a business application to a bot process for an effective event correlation or to get information about assigned business applications. For example, you might want to see information about the SAP application.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Adding details for your bot process, Configuring a bot process record, Use, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Assign a business application to a bot process in RPA Hub

Assign a business application to a bot process for an effective event correlation or to get information about assigned business applications. For example, you might want to see information about the SAP application.

## Before you begin

Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Verify that the business application exists on this ServiceNow instance. To add a new business application, navigate to **All** &gt; **Self-service** &gt; **Business Applications**.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

You can add any credentials for assigned business applications. If you remove a business application, the associated application credentials are also removed.

You can't remove or edit an associated business application for a published or a retired bot process.

An RPA business user \[sn\_rpa\_fdn.rpa\_business\_user\] can view the business applications.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process that you want to associate a business application to.

5.  On the **Business Applications** tab, select **Add**.

6.  On the **Available Business Applications** tab, select the required business application.

7.  Select **Add**.

8.  Select **Save**.

9.  To remove a business application, select the business application, and select **Remove**.


