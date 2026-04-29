---
title: Get help with ServiceNow CLI
description: See available commands, command options, and examples, or generate debug logging output.
locale: en-US
release: australia
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Get help with ServiceNow CLI

See available commands, command options, and examples, or generate debug logging output.

## Before you begin

-   [Install the ServiceNow CLI](download-cli.md)
-   [Configuring and managing your ServiceNow CLI connection profiles](configure-profile.md)
-   Role required: none

## About this task

In addition to the debug logging output option, the CLI logs all command executions to a log file at the following locations:

-   Linux and Mac: `~/.snc/.logs`.
-   Windows:`%USERPROFILE%\.snc\.logs`.

## Procedure

1.  To see the available commands and arguments, open your system's command-line tool and enter the command you need help with, followed by the `--help` argument.

    The following example displays help for the available top-level commands.

    ```
    $ snc --help
    ```

    The following example displays the available profile-specific commands.

    ```
    $ snc configure profile --help
    ```

    The CLI displays help for the requested command divided into eight sections:

    -   **Name**

        The name of the command.

        ```
        **Name**
             set
        ```

    -   **Description**

        The description of what the command does and its return values.

        ```
        **Description**
             Configure connection profiles. This command is interactive and will prompt you for each configuration value.
        ```

    -   **Synopsis**

        The basic syntax for using the command and its options.

        ```
        **Synopsis**
             snc configure profile set [arguments]
        ```

    -   **Available commands**

        The commands available under the current command group.

        ```
        **Available Commands**
         list    : Lists the configured connection profiles.
         refresh : Updates the available commands from the instance for the given profile.
         remove  : Removes the specified connection profile.
         set     : Configures connection profiles in order to communicate with an instance.
        ```

    -   **Command groups**

        The command groups available under the current command group.

        ```
        **Command Groups**
             profile : Set, view, and remove connection profiles.
        ```

    -   **Arguments**

        A description of each of the arguments the command accepts.

        ```
        **Arguments**
             -p, --profile string : Use a specific connection profile when executing a command.
        ```

    -   **Global arguments**

        The global arguments that the command accepts.

        ```
        **Global Arguments**
             -d, --debug Print logs to console.
             -h, --help Display detailed help information.
             -o, --output string Set the format for printing command output.
        ```

    -   **Examples**

        Examples of the requested command.

        ```
        **Examples**
           Create a new profile to save as the default:
              $ snc configure profile set
                 Host:
                 Login method:
                 Username:
                 Password:
                 Client id:
                 Client secret:
        ```

2.  To generate debug logging output, open your system's command-line tool and enter the command you want to debug, followed by the `--debug` argument.

    The following example generates debug logging output when trying to perform the operation.

    ```
    $ snc record delete --table incident --sysid 552c48888c033300964f4932b03eb092 --debug
    ```

    The CLI generates debug logging output when executing the command.


**Parent Topic:**[ServiceNow CLI](../concept/servicenow-cli.md)

