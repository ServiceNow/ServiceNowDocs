---
title: Set up your environment
description: Prepare your local environment by installing the Node.js JavaScript runtime environment, Node package manager \(npm\), and the ui-component extension. These tools enable you to develop and build components locally and deploy them to your instance.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create custom components using ServiceNow CLI, Builder library, Developing your application, Building applications]
---

# Set up your environment

Prepare your local environment by installing the Node.js JavaScript runtime environment, Node package manager \(npm\), and the ui-component extension. These tools enable you to develop and build components locally and deploy them to your instance.

## Before you begin

The ui-component extension only supports these operating systems.

-   Windows 10
-   MacOS Yosemite and later
-   Linux CentOS v7.5

Role required: none

## Procedure

1.  Install Node.js version 12.16.1 or greater.

    npm automatically installs as part of the Node.js package. Node.js is a JavaScript runtime environment that enables you to execute JavaScript locally. npm is the default JavaScript package manager for Node.js. For more information, see [Node.js](https://nodejs.org) and [npmjs.com](https://www.npmjs.com/).

2.  Add the ui-component extension to the ServiceNow CLI.

    1.  Open your system's command-line tool and execute this command.

        ```
        $ snc extension add --name ui-component
        ```

3.  Verify the installation by running an extension command with the `--help` argument.

    ```
    $ snc ui-component --help
    ```

    The CLI displays a list of available commands. See [Get help with ServiceNow CLI](../../servicenow-cli/task/get-help.md).


## What to do next

[Set up your project](setup-component-project.md).

**Parent Topic:**[Create custom components using ServiceNow CLI](../concept/custom-components.md)

**Related topics**  


[Create custom components using ServiceNow CLI](../concept/custom-components.md)

[ServiceNow CLI](../../servicenow-cli/concept/servicenow-cli.md)

