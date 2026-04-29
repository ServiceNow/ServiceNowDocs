---
title: Create a parsing rule
description: Populate output variables defined in a custom activity with payload data returned from an inputs test on an external host or endpoint.This table lists the parsing sources available with each execution template.In this example, the parsing rule is configured to populate the activityOutput.ipv4 variable with the value for the IP address from a domain server, using PowerShell.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create custom activities using custom activity designer templates, Orchestration activity designer, Classic Orchestration, Workflow Data Fabric]
---

# Create a parsing rule

Populate output variables defined in a custom activity with payload data returned from an inputs test on an external host or endpoint.

## Before you begin

Roles required: activity\_admin, activity\_creator

## About this task

## Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor**.

2.  From the **Custom** tab in the palette, open a custom activity.

3.  In the Activity Designer form, advance to the **Output** stage.

4.  Drag an output variable from the data structure builder into the **Variable name** field in the **Parsing rules** builder.

    ![Mapping variables to parsing rules](../image/OutputsMappingVariable.png "Mapping variables to parsing rules")

    The parsing rules form appears for the selected variable. By default, the parsing type is set to **Direct**, which populates the variable with all the data from the selected payload, without parsing the contents. Each template has a specific default [parsing source](t_CreateAParsingRule.md#).

5.  Complete the form using the fields in the table.

    In this example, the parsing type selected is **XML**, which allows you to select specific parameters from the payload to parse.

    ![Parsing rules form](../image/ActivityParsingRule.png)

<table id="table_yry_ptm_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Parsing source

</td><td>

Source of the data returned from the target host or endpoint. Each template opens to a specific, default payload. Available choices depend on the execution template selected for the activity. You can also use local variables as a parsing source if a parsing rule has previously been defined for them. For a list of the available payloads for each template, see [Activity designer parsing sources](t_CreateAParsingRule.md#).

</td></tr><tr><td>

Expression

</td><td>

Expression used to extract specific data from the selected parsing source. This expression is created from clickable data in the sample payload and appears in the format selected in the **Parsing type** field. When testing, the expression can return multiple results. Discern which choice gives reliable or predictable results before choosing your expression.**Note:** The system cannot generate clickable **RegEx** expressions from sample data. You must write all regular expressions manually.

</td></tr><tr><td>

Variable name

</td><td>

Revised variable name as it is used in the final output expression. The system adds the **activityOutput** or **activityLocal** prefix to the variable you specify.

</td></tr><tr><td>

Parsing type

</td><td>

The language to use for querying the target host's payload. The selections are:-   **Direct**: Maps to the entire content of the payload selected in the **Parsing source** field, without any parsing. This is the default parsing type.
-   **XML**: XPath query used for selecting nodes from an XML payload.
-   **JSON**: JSONPath query for selecting parts of a JSON payload.
-   **RegEx**: Parsing method that uses a regular expression to extract data from a payload. The RegEx parsing type does not support multi-line parsing and is not case sensitive.


</td></tr><tr><td>

Short description

</td><td>

Brief description of this parsing rule.

</td></tr><tr><td>

Sample payload data

</td><td>

Sample data from the source containing the data requested. This field is not available for **Direct** parsing types. After you click **Parse sample data**, the data in this field cannot be edited, but becomes clickable for the purpose of creating expressions. Click **Edit sample data** to make the field editable again.

</td></tr><tr><td>

Parsing results

</td><td>

Displays the data returned from the source by the selected expression. This field is not available for **Direct** parsing types.

</td></tr></tbody>
</table>6.  To retest the inputs, click **Get sample payload from test**.

    This action reopens the test form, allowing you to substitute different test values and create a different payload.

7.  Click **Save** to have the parsing rules overwrite the previous payload with the one you just created.

8.  To create an expression for the parsing rule, click the specific parameter you want to see in the sample payload.

    The value for that parameter appears in the **Parsing result** field, and the system creates the appropriate expression in the **Expression** field.

9.  Click **Submit** to save the parsing rule for that variable.


**Parent Topic:**[Create custom activities using custom activity designer templates](create-custom-activities.md)

## Activity designer parsing sources

This table lists the parsing sources available with each execution template.

<table id="table_wjw_bvm_cr"><thead><tr><th>

Template

</th><th>

Source

</th></tr></thead><tbody><tr><td>

SOAP Web Service

</td><td>

-   executionResult.body \(Default\)
-   executionResult.status\_code
-   executionResult.header
-   executionResult.error

</td></tr><tr><td>

JDBC

</td><td>

-   executionResult.output \(Default\)
-   executionResult.errorMessages
-   executionResult.probeCompletedEccId
-   executionResult.totalRows

</td></tr><tr><td>

JavaScript Probe

</td><td>

-   executionResult.payload \(Default\)
-   executionResult.output
-   executionResult.eccSysId
-   executionResult.errorMessages

</td></tr><tr><td>

Powershell

</td><td>

-   executionResult.output \(Default\)
-   executionResult.tags
-   executionResult.hresult
-   executionResult.eccSysId
-   executionResult.errorMessages

</td></tr><tr><td>

REST Web Service

</td><td>

-   executionResult.body \(Default\)
-   executionResult.status\_code
-   executionResult.header
-   executionResult.error

</td></tr><tr><td>

SFTP

</td><td>

-   executionResult.output \(Default\)
-   executionResult.eccSysId
-   executionResult.errorMessages
-   executionResult.tags

</td></tr><tr><td>

Probe

</td><td>

-   executionResult.output \(Default\)
-   executionResult.payload
-   executionResult.eccSysId

</td></tr><tr><td>

SSH

</td><td>

-   executionResult.output \(Default\)
-   executionResult.eccSysId
-   executionResult.errorMessages
-   executionResult.tags

</td></tr><tr><td>

JMS

</td><td>

-   executionResult.status
-   executionResult.standardHeaders
-   executionResult.customHeaders
-   executionResult.messagePayload
-   executionResult.eccSysId
-   executionResult.errorMessages

</td></tr></tbody>
</table>## Activity designer parsing rule example

In this example, the parsing rule is configured to populate the activityOutput.ipv4 variable with the value for the IP address from a domain server, using PowerShell.

### Before you begin

Role required: activity\_creator, activity\_admin

### About this task

To generate the sample data, the administrator must actually run the command on the host and then paste the data returned into the **Sample payload data** field when creating the parsing rule. The administrator can then create an expression that returns IP addresses from that sample in two formats: `ipv4` and `ipv6`. In this example, the system produces two expressions to use for the parsing rule.

### Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Workflow Editor** and open the activity that runs on the host.

2.  Click the **Inputs** tab, and note the **Command**.

    ![Parsing rule PowerShell inputs command](../image/ParsingRulesPowershellCommand.png "Parsing rule PowerShell inputs command")

3.  In a PowerShell console, run the **Command** on the host to extract the XML sample that contains the values you need.

4.  Copy the data that is returned to the clipboard.

5.  In the activity designer, click the **Outputs** tab and paste the returned data into the **Sample payload data** field.

    In this example, the data includes IP addresses in two different formats and the domain name.

6.  Select the parsing type for the source.

    In the following example, you would select **XML**.

    ![Parsing rule raw payload data](../image/ParsingRulesSampleDataRaw.png)

7.  Click **Parse sample data**.

    The system displays the XML in the proper format, and it becomes clickable. In this view, the system can translate clicked data from the sample into an expression.

    ![Parsing rule parsed payload data](../image/ParsingRulesSampleData.png)

8.  To create the expression, click the elements in the data sample you want to map to the variable.

    Based on the sample data you clicked, the system creates two expressions.

    ![Creating parsing rule expressions](../image/ParsingRulesCreateExpression.png)

9.  Select an expression from the list.

    The desired result is the IP address that has a **type** attribute of **ipv4**. The system populates the **Expression** field with this choice.

    ![Selecting a parsing rule expression](../image/ParsingRulesSelectExpression.png)

10. Click **Test expression**.

    The system parses the payload using the selected expression and returns the requested data in the **Parsing result** field.

    ![Testing a parsing rule expression](../image/ParsingRulesTestExpression.png)

11. Click **Submit**.

    The view returns to the **Outputs** tab of the activity designer. The new parsing rule is listed, and a blank row is available for another rule.

    ![List of completed parsing rules](../image/ParsingRulesList.png)


