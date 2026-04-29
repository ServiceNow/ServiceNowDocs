---
title: Manage ServiceNow CLI extensions
description: Add extensions to the ServiceNow CLI to load additional functionality and commands, update existing extensions, or remove extensions you no longer need.
locale: en-US
release: australia
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Manage ServiceNow CLI extensions

Add extensions to the ServiceNow CLI to load additional functionality and commands, update existing extensions, or remove extensions you no longer need.

## Before you begin

Role required: none.

## Procedure

1.  Find available extensions.

    1.  Open your system's command-line tool and execute this command.

        ```
        $ snc extension list-available -o table
        ```

        The system lists available extensions and associated details.

        ```
        NAME       DESCRIPTION                                    VERSION            INSTALLED 
        --------------------------------------------------------------------------------------
        ui-component        Build and deploy components                  19.0.0-alpha.15     false 
        ```

2.  Install an extension.

    1.  Open your system's command-line tool and execute this command.

        ```
        $ snc extension add --name <extension-name>
        ```

3.  Update an extension.

    1.  Open your system's command-line tool and execute this command.

        ```
        $ snc extension update --name <extension-name>
        ```

4.  Remove an extension.

    1.  Open your system's command-line tool and execute this command.

        ```
        $ snc extension remove --name <extension-name>
        ```


**Parent Topic:**[ServiceNow CLI](../concept/servicenow-cli.md)

