---
title: JDBC step
description: Create a reusable action to send SQL commands to a relational database.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Steps, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# JDBC step

Create a reusable action to send SQL commands to a relational database.

**Note:**

-   This step requires an Integration Hub subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf). After the required plugin is activated, the step is visible under Integrations.
-   The JDBC step runs only on a ServiceNow® MID Server with JDBC step capabilities. Activate the plugin, Integration Hub Standard Pack Installer \(com.glide.hub.integrations.standard\) or later to use the JDBC capability for the MID Server.

## Roles and availability

The JDBC step is available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Sanitizing inputs

Escape all user inputs to eliminate the possibility of a malicious user from executing malicious SQL statements that can result in SQL injection on your target database. When you use data pills in JDBC step SQL statements, sanitize them first using [Sanitize SQL transform functions](sanitize-sql-transform-functions.md). This transform function category automatically appears when a data pill is dropped into the SQL Statement input.

## SQL operations inclusion list

By default, you can run the following SQL operations.

-   SELECT
-   INSERT
-   UPDATE
-   DELETE
-   SHOW
-   DESCRIBE

To enable only some of these SQL operations that the JDBC step can perform, create a MID Server property, **mid.property.jdbc\_operations** and enter the SQL operations, separated by comma. To learn more about MID Server properties, see MID Server properties.

**Note:** Multiple SQL statements are not allowed. Stored procedures with output parameters are not supported.

## Fields

<table id="table_zms_zhj_2hb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connection Details

</td></tr><tr><td>

Connection

</td><td>

Type of connection to use.-   **Define Connection Inline**: Define connection information within the action step.
-   **Use Connection Alias**: Define connection information using the Connection Alias table. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action.

 To learn more about connections and credentials, see Introduction to credentials, connections, and aliases.

</td></tr><tr><td>

Connection Alias

</td><td>

Connection &amp; Credential alias record that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action. To learn more about connections and credentials, see credentials, connections, and aliases. The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. This field is available when **Use Connection Alias** is selected from the Connection list.

</td></tr><tr><td>

Credential Alias

</td><td>

Credential alias that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials when using an action in multiple environments. Likewise, if the credential information changes, you don't need to update your custom action. To learn more about connections and credentials, see credentials, connections, and aliases. The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see Configure a MID Server cluster.


 This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

MID Cluster

</td><td>

Data pill for the MID Cluster you want to use. This field is available when **Define Connection Inline** is selected from the Connection list, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr><tr><td>

Database Type

</td><td>

Database type for this connection. The choices are:-   **MySQL**
-   **Oracle**
-   **SQLServer**
-   **Custom**

The default choice is **Custom**. This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

JDBC Driver

</td><td>

Driver to use for this connection when it's not a default database type such as DB2 Universal and Sybase. The database Type is **Custom**. This field is available when **Define Connection Inline** is selected from the Connection list and **Custom** is selected from the Database Type list.

</td></tr><tr><td>

Connection URL

</td><td>

URL that the MID Server uses to connect to the specified database. The URL is created automatically when you save the form, and is read-only for the default databases. This field is available when **Define Connection Inline** is selected from the Connection list and **Custom** is selected from the Database Type list.

</td></tr><tr><td>

MID Application

</td><td>

Application that the MID Server must support to be eligible for selection. This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Capabilities

</td><td>

Capability of the MID Server. Select**JDBC**. This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Connection Timeout

</td><td>

Maximum elapsed time, in seconds, for the activity to wait while attempting to connect to the target database. This field is available when **Define Connection Inline** is selected from the Connection list.**Note:** Avoid setting the **Connection Timeout** value to zero, as this may cause a stale connection.

</td></tr><tr><td>

Query Timeout

</td><td>

Maximum elapsed time, in seconds, that the query is allowed to run without a response. This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td colspan="2">

JDBC Configuration

</td></tr><tr><td>

SQL Statement

</td><td>

SQL statement that the step executes.**Note:** When you use data pills in step SQL statements, sanitize them first using a preprocessing [Script step](javascript-step-action-designer.md). For more information, see [Sanitizing inputs using the escape functions](jdbc-step.md#section_gqd_cy4_qhb).

</td></tr><tr><td>

Maximum Rows

</td><td>

Maximum number of rows to be returned from the SQL statement. The default value is **1000**.

</td></tr><tr><td>

Maximum Payload Size \(KB\)

</td><td>

Maximum allowable payload size, in KB, to be returned from the SQL statement. The default payload size is **5120 KB**. The maximum payload size is **10 MB**.

</td></tr><tr><td>

Test JDBC Step

</td><td>

Test the JDBC step. View test results directly in the Test JDBC Step window. For more information, see [Test JDBC step](../task/test-jdbc-step.md).

</td></tr><tr><td colspan="2">

Retry Policy

</td></tr><tr><td>

Enable Retry Policy

</td><td>

Option to enable the retry policy. For more information, see [Retry policy](../concept/retry-policy.md#).

</td></tr><tr><td>

Override Default Policy for Alias

</td><td>

Option to override the default retry policy. This option is not applicable when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Retry Policy

</td><td>

Default retry policy associated with **Connection Alias**. If **Override Default Policy for Alias** is selected, you can override the default retry policy and select another existing retry policy based on your requirement.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


-   **[Test JDBC step](../task/test-jdbc-step.md)**  
Test the JDBC step before testing or publishing an action that contains the JDBC step.

**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

