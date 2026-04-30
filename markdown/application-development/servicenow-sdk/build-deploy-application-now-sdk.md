---
title: Build and install an application with the ServiceNow SDK
description: Build and install a local application developed with the ServiceNow SDK on a ServiceNow instance.
locale: en-US
release: yokohama
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Develop applications, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Build and install an application with the ServiceNow SDK

Build and install a local application developed with the ServiceNow SDK on a ServiceNow instance.

## Before you begin

Add an application to your local system with the ServiceNow SDK. For more information, see [Adding applications with the ServiceNow SDK](../concept/creating-applications-servicenow-sdk.md).

Role required: admin

## About this task

This procedure uses the ServiceNow SDK command-line interface \(CLI\). From a command-line tool, enter `now-sdk --help` to get information about the available commands and global options. To get additional information about a command and its parameters, enter the command and `--help` or `-h`. For example, `now-sdk auth --help`. For more information about the CLI, see [ServiceNow SDK CLI](../reference/servicenow-sdk-cli-commands.md#).

**Note:** To build global applications with the ServiceNow SDK, you should use Node Package Manager \(npm\) as your package manager, especially if your application has more complex dependencies.

## Procedure

1.  In Visual Studio Code, open your scoped application directory.

2.  From the application directory, open an integrated Terminal window.

3.  Download changes to the application from the instance with the `transform` command to stay up to date with changes locally.

    ```cmd
    now-sdk transform --auth <alias>
    ```

    Changes to application metadata are downloaded and synchronized into source code. If metadata exists in the local application as both XML and source code, the XML version takes precedence when installed on the instance.

    **Note:** Updates to JavaScript modules aren't included when downloading application metadata from your instance.​

4.  Build your application using the `build` command.

    ```cmd
    now-sdk build
    ```

    The build artifacts are output to the `dist/app` directory, including the metadata as XML files in the `dist/app/update` directory.

5.  Install your application using the `install` command.

    ```cmd
    now-sdk install --auth <alias>
    ```

    **Warning:** If you set the `--reinstall` parameter to true with the `install` command, application metadata created by other developers on your instance can be removed. Any application metadata on your instance that is not present in the local installment package generated during the build process is removed during installment. Before building your application, use the `now-sdk transform` command to synchronize your local metadata with the metadata on your instance.


## Result

The application is updated on your instance to reflect your local changes. ServiceNow Fluent code is compiled into application metadata, and modules in the application are added to the EcmaScript Module \[sys\_module\] table on the instance.

**Note:** If you have previous versions of modules in the EcmaScript Module \[sys\_module\] table that aren't needed, re-installing an application removes previous versions of the application’s modules from the table.

**Parent Topic:**[Developing applications with the ServiceNow SDK](../concept/developing-applications-sdk.md)

