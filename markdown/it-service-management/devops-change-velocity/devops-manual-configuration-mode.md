---
title: Manual configuration mode in DevOps
description: As an alternative to making a connection using the standard setup process, you can use manual configuration mode to set up a webhook manually.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Manual configuration mode in DevOps

As an alternative to making a connection using the standard setup process, you can use manual configuration mode to set up a webhook manually.

For example, if you do not have admin privileges for a tool \(to allow automatic configuration the webhook URL\), you can send an email to the admin of the tool requesting the ServiceNow instance be added to the webhook. Once the instance is added, you can **Enter Manual Configuration Mode** and change the **Connection state** field to Connected \(to connect manually\).

This way you only need read-only permission to the tool. Once the connection is made, click **Exit Manual Configuration Mode**.

**Note:** The **Connection state** field can only be edited in manual configuration mode.

All planning, coding, and orchestration tool connections support manual configuration mode.

**Note:** Connection state automatically changes to disconnected if there is a change in configuration, such as URL, credentials, alias, type, or MID Server settings.

**Parent Topic:**[Managing DevOps Change Velocity](using-devops-change-velocity.md)

