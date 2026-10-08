---
title: Create check parameters for a check
description: Create a check parameter to add a configurable input that customizes how a check runs, without changing the underlying script or command.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/create-check-parameters-for-a-check.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Collect data from your system devices, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Create check parameters for a check

Create a check parameter to add a configurable input that customizes how a check runs, without changing the underlying script or command.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

A check parameter contains:

-   Check Parameter Definition: defines each check type. It declares the parameter's name, meaning, default value, and the command-line flag it maps to.
-   Check Parameter Value: specify the value of the defined parameter which is specific to a check instance.

**Note:** The meaning and valid values of any parameter depend on the related check definition.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Check Definitions**.

2.  Select a check definition from the displayed list.

    The **Check Definition** page for the selected check appears.

3.  Scroll to the bottom of the page and select the **Check Parameter Definitions** tab.

4.  Select **New**.

    The **Check Parameter Definition New Record** page appears.

    \[Omitted image "ACC-Check-Parameter.png"\] Alt text: Check Parameter Definition New Record page

5.  Configure the fields on the page.

    |Field|Description|
    |-----|-----------|
    |**Name**|Name of the parameter, formatted as a reference prefix.|
    |**Active**|Activates the check parameter on selection.|
    |**Default Value**|Indicates that the parameter must contain a default value.|
    |**Flag**|A prefix that must be added before the parameter value in the command. For example `-p`.|
    |**Check Definition**|The name of the check definition connected to the parameter.|
    |**Mandatory**|Indicates that the parameter is mandatory.|
    |**Value required**|Indicates that a value must be provided for the parameter.|

    **Note:** The **Active**, **Flag**, and **Value required** options are displayed only when the **Command Auto Generation** option is selected.

6.  Select **Submit**.

    The configured parameter appears in the table on the **Check Parameter Definitions** tab.

    Repeat this procedure to enter multiple check parameters.

7.  Enter the check parameters in the **Command** field of the check definition.

    Each check definition has a **Command** field containing a template. Parameter values are substituted into this template at execution time:

    ```
    check-kernel-parameter.rb {{if .labels.params_parameter_value}} -v {{.labels.params_parameter_value}} {{end}} {{if .labels.params_parameter_name}} -p {{.labels.params_parameter_name}} {{end}}
    ```

    -   `.labels.params_<parameter_name>` refers to the value configured for that parameter.
    -   `{{if ...}} ... {{end}}` adds the flag and value only when the parameter has a value. If the parameter is empty, its flag is omitted.
    -   The flag prefix such as `-v`, `-p`, and so on is picked from the **Flag** field on the check parameter definition.
    This command is assembled automatically from the configured parameter values.

    Example:

    The `os.linux.check-kernel-parameter` check defines two parameters:

    |Parameter name|Flag|Purpose|
    |--------------|----|-------|
    |`parameter_name`|-p|The Linux kernel parameter to check. For example, `kernel.shmmni`|
    |`parameter_value`|-v|The expected value for that kernel parameter.|

    When you configure `parameter_name` with the following settings:

    ```
    
    Name:           parameter_name
    Active:         true
    Mandatory:      true
    Flag:           -p
    Value required: true
    Value:          kernel.shmmni
    
    ```

    You also specify the `parameter_value` as 4096. The check runs as follows:

    ```
    check-kernel-parameter.rb -v 4096 -p kernel.shmmni
    ```


**Related topics**  


[Create a check definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/acc-api-check-def.md)

[Agent Client Collector check definition page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/check-definition-form.md)

