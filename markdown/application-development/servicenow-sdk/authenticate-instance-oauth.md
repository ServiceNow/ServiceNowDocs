---
title: Authenticate to a ServiceNow instance using OAuth 2.0 with the ServiceNow SDK
description: Use OAuth 2.0 authentication to connect to a ServiceNow instance with the ServiceNow SDK.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Authenticate, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Authenticate to a ServiceNow instance using OAuth 2.0 with the ServiceNow SDK

Use OAuth 2.0 authentication to connect to a ServiceNow instance with the ServiceNow SDK.

## Before you begin

To use OAuth 2.0 authentication, your instance must have ServiceNow IDE \(version 1.1 or later\) installed or have the required XML configuration imported. By default, instances on the Australia release include ServiceNow IDE version 1.1.4 and support using OAuth 2.0 authentication with the ServiceNow SDK.

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

Select `oauth`.

</td></tr><tr><td>

`Alias for these credentials`

</td><td>

Enter an alias for your credentials and the instance.The alias can be used for authentication with the `init`, `transform`, `dependencies`, and `install` commands.

</td></tr></tbody>
</table>    The ServiceNow SDK opens a web browser to authenticate with the instance.

6.  Navigate to the web page that opens and log in to the instance if you aren't currently logged in.

7.  Select **Accept** to allow the ServiceNow SDK to connect to the instance.

    The page refreshes and includes an authentication code.

8.  Select **Copy** to copy the authentication code provided.

9.  In the command line, paste the authentication code.


## Result

The alias and credentials are stored in the device keychain or credential manager on your system and are set as the default credentials.

## What to do next

Add an application to your local system with the ServiceNow SDK. For more information, see [Adding applications with the ServiceNow SDK](../concept/creating-applications-servicenow-sdk.md).

**Parent Topic:**[Authenticating to a ServiceNow instance with the ServiceNow SDK](../concept/authenticate-instance-now-sdk.md)

