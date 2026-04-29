---
title: View profiles
description: View all connection profiles set in the configuration file, or view information about a specific profile.
locale: en-US
release: australia
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring and managing your ServiceNow CLI connection profiles, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# View profiles

View all connection profiles set in the configuration file, or view information about a specific profile.

## Before you begin

A default profile must first exist to communicate with an instance.

Role required: none.

## About this task

For each profile, the CLI displays host information, version details, user name, login method, and preferred output format. It does not display sensitive information such as passwords or client IDs.

## Procedure

1.  Open your system's command-line tool and execute this command.

    Include the `[--profile profile-name]` argument to view the connection information for a single profile. Otherwise, the CLI lists information for all profiles.

    ```
    $ snc configure profile list [--profile profile-name]
    ```

    This command displays all configured profiles.

    ```
    $ snc configure profile list
    ```

    The CLI provides the following output.

    ```
    {
       "profiles":{
          "default":{
          "host":"https://myinstance.service-now.com",
          "loginmethod":"basic",
          "username":"admin",
          "output":"json",
          "hostversion":"Paris",
          "appversion":"1.0"
       }
    }
    ```


**Parent Topic:**[Configuring and managing your ServiceNow CLI connection profiles](configure-profile.md)

