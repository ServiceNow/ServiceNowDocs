---
title: Create a custom command in ServiceNow CLI
description: Manage your custom application from the command line by creating custom commands in the ServiceNow CLI.
locale: en-US
release: zurich
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Create a custom command in ServiceNow CLI

Manage your custom application from the command line by creating custom commands in the ServiceNow CLI.

## Before you begin

Role required: admin

## About this task

A ServiceNow CLI command maps to a scripted REST endpoint in the End Point \[sn\_cli\_metadata\_end\_point\] table. You can define a scripted REST endpoint to perform a function in your custom application, or use any existing REST endpoint. Then map a CLI command to execute the REST call.

## Procedure

1.  Make a REST endpoint available to a ServiceNow CLI command.

    1.  Navigate to **Command Line Interface \(CLI\)** &gt; **End Points**.

    2.  Select **New** and complete the form.

        |Field|Description|
        |-----|-----------|
        |Resource Path|Required. Path to the endpoint on the instance to map a command to. Can be the path to an inbound REST API, or a scripted REST API. For example, `api/now/table/{table}/{sysid}`. For more information, see [Available REST APIs](https://www.servicenow.com/docs/access?context=api-rest&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) and [Scripted REST APIs](https://www.servicenow.com/docs/access?context=c_CustomWebServices&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).|
        |HTTP Method|Required. HTTP method to use when the user runs the associated command.|
        |Application|Read-only application scope for the endpoint.|

2.  Create a command group.

    Alternatively, you can add your new command to an existing command group.

    1.  Navigate to **Command Line Interface \(CLI\)** &gt; **Command Groups**.

    2.  Select **New** and complete the form.

        |Field|Description|
        |-----|-----------|
        |Name|Required. Name of the command group.|
        |Parent Group|Parent command group.|
        |Reference Group|Command group to reference. For example, you can create a new command group as an alias for an existing command group. When the user calls a referenced command using the new command group, the original command executes. This enables you to create a command group specific to your custom application that includes both new and existing commands.|
        |Short Description|Required. Short description for the command group.|
        |Description|Description of the command group used as help text when the user runs the `--help` command on the command group.|
        |Application|Read-only application scope for the command group.|
        |Active|When selected, the command group is active.|

3.  Create a command.

    1.  Navigate to **Command Line Interface \(CLI\)** &gt; **Commands**.

    2.  Select **New** and complete the form.

<table id="table_o3q_qyg_m4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Required. Name of the command.

</td></tr><tr><td>

Command Group

</td><td>

Required. Command group that the command is a part of.

</td></tr><tr><td>

Reference Command

</td><td>

Command to reference. For example, you can create a new command as an alias for an existing command. When the user calls the new command, the original command executes. This enables you to create a command specific to your custom application that executes existing functionality.**Note:** A command cannot reference a command that references another command, or reference a descendant command, an ancestor command, or a callback command.

</td></tr><tr><td>

API Endpoint

</td><td>

Required. API call to execute when the user runs the command.

</td></tr><tr><td>

Short Description

</td><td>

Required. Short description of the command.

</td></tr><tr><td>

Application

</td><td>

Read-only application scope for the command.

</td></tr><tr><td>

Active

</td><td>

When selected, the command is active.

</td></tr><tr><td>

Is Callback Command

</td><td>

When true, designates the command as a callback command. Select this option to hide the command from the CLI client and prevent users from calling it from the command line. Use this field with the **Callback** section of a primary command. The callback command executes when the primary command is complete.

</td></tr><tr><td colspan="2">

**Help Text**

</td></tr><tr><td>

Description

</td><td>

Description of the command used as help text when the user runs the `--help` command.

</td></tr><tr><td>

Examples

</td><td>

Examples of the command used as help text when the user runs the `--help` command.

</td></tr><tr><td colspan="2">

**Expressions**

</td></tr><tr><td>

Success Expression

</td><td>

Expression used to evaluate the response from the server and determine if the command succeeded. For example, `result.code = 1`.

</td></tr><tr><td>

Failure Expression

</td><td>

Expression used to evaluate the response from the server and determine if the command failed.

</td></tr><tr><td colspan="2">

**Messages**

</td></tr><tr><td>

Success Message

</td><td>

Message displayed on the CLI client when the command is successful.

</td></tr><tr><td>

Progress Message

</td><td>

Message displayed on the CLI client when the command is in progress.

</td></tr><tr><td>

Failure Message

</td><td>

Message displayed on the CLI client when the command fails.

</td></tr><tr><td colspan="2">

**Callback**

</td></tr><tr><td>

Callback Expression

</td><td>

Expression used to determine whether to execute the callback command. For example, you can write an expression that checks on a long-running process. If the expression produces a certain result, the callback executes.

</td></tr><tr><td>

Callback Command

</td><td>

Command to execute when the **Callback Expression** is satisfied. Must be a command with the **Is Callback Command** field selected.

</td></tr><tr><td>

Callback Interval

</td><td>

The interval between callback command executions. Unit: Milliseconds

 Default: 1,000

</td></tr><tr><td>

Max Retries

</td><td>

Maximum number of times the callback command executes. Default: 10

</td></tr></tbody>
</table>    3.  In the Command Arguments related lists, create any command arguments needed for the command.

        Create a command argument to allow users to set options when running a command.

<table id="table_hg5_nnh_m4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Required. Name of the command argument, for example `data`.

</td></tr><tr><td>

Short Name

</td><td>

Short dame of the command argument, for example `d`.

</td></tr><tr><td>

Data Type

</td><td>

Required. Type of data expected for the command argument. Options include:-   String: Allows users to enter a string as input.
-   Integer: Allows users to enter a number as input.
-   Boolean: Allows users to enter `true` or `false` as input.
-   File Input: Allows users to upload a file as input. Map this argument to a Body **Parameter Type** in the API Endpoint Arguments related list in the next step. Users can pass plain text, YAML, JSON, or another file type accepted by the REST API. When the user submits a YAML file, the CLI client converts to file to JSON format by default. Use the **Skip Pre-processing** field to disable this behavior.
-   Password: Allows users to securely enter a password as input.
 **Note:** For File Input data types, the file size limit is 10 MB by default. However, you change this limit using the **glide.rest.scripted.max\_inbound\_content\_length\_mb** system property.

</td></tr><tr><td>

Skip Pre-processing

</td><td>

Set this flag to prevent the CLI client from converting YAML files into JSON format before sending them in the request. When **Data Type** is set to **File Input** and the user submits a YAML file, the CLI client converts the file to JSON before executing the command by default.**Note:** Only applies when **Data Type** is set to **File Input**.

</td></tr><tr><td>

Default Value

</td><td>

Default value to use when the user does not pass a value.

</td></tr><tr><td>

Short Description

</td><td>

Required. Short description of the command argument. Used as help text when the user runs the `--help` command.

</td></tr><tr><td>

Application

</td><td>

Read-only application scope for the argument.

</td></tr><tr><td>

Command

</td><td>

Required. Command that the argument applies to.

</td></tr><tr><td>

Mandatory

</td><td>

When selected, the user must provide a value for the argument when running the associated command.

</td></tr><tr><td>

Prompt

</td><td>

Prompt to request information from the user. The CLI prompts for information when the user does not include a required argument in a command.

</td></tr><tr><td>

Visibility Expression

</td><td>

Expression used to determine whether the CLI should prompt for the argument. Typically used to display an argument based on the value provided to a previous argument.

</td></tr><tr><td>

Order

</td><td>

Order in which to prompt for the argument.

</td></tr></tbody>
</table>    4.  In the API Endpoint Arguments related lists, create any API endpoint arguments needed for the command.

        Map command arguments from the Command Arguments related list to parameters in your REST endpoint.

<table id="table_jqf_qnh_m4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Required. Name of the argument.

</td></tr><tr><td>

Value

</td><td>

Required. The value from the command that you want to pass to the REST endpoint. You can pass a static value, or an expression such as `{flags.table}`. Use the `flags` global variable to access the command arguments.

</td></tr><tr><td>

Parameter Type

</td><td>

Required. The type of parameter in the REST endpoint that you want to pass the **Value** to. For example, if you select **Body**, the CLI passes the value of the **Value** field to the REST endpoint body. Options include:-   Body
-   Header
-   Path
-   Query


</td></tr><tr><td>

Application

</td><td>

Read-only application scope for the argument.

</td></tr><tr><td>

Command

</td><td>

Required. Command that the argument applies to.

</td></tr></tbody>
</table>    5.  In the Return Values related lists, create any return values needed for the command.

        Create return values to only return certain keys from the response.

        |Field|Description|
        |-----|-----------|
        |Path Expression|Required. Expression representing the path to the key that you want to return.|
        |Alias|Variable name to assign the return value to.|
        |Application|Read-only application scope for the command.|
        |Command|Required. Command that the return value applies to.|


## Result

When the user runs the ServiceNow CLI command, the system executes the associated REST API call and returns the result to the ServiceNow CLI.

**Parent Topic:**[ServiceNow CLI](../concept/servicenow-cli.md)

