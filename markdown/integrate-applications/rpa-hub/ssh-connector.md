---
title: Secure Shell \(SSH\) connector
description: Secure Shell \(SSH\) connector helps establish an SSH connection to a remote server and execute commands.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Secure Shell \(SSH\) connector

Secure Shell \(SSH\) connector helps establish an SSH connection to a remote server and execute commands.

In the UNIX environment, SSH is the preferred way to access remote systems. In an automation workflow, when you need to connect to a remote system and perform an operation, you can use SSH connector methods to accomplish the task efficiently.

The SSH connector is available as a plugin by default in RPA Desktop Design Studio from 12.0.X versions. Add the SSH plugin from the Plugins Manager. For more information about adding the SSH plugin, see [Manage plugins in RPA Desktop Design Studio](../task/install-plugins-rpa-studio.md).

![Add The SSH plugin in the Plugins Manager](../image/ssh-plugin-add.png "SSH plugin")

Use the different methods available in the connector to perform activities such as establishing an SSH connection, executing command over an established connection, and disconnecting the session that was established using Connect method.

-   To use a connector in RPA Desktop Design Studio, see [Use a connector in RPA Desktop Design Studio](../task/use-connector.md). Add the Secure Shell connector in the Global Objects.

    ![Add Secure Shell connector in the Global Objects](../image/ssh-connector-add-global-object.png "Add Secure Shell connector in the Global Objects")

-   To learn more about the various methods in the SSH connector, see [Secure Shell \(SSH\) connector methods](../reference/connector-ssh-methods.md).

-   **[Secure Shell \(SSH\) connector methods](../reference/connector-ssh-methods.md)**  
The Secure Shell \(SSH\) connector methods establish an SSH connection, execute commands over the established connection, and disconnect the session.

**Parent Topic:**[Connectors](connectors.md)

