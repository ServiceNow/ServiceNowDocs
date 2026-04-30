---
title: Authenticate to a ServiceNow instance using basic authentication with the ServiceNow SDK
description: Use basic authentication to connect to a ServiceNow instance with the ServiceNow SDK.
locale: en-US
release: yokohama
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authenticate, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Authenticate to a ServiceNow instance using basic authentication with the ServiceNow SDK

Use basic authentication to connect to a ServiceNow instance with the ServiceNow SDK.

## Before you begin

Role required: admin

## About this task

This procedure uses the ServiceNow SDK command-line interface \(CLI\). From a command-line tool, enter `now-sdk --help` to get information about the available commands and global options. To get additional information about a command and its parameters, enter the command and `--help` or `-h`. For example, `now-sdk auth --help`. For more information about the CLI, see [ServiceNow SDK CLI](../reference/servicenow-sdk-cli-commands.md#).

## Procedure

1.  Create a local directory for your application.

2.  In Visual Studio Code, open the directory.

3.  From the application directory, open an integrated Terminal window.

4.  Specify the instance to authenticate to with the `auth` command.

    ```cmd
    npx @servicenow/sdk auth --add <instance>
    ```

    For example:

    ```cmd
    npx @servicenow/sdk auth --add https://myinstance.service-now.com
    ```

    **Note:** Using the `npx` command installs the ServiceNow SDK in your application directory instead of globally.

5.  Respond to the following series of prompts.

<table id="table_ivh_lzn_pdc"><thead><tr><th>

Prompt

</th><th>

Response

</th></tr></thead><tbody><tr><td>

`Type of authentication to use`

</td><td>

Select `basic`.

</td></tr><tr><td>

`Alias for these credentials`

</td><td>

Enter an alias for your credentials and the instance.The alias can be used for authentication with the `init`, `transform`, `dependencies`, and `install` commands.

</td></tr><tr><td>

`The username to authenticate with the instance`

</td><td>

Enter your username for the instance.You must be assigned the admin role.

</td></tr><tr><td>

`The password to authenticate with the instance`

</td><td>

Enter your password.

</td></tr></tbody>
</table>
## Result

The alias and credentials are stored in the device keychain or credential manager on your system and are set as the default credentials.

## What to do next

Add an application to your local system with the ServiceNow SDK. For more information, see [Adding applications with the ServiceNow SDK](../concept/creating-applications-servicenow-sdk.md).

**Parent Topic:**[Authenticating to a ServiceNow instance with the ServiceNow SDK](../concept/authenticate-instance-now-sdk.md)

