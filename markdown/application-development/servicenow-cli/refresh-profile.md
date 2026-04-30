---
title: Refresh your connection
description: Update the available commands from the instance for the given profile. Refresh your connection after modifying any of the commands on the corresponding instance in order to keep the CLI up-to-date.
locale: en-US
release: yokohama
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring and managing your ServiceNow CLI connection profiles, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Refresh your connection

Update the available commands from the instance for the given profile. Refresh your connection after modifying any of the commands on the corresponding instance in order to keep the CLI up-to-date.

## Before you begin

A default profile must first exist to communicate with an instance.

## Procedure

1.  Open your system's command-line tool and execute this command.

    Include the `[--profile profile-name]` argument to refresh connection information from a named profile. If you do not include the argument, the CLI refreshes the default profile.

    ```
    $ snc configure profile refresh [--profile profile-name]
    ```


## Result

The CLI connects to the instance in the designated connection profile and updates any commands that may have changed.

**Parent Topic:**[Configuring and managing your ServiceNow CLI connection profiles](configure-profile.md)

