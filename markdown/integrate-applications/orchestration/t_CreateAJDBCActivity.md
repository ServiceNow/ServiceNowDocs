---
title: Create a JDBC activity
description: Create a custom JDBC activity to automate SQL commands and stored procedure calls to relational databases from workflow.The JDBC Connection \[jdbc\_connection\] table provides the information custom JDBC Orchestration activities use to connect to various target databases.The ServiceNow activity designer allows you to map parameter values in a JDBC test payload to variables in the Outputs tab automatically.You can use Orchestration to run a stored procedure on MySQL, Oracle DB, and MS-SQL databases.You can test the input parameters of a custom JDBC activity during its development without having to run the activity in a workflow context.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, Data and Automation]
---

# Create a JDBC activity

Create a custom JDBC activity to automate SQL commands and stored procedure calls to relational databases from workflow.

## Before you begin

Role required: activity\_admin, activity\_creator

## About this task

The JDBC activity template allows you to execute ANSI SQL statements or stored procedures on a target database. Support for stored procedures with IN, OUT, and INOUT parameters are available in Yokohama. To learn how to set up these parameters, see [JDBC stored procedure parameters](t_CreateAJDBCActivity.md#).

**Note:** If you are transferring bulk data into a ServiceNow instance from an external data source, use [Import sets key concepts](../../import-sets/concept/c_ImportSetsKeyConcepts.md). The JDBC activities allow you to transfer data between external data sources and ServiceNow within a workflow. It is not intended to replace the bulk import features of data sources.

## Procedure

1.  Create or verify your [JDBC credential](https://www.servicenow.com/docs/access?context=r_JDBCCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

    Your JDBC credentials must have permission for the target database and proper configuration for the corresponding JDBC connection. Credentials must be set up before you can create a JDBC activity.

2.  Create or verify your [JDBC connection](t_CreateAJDBCActivity.md#).

    Your JDBC connection must be configured with valid JDBC credentials set up before you can create a JDBC activity.

3.  Create a [custom activity](create-custom-activities.md).

    This action creates a custom activity using a template.

4.  After setting up [general properties](../reference/General-Flds-Templates.md) and [creating input variables](CreateInputVariables.md#), configure the JDBC Execution Command.

<table id="choicetable_py3_zmj_4y"><tbody><tr><td id="d444479e163">

**[JDBC Connection](t_CreateAJDBCActivity.md#)**

</td><td>

Configure or reference the appropriate JDBC Connection for the database. The connection selected provides the activity with the following information: -   Target database information \(server and database names\)
-   Connection URL
-   Target database port \(if different from standard port number\)
-   Database instance name


</td></tr><tr><td id="d444479e194">

**Credential**

</td><td>

JDBC credential to use for your JDBC connection.

</td></tr><tr><td id="d444479e203">

**SQL statement**

</td><td>

Input the ANSI SQL to execute on the JDBC target database. **Note:** This field is hidden when the Stored Procedure check box is selected.

 You can [map the input variables](CreateInputVariables.md#) you created to configure the SQL statements. By default, you can run the following SQL statements. -   select
-   insert
-   update
-   delete
-   show
-   create
-   describe
For added security measure, a MID Server property controls the operations that this JDBCOrchestrationProbe executes, which restricts the SQL commands used. This property protects against potentially destructive commands, such as drop database. The mid.property.jdbc\_operations contains the MID Server property controls.**Note:** You cannot run multiple statements of different types. For example, you cannot run a select statement and an update statement together, but you can run two insert statements. However, you cannot run multiple select statements in this activity.

</td></tr><tr><td id="d444479e250">

**Maximum rows**

</td><td>

Maximum number of records to retrieve from database. The default is 1000.

</td></tr><tr><td id="d444479e259">

**Maximum payload size \(KB\)**

</td><td>

You can set a limit on the maximum payload size of data retrieved from the database. The default is 64 kilobytes.

</td></tr><tr><td id="d444479e269">

**Connection timeout**

</td><td>

How long the activity waits to make the connection. This field is populated automatically from the data source, but can be changed for this activity.

</td></tr><tr><td id="d444479e278">

**Query timeout**

</td><td>

Elapsed time to wait after running the query until the data is returned. This field is populated automatically from the data source, but can be changed for this activity.

</td></tr><tr><td id="d444479e287">

**Required MID Server capabilities**

</td><td>

MID Server to use for querying JDBC, by capabilities. By default, the system selects a MID Server that has JDBC capability.

</td></tr><tr><td id="d444479e296">

**Use stored procedure**

</td><td>

If checked, you can run a stored procedure on MySQL, Oracle, or SQL Server databases by entering the procedure name and parameters. See [JDBC stored procedure parameters](t_CreateAJDBCActivity.md#).

</td></tr></tbody>
</table>    **Note:** You can map parameter values in a test payload to variables in the **Outputs** tab automatically. See [automap output variables](automap-output-variable-inputs.md).


## What to do next

-   [Test JDBC activity inputs](t_CreateAJDBCActivity.md#)
-   Use [auto-mapping](automap-output-variable-inputs.md) to generate outputs and parsing rules \(recommended for JDBC\)
-   If you do not use auto-mapping, you can manually [create output variables](t_CreateAnOutputVariable.md#) and [create parsing rules](t_CreateAParsingRule.md#)

**Parent Topic:**[Orchestration custom activity templates](../concept/c_ActivityDesignerComponents.md)

**Related topics**  


[Create custom activities using custom activity designer templates](create-custom-activities.md)

## Create a JDBC connection for an Orchestration activity

The JDBC Connection \[jdbc\_connection\] table provides the information custom JDBC Orchestration activities use to connect to various target databases.

### Before you begin

You must have an appropriate JAR file, whether it is supplied with the instance or a custom JAR file.

**Note:** The ServiceNow instance supplies `mysql-connector-java-5.1.21.jar`, `sql-server-jdbc-4.0.jar`, and `ojdbc6.jar` files as part of the current release, which supports MySQL, SQLServer, and Oracle databases. Other databases, such as Sybase or DB2 Universal, must use a custom JAR file that must be uploaded to the instance before setting the JDBC connection.

Role required: activity\_admin, activity\_creator

### About this task

[JDBC credentials](https://www.servicenow.com/docs/access?context=r_JDBCCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) [JDBC credentials](https://www.servicenow.com/docs/access?context=r_JDBCCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) are retrieved separately by the activity designer template and support external credential storage, such as [CyberArk](https://www.servicenow.com/docs/access?context=c_CyberArkCredStorageIntegrate&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

### Procedure

1.  Navigate to **All** &gt; **Orchestration** &gt; **Credentials &amp; Connections** &gt; **JDBC Connections** and click **New**.

2.  Complete the form using the fields in the table.

    The database selection in the **Format** field determines which fields are available.

<table id="table_dls_tpv_sx"><thead><tr><th>

Field

</th><th>

Database Format

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

All

</td><td>

Unique name of this JDBC connection. For example, you might enter **JDBC MySQLProd**.

</td></tr><tr><td>

Query timeout

</td><td>

All

</td><td>

Maximum elapsed time the JDBC query is allowed to run without a response.

</td></tr><tr><td>

Connection timeout

</td><td>

All

</td><td>

Maximum elapsed time for the JDBC activity to wait while attempting to connect to the target database.

</td></tr><tr><td>

Application

</td><td>

All

</td><td>

Scope for this table. By default, the JDBC Connection \[jdbc\_connection\] table runs in the **Global** scope.

</td></tr><tr><td>

Domain

</td><td>

All

</td><td>

Domain for this table. By default, the JDBC Connection \[jdbc\_connection\] table runs in the **global** domain.

</td></tr><tr><td>

Format

</td><td>

All

</td><td>

Database type for this connection. The default choices are: -   **MySQL**
-   **Oracle**
-   **SQLServer**
-   **None**
You can add **Sybase** or **DB2 Universal** to the choice list by uploading the appropriate JDBC driver JAR file to the instance. Orchestration automatically recognizes these drivers when they are loaded into the system and adds them to this list.

</td></tr><tr><td>

Server

</td><td>

Oracle, MySQL, SQLServer

</td><td>

Host name or IP address of the database server.

</td></tr><tr><td>

Oracle sid

</td><td>

Oracle

</td><td>

The Oracle database site identifier. The default value is **orcl**.

</td></tr><tr><td>

Oracle port

</td><td>

Oracle

</td><td>

Port that the Oracle database is using. The default value is **1521**.

</td></tr><tr><td>

Database name

</td><td>

MySQL, SQLServer

</td><td>

Name of the database.

</td></tr><tr><td>

Database port

</td><td>

My SQL, SQLServer

</td><td>

Port that the selected database is using.

</td></tr><tr><td>

Instance name

</td><td>

SQLServer

</td><td>

Instance name for the selected SQLServer

</td></tr><tr><td>

Connection URL

</td><td>

All

</td><td>

URL that the MID Server uses to connect to the specified database. The URL is created automatically when you save the form, and is read-only for the default databases. **Note:** If the format selected is not one of the default databases, you must create the connection URL manually so that the MID Server knows how to create the connection.

</td></tr><tr><td>

JDBC driver

</td><td>

None, DB2 Universal, Sybase

</td><td>

The JDBC driver to use for this connection when it is not a default database. **Note:** If you add a Sybase or DB2 Universal database, you must enter the driver name in this field and upload the driver JAR file to the instance.

</td></tr></tbody>
</table>    ![JDBC connection example](../image/JDBCConnection.png "JDBC connection to Oracle example")

3.  Click **Submit**.


**Related topics**  


[JDBC credentials](https://www.servicenow.com/docs/access?context=r_JDBCCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

## Auto-map JDBC activity output variables

The ServiceNow activity designer allows you to map parameter values in a JDBC test payload to variables in the **Outputs** tab automatically.

### Before you begin

Role required: admin

### Procedure

1.  In the JDBC provider template form, select the **Inputs** tab.

2.  Click **Test Activity** to test the input parameters.

    If you added actual values for the parameters and fields, the system runs those values against the specified target and returns the resulting payload. If you mapped input variables to fields and parameters, the system displays a dialog box for assigning test values to those variables.

3.  Provide test values, if requested, and click **OK** to display the payload.

    The entire payload appears in the **Raw Output** tab of the Response form.

    ![Auto-mapping controls](../image/AutoMappingButtons.png)

4.  Select one of these auto-mapping options.

    -   **Auto-Map to Local**: Directly maps values to a local variable for use within the activity.
    -   **Auto-Map to Output**: Directly maps values to the output variable to pass to other activities in the workflow. Auto-mapping to an output variable creates an array of objects, each of which contains the column names from the query result.

## JDBC stored procedure parameters

You can use Orchestration to run a stored procedure on MySQL, Oracle DB, and MS-SQL databases.

There is support of multiple data types, with the following limitations:

-   Only one result-set is returned.
-   The order of input and output data types in the stored procedure parameters must match the activity definition.
-   Binary, Blob, Varbinary, and LongBinary should be base64 encoded.
-   Date, Time, and Timestamp have a specific format:
    -   **Date format: yyyy-mm-dd**

        yyyy-mm-dd is the supported format.

    -   **Time format: hh:mm:ss\[.sss\]**

        hh:mm:ss\[.sss\] is the supported format. Precision is in milliseconds only, microseconds or nanoseconds cannot be handled.

        **Note:** `10:30:59` and `10:30:59.999000` are correct, but `10:30:59.` is incorrect.

    -   **Timestamp format: yyyy-mm-dd hh:mm:ss\[.ffffff\]**

        yyyy-mm-dd hh:mm:ss\[.ffffff\] is the supported format. Precision is to microseconds.

-   ResultSet is the first result set coming back from database server.
-   MS-SQL does not support INOUT parameters. If you use INOUT parameters, the Activity Template transparently maps them to OUT parameters.

**Note:** If you do not want to do a validation of data types in stored procedure parameters, like the legacy behavior, you set the glide.stored\_proc.data\_type.validation as false. See [MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

<table id="table_vry_jqc_cz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mode

</td><td>

Type of stored procedure parameter. Supported parameters:-   IN
-   OUT
-   INOUT

</td></tr><tr><td>

Sql Type

</td><td>

A SQL data type. Supported data types:-   ARRAY
-   BIGINT
-   BINARY
-   BIT
-   BLOB
-   CHAR
-   CLOB
-   DATE
-   DECIMAL
-   DISTINCT
-   DOUBLE
-   FLOAT
-   INT
-   INTEGER
-   JAVA\_OBJECT
-   LONGVARBINARY
-   LONGVARCHAR
-   NULL
-   NUMERIC
-   OTHER
-   REAL
-   REF
-   REF\_CURSOR
-   SMALLINT
-   STRUCT
-   TIME
-   TIMESTAMP
-   TINYINT
-   VARBINARY
-   VARCHAR

</td></tr><tr><td>

Name/Value

</td><td>

Name-value pairs to pass to the host. You can create these parameters manually, or drag and drop input variables into the parameter fields and assign a value.

</td></tr></tbody>
</table>**Note:** Not all database providers support the entire realm of JDBC data types. Reference your database reference manual to understand the supported datatypes for your installation.

## Test JDBC activity template inputs

You can test the input parameters of a custom JDBC activity during its development without having to run the activity in a workflow context.

### Before you begin

Create input variables and map them to fields in the Execution Command form or provide actual values for these fields. Role required: web\_service\_admin, activity\_admin, activity\_creator

### About this task

This test executes only the input parameters against an endpoint and not the pre-processing or post-processing scripts. It is not necessary to check out the activity to test it.

**Note:** If you provide enough information for Orchestration to contact the endpoint or host and return data, you can test the input variables. You can test from any stage in the activity designer. Typically, the Execution Command stage is the point at which your inputs are ready for testing.

### Procedure

1.  From the JDBC Execution Command, click **Test Inputs**.

    The list of input source variables appears. If you added default values for these variables, those values appear in the **Substitute Value** column. Mandatory variables are marked with a red star.

    **Note:** The test fails if the MID Server cannot be found or if it cannot connect to the target.

    ![JDBC input test values](../image/TestDesignerJDBCInputValues.png "JDBC input test values")

2.  Filter the variable list with these controls:

    -   **All Inputs**: Displays all input variables. This control is the default view.
    -   **Mandatory Inputs**: Displays only mandatory variables.
    -   **Inputs Without Defaults**: Shows input variables that do not have assigned default values.
3.  Reset values as needed.

    -   **Reset default values**: If values are present, this control replaces any test values set in this form with the default values.
    -   **Clear values**: Clears all values in the input variable list, even if default values exist.
4.  When your test values are configured correctly, click **OK**.

    The system runs the values for all the inputs configured against the specified target and returns the resulting payload. The buttons in the Response form display different views of the payload. The entire payload appears in the **Raw Output** window.

    ![Response payload from inputs test](../image/TestDesignerJDBCInputsResponse.png "Response payload from inputs test")

5.  To map appropriate parameter values in the payload to variables in the **Outputs** stage automatically, select an [auto-mapping option](t_CreateAJDBCActivity.md#).

6.  Click the **X** in the upper right corner of the window to close it.


