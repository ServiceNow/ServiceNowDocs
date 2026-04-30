---
title: ServiceNow CLI
description: The ServiceNow CLI is a command-line interface that lets you perform instance operations from your local system. You can extend the CLI to include new commands that meet your application's needs.
locale: en-US
release: xanadu
product: ServiceNow CLI
classification: servicenow-cli
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Building low-code applications, Developing your application, Building applications]
---

# ServiceNow CLI

The ServiceNow CLI is a command-line interface that lets you perform instance operations from your local system. You can extend the CLI to include new commands that meet your application's needs.

## Benefits

The ServiceNow CLI lets you:

-   Perform basic CRUD operations on records in your instance.
-   Develop custom components and deploy them to your instance to personalize a UI.
-   Create custom commands that enable you to manage custom applications from the command line.
-   Use the ServiceNow CLI in scripts to simplify setup tasks and operational activities.

## Architecture

Commands are stored in a table on the instance you are connected to. When the ServiceNow CLI connects to the instance, it receives all the available commands supported by that instance.

![Communication flow between Servicenow CLI and the instance.](../image/cli-arch.png)

Commands map to a REST endpoint that executes asynchronously. For more information, see [Create a custom command in ServiceNow CLI](../task/create-command.md).

## Activating ServiceNow CLI

Install ServiceNow CLI by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Configuration file

The ServiceNow CLI stores profile information in a `config.json` file which, by default, is stored in your home directory at the following path:

-   Linux and Mac: `~/.snc/config.json`
-   Windows: `%USERPROFILE%\.snc\config.json`

The CLI uses this file to determine what information to use to connect to an instance, and what settings to use to generate output. By default, the ServiceNow CLI uses the settings found in the default profile to connect to an instance. To use alternate settings, you can create and reference additional named profiles. For more information, see [Configuring and managing your ServiceNow CLI connection profiles](../task/configure-profile.md).

The following example shows a  configuration  file with a default profile and a named profile. Each profile can use different credentials and specify different hosts and output formats.

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
         },
      "user1":{
         "host":"https://otherinstance.service-now.com",
         "loginmethod":"basic",
         "username":"user1",
         "output":"yaml",
         "hostversion":"Paris",
         "appversion":"1.0"
         }
      }
}
```

**Note:** Sensitive credential information is only stored in the OS keychain, not in the configuration file.

## Command structure

ServiceNow CLI commands follow this structure:

1.  The base call to the `snc` program.
2.  The top-level command group followed by any child command groups.
3.  The command that specifies which operation to perform.
4.  General CLI arguments required by the operation. You can specify arguments in any order.

```
$ snc <command-group> <command> [arguments]
```

Arguments can take various types of input values, such as numbers, strings, and JSON objects. The types supported depend on the command you specify.

## Argument values

Many argument values in the ServiceNow CLI are simple string or numeric values, such as the table and table name in the following example.

```
$ snc record create --table incident --data "{short_description: 'New Incident'}"
```

You can surround strings that do not contain any space characters with quotation marks or not. However, you must use quotation marks around strings that include one or more space characters.

## Output formats

The ServiceNow CLI supports four output formats:

-   `json`: The output is formatted as JSON. This is the default.

    ```
    
    {
       "default": {
          "appversion": "1.0.8",
          "host": "https://myinstance.service-now.com",
          "hostversion": "Paris",
          "loginmethod": "basic",
          "output": "json",
          "username": "admin"
       },
       "user1": {
          "appversion": "1.0.8",
          "host": "https://otherinstance.service-now.com",
          "hostversion": "Paris",
          "loginmethod": "basic",
          "output": "yaml",
          "username": "admin"
       }
    }
    ```

-   `yaml`: The output is formatted as YAML. Use YAML to handle the output with services and tools that emit or consume YAML-formatted strings.

    ```
    default:
       appversion: 1.0.8
       host: https://myinstance.service-now.com
       hostversion: Paris
       loginmethod: basic
       output: json
       username: admin
    user1:
       appversion: 1.0.8
       host: https://otherinstance.service-now.com
       hostversion: Paris
       loginmethod: basic
       output: yaml
       username: admin
    ```

-   `text`: The output is formatted as multiple lines of tab-separated string values. Use this output with traditional UNIX text tools such as grep, sed, and awk, and the text processing performed by PowerShell.

    ```
    default   https://myinstance.service-now.com   Paris   1.0.8   basic   admin   json 
    user1   https://otherinstance.service-now.com   Paris   1.0.8   basic   admin   yaml
    ```

-   `table`: The output is formatted as a table which presents the information in a human-readable format.

    ```
    NAME   HOST   HOST   VERSION   APP   VERSION   LOGIN   METHOD   USERNAME   OUTPUT 
    -------------------------------------------------------------------------------
    default   myinstance   Paris   1.0.8   basic   admin   json 
    user1   otherinstance   Paris   1.0.8   basic   admin   yaml
    ```

-   `none`: The CLI does not print the output to the console. Success, error, and progress messages still display.

You can specify command output in two ways:

-   **Use the `output` option in a named profile in the configuration file**

    The following example sets the default output format to text.

    ```
    {
        "profiles":{
           "default":{
              "output":"text"
          }
    }
    ```

-   **Use the `--output` argument on the command line**

    The following example sets the output of a single command to JSON. This option on the command overrides any currently set value in the configuration file.

    ```
    $ snc record query --table incident --query ‘active=true’ --output json
    ```


-   **[Install the ServiceNow CLI](../task/download-cli.md)**  
Install the ServiceNow CLI on a Mac, Windows, or Linux machine.
-   **[Configuring and managing your ServiceNow CLI connection profiles](../task/configure-profile.md)**  
Create a connection profile to connect with your instance, view connection profiles, refresh your connection and available commands, or delete profiles you no longer need.
-   **[Get help with ServiceNow CLI](../task/get-help.md)**  
See available commands, command options, and examples, or generate debug logging output.
-   **[Perform record operations using ServiceNow CLI](../task/manage-records.md)**  
Create, read, update, delete, and query records in your instance using the ServiceNow CLI command-line tool.
-   **[Create a custom command in ServiceNow CLI](../task/create-command.md)**  
Manage your custom application from the command line by creating custom commands in the ServiceNow CLI.
-   **[Manage ServiceNow CLI extensions](../task/find-extensions.md)**  
Add extensions to the ServiceNow CLI to load additional functionality and commands, update existing extensions, or remove extensions you no longer need.
-   **[ServiceNow CLI available commands](../reference/sn-cli-commands.md)**  
Commands and command arguments available to the base system ServiceNow CLI.
-   **[Commands installed with CMDB Application CLI and API](../reference/cmdb-cli-commands.md)**  
Commands and command groups available to the ServiceNow CLI when the app-cmdb-api-cli plugin is installed.

**Parent Topic:**[Building low-code applications](../../custom-application/reference/building-low-code-applications-with-app-engine.md)

