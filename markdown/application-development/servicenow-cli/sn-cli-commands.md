---
title: ServiceNow CLI available commands
description: Commands and command arguments available to the base system ServiceNow CLI.
locale: en-US
release: xanadu
product: ServiceNow CLI
classification: servicenow-cli
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# ServiceNow CLI available commands

Commands and command arguments available to the base system ServiceNow CLI.

## Global command arguments

Use command arguments to set options for any CLI commands.

-   **--help**

    Provides help information for the specified command, which includes the description, supported arguments, and examples. For more information, see [Get help with ServiceNow CLI](../task/get-help.md).

    ```
    $ snc --help
    ```

-   **--debug**

    provides debug logging output when executing a command. For more information, see [Get help with ServiceNow CLI](../task/get-help.md).

    ```
    $ snc record delete --table incident --sysid 552c48888c033300964f4932b03eb092 --debug
    ```

-   **--profile**

    Specifies the named profile to use for a command. For more information, see [Configuring and managing your ServiceNow CLI connection profiles](../task/configure-profile.md).

    ```
    $ snc configure profile set --profile <profilename>
    ```

-   **--output**

    Specifies the output format to use for a command. The ServiceNow CLI supports the following output formats.

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
    ```
    $ snc record query --table incident --query ‘active=true’ --output json
    ```

-   **--no-interactive**

    Prevents the CLI from prompting the user for argument values. If the user does not pass a value for a required argument, the system uses the default value. If no default value is defined, the system throws an error.

-   **--no-verbose**

    The command executes silently without messages.​ Use this argument in automated testing scenarios.


## Configure profile

Create a connection profile to connect with your instance, view connection profiles, refresh your connection and available commands, or delete profiles you no longer need. For more information about configuring your profile, see [Configuring and managing your ServiceNow CLI connection profiles](../task/configure-profile.md).

