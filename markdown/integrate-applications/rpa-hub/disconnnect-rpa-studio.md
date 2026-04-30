---
title: Disconnect from an RPA Hub instance in RPA Desktop Design Studio
description: Disconnect a connected RPA Hub instance while you’re using the RPA Desktop Design Studio. You can then log in to the same instance with different credentials. For example, you might want to switch credentials when you use the Assign Bot Process feature.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring RPA Desktop Design Studio, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Disconnect from an RPA Hub instance in RPA Desktop Design Studio

Disconnect a connected RPA Hub instance while you’re using the RPA Desktop Design Studio. You can then log in to the same instance with different credentials. For example, you might want to switch credentials when you use the Assign Bot Process feature.

## Before you begin

Connect to an RPA Hub instance. For more information, see [Connect to an RPA Hub instance from RPA Desktop Design Studio](connect-studio-instance-rpa.md).

Role required: none

## About this task

You can't disconnect from an RPA Hub connected instance and then connect to a different RPA Hub instance when you're using Connection Manager in RPA Desktop Design Studio. If you want to connect to the same RPA Hub instance with another user role, you can select the **Disconnect** option in Connection Manager to disconnect from the instance. For example, let's consider a scenario where you were connected to the RPA Hub instance as a developer user. If you want to connect to the instance as an admin user, you can select the **Disconnect** option in Connection Manager and then log in to the same instance by using the admin user credentials.

## Procedure

1.  On the **Design** tab, select **Connect to instance**.

    The Connection Manager dialog box is displayed.

2.  Disconnect from the connected instance by selecting **Disconnect**.


## What to do next

Log in with new credentials. For more information about connecting to an instance, see [Connect to an RPA Hub instance from RPA Desktop Design Studio](connect-studio-instance-rpa.md).

**Related topics**  


[Assign bot process to an automation project](assign-bot-process.md)

