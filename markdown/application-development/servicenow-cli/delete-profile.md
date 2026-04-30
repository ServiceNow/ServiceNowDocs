---
title: Remove a profile
description: Remove a named connection profile that you no longer need from the configuration file.
locale: en-US
release: xanadu
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring and managing your ServiceNow CLI connection profiles, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Remove a profile

Remove a named connection profile that you no longer need from the configuration file.

## Before you begin

A default profile must first exist to communicate with an instance.

## About this task

You cannot remove the default connection profile using this command. To remove the default connection profile, edit the configuration file manually.

## Procedure

1.  Open your system's command-line tool and execute this command.

2.  Specify the name of the named profile in the *profile-name* argument.

    ```
    $ snc configure profile remove [--profile profile-name]
    ```


## Result

The CLI removes the specified profile from the configuration file.

**Parent Topic:**[Configuring and managing your ServiceNow CLI connection profiles](configure-profile.md)