-   **Set up a default profile**

    Create a connection profile that the ServiceNow CLI uses by default. You must create a default profile to set up the CLI's initial connection with an instance.

    ```
    $ snc configure profile set
    ```

    The system prompts you for the following information:

    |Requested information|Description|
    |---------------------|-----------|
    |Host|The host name of the instance to connect to. Supports both the full URL \(https://my-instance.service-now.com\) or just the host name \(my-instance\).|
    |Login method|The login method to use to connect to the instance. Supports `Basic`, `OAuth`, and `OAuth + MFA`.|
    |Username|The user name to use to connect to the instance.|
    |Password|The password to use to connect to the instance.|
    |Client id|The client ID to use to connect to the instance when the login method is OAuth or OAuth + MFA.|
    |Client secret|The client secret to use to connect to the instance when the login method is OAuth or OAuth + MFA.|
    |Authentication code|The authentication code to use to connect to the instance when the login method is OAuth + MFA.|
    |Default output format|Specifies how to format the command results. Options are `json`, `yaml`, `text`, and `table`.|

-   **Set up a named profile**

    Create a named connection profile to use with specific commands. This allows you to specify a different instance or connection protocol for a specific command.

    ```
    $ snc configure profile set [--profile profile-name]
    ```

    The system prompts you for the following information:

    |Requested information|Description|
    |---------------------|-----------|
    |Host|The host name of the instance to connect to. Supports both the full URL \(https://my-instance.service-now.com\) or just the host name \(my-instance\).|
    |Login method|The login method to use to connect to the instance. Supports `Basic`, `OAuth`, and `OAuth + MFA`.|
    |Username|The user name to use to connect to the instance.|
    |Password|The password to use to connect to the instance.|
    |Client id|The client ID to use to connect to the instance when the login method is OAuth or OAuth + MFA.|
    |Client secret|The client secret to use to connect to the instance when the login method is OAuth or OAuth + MFA.|
    |Authentication code|The authentication code to use to connect to the instance when the login method is OAuth + MFA.|
    |Default output format|Specifies how to format the command results. Options are `json`, `yaml`, `text`, and `table`.|

-   **View profiles**

    View all connection profiles set in the configuration file, or view information about a specific profile.

    ```
    $ snc configure profile list [--profile profile-name]
    ```

-   **Remove a profile**

    Remove a named connection profile that you no longer need from the configuration file.

    ```
    $ snc configure profile remove [--profile profile-name]
    ```

-   **Refresh a profile**

    Update the available commands from the instance for the given profile. Refresh your connection after modifying any of the commands on the corresponding instance in order to keep the CLI up-to-date.

    ```
    $ snc configure profile refresh [--profile profile-name]
    ```


## Perform record operations

Create, read, update, delete, and query records in your instance using the ServiceNow CLI command-line tool. For more information about performing record operations, see [Perform record operations using ServiceNow CLI](../task/manage-records.md).

-   **Create a record**

    Inserts a single record in a specified table.

    ```
    $ snc record create [--table table --data data]
    ```

    Pass in values for these arguments.

    |Parameter|Description|
    |---------|-----------|
    |table|Required. Name of the table in which to save the record.|
    |data|Required. Field name and the associated value for each field to define in the specified record in JSON string format.|

-   **Delete a record**

    Deletes the specified record from the specified table.

    ```
    $ snc record delete [--table table --sysid sys_id]
    ```

    Pass in values for these arguments.

    |Parameter|Description|
    |---------|-----------|
    |table|Required. Name of the table in which to delete the record.|
    |sysid|Required. Sys\_id of the record to delete.|

-   **Get a record**

    Retrieves a single record based on the specified sys\_id from the specified table.

    ```
    $ snc record get [--table table --sysid sys_id]
    ```

    Pass in values for these arguments.

    |Parameter|Description|
    |---------|-----------|
    |table|Required. Name of the table from which to retrieve the record.|
    |sysid|Required. Sys\_id of the record to retrieve.|

-   **Query records**

    Retrieves multiple records from a specified table.

    ```
    $ snc record query [--displayvalue displayValue --fields fields --limit limit --offset offset --query query --table table]
    ```

    Pass in values for these arguments.

    |Parameter|Description|
    |---------|-----------|
    |displayValue|Include `--displayvalue` to retrieve the display value from the database for reference and choice fields. Do not include this parameter to retrieve the actual values.|
    |fields|Comma-separated list of field names to return from the database.|
    |limit|Maximum number of records to return.|
    |offset|Starting record index for which to begin retrieving records. Use this value to paginate record retrieval.|
    |query|Required. Encoded query used to filter the result set in the following format: `--query '<column_name><operator><value>'`.|
    |table|Required. Name of the table in which to query the records.|

-   **Update a record**

    Updates the specified record with the given data attributes.

    ```
    $ snc record update [--sysid sys_id --table table --data data]
    ```

    Pass in values for these arguments.

    |Parameter|Description|
    |---------|-----------|
    |table|Required. Name of the table in which to save the record.|
    |sysid|Required. Sys\_id of the record to update.|
    |data|Required. Field name and the associated value for each field to define in the specified record in JSON string format.|


## Work with extensions

Add extensions to the ServiceNow CLI to load additional functionality and commands, update existing extensions, or remove extensions you no longer need. For more information, see [Manage ServiceNow CLI extensions](../task/find-extensions.md).

-   **Find available extensions**

    ```
    $ snc extension list-available -o table
    ```

-   **Install an extension**

    ```
    $ snc extension add --name <extension-name>
    ```

-   **Update an extension**

    ```
    $ snc extension update --name <extension-name>
    ```

-   **Remove an extension**

    ```
    $ snc extension remove --name <extension-name>
    ```


## Use the ui-component extension

-   **Add the ui-component extension**

    Add the ui-component extension to the ServiceNow CLI.

    ```
    $ snc extension add --name ui-component
    ```

-   **Set up your project**

    Create the component project and the set of files required to develop a component. You can connect to your instance and create an application scope for your component, or you can reserve a scope to verify later.

    ```
    $ snc ui-component project [--name name --description description --scope scope --offline]
    ```

    Pass in values for these arguments.

<table id="table_gsw_mbg_m4b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

Required. The project name. Must be a valid and unique npm package name.

</td></tr><tr><td>

description

</td><td>

The project description to be available in the npm registry and the plugins list in your instance.

</td></tr><tr><td>

scope

</td><td>

Suggested application scope to assign to this project and its components. If provided, the instance validates the name. Use the namespace identifier guidelines for application development on the instance. For more information, see [Application scope](../../applications/concept/c_ApplicationScope.md). Maximum: 18 characters.

 Case: snake case.

 Default: `x_customerprefix_componentname`, where:

-   `customerprefix` is the value in the **glide.appcreator.company.code** system property on your instance.
-   `componentname` is the value provided in the component's `name` parameter when you created the project.
 Alternatively, you can add a value to the `scopeName` parameter in the `now-ui.json` file. For more information, see [Change a component's application scope](../../components/task/change-scope.md).

</td></tr><tr><td>

offline

</td><td>

When true, creates and scaffolds a component while disconnected from your instance. Skips validation of the given scope name. Default: `false`.

</td></tr></tbody>
</table>-   **Run the development server**

    Add your component code and test it using a local development server.

    ```
    $ snc ui-component develop [--entry entry --open --port port --host host]
    ```

    Pass in values for these arguments.

<table id="table_lnx_bzt_vkb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

entry

</td><td>

Path to the test module in your component project. Default: `example/index.js`.

</td></tr><tr><td>

open

</td><td>

Opens the default browser and navigates to the test page. Default: false.

</td></tr><tr><td>

port

</td><td>

Port where the development server runs. Default: 8081.

</td></tr><tr><td>

host

</td><td>

Host address to use if you want your local development server to be accessible externally by others. Typically set to `0.0.0.0`

</td></tr></tbody>
</table>-   **Deploy a component to an instance**

    Deploy your component to display in your instance as an application plugin.

    ```
    $ snc ui-component deploy [--open --force]
    ```

    Pass in values for these arguments.

<table id="table_ck1_qzt_vkb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

open

</td><td>

When true, opens the default browser and navigates to UI Builder in your instance. Default: false

</td></tr><tr><td>

force

</td><td>

Deploys component changes and overwrites any existing component records. Default: false.

</td></tr></tbody>
</table>
**Parent Topic:**[ServiceNow CLI](../concept/servicenow-cli.md)

