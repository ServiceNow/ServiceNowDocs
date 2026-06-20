---
title: Use the SQL component
description: Write custom SQL queries to perform various operations by using the SQL component in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/use-general-sql.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [General, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the SQL component

Write custom SQL queries to perform various operations by using the SQL component in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

You can configure the properties for the SQL component. For more information about these properties, see [Properties of the General components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/Properties-general-components.md).

## Procedure

1.  In the Toolbox pane, navigate to **General** &gt; **SQL**.

2.  Drag the SQL component to the Design surface.

3.  Click the component settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Component settings icon.\).

4.  Under the SCRIPT \(SQL\) heading, write the custom SQL query.

5.  To add a parameter to the query, do the following.

    1.  Click the add parameter icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add parameter icon.\).

    2.  Update the data type of the parameter.

    3.  Repeat the steps to add more parameters.

    A Data In Port is added with each parameter you add.

6.  Click **OK**.

7.  To configure the input fields, see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-input-port-properties.md).

8.  To close the PORT PROPERTIES dialog, click **OK**.

9.  Connect the data and control ports of the SQL component to the corresponding ports of the other component as described in the following table.

<table id="table_jnw_jn1_krb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port type

</th></tr></thead><tbody><tr><td>

Connection Provider

</td><td>

Takes the data table connection provider that enables an application to communicate with a database.-   **Example:**

SqlClient, MySqlClient

</td><td>

Data In

</td></tr><tr><td>

Connection String

</td><td>

Connection string helps in connecting to the required data source using the details, such as server name, username, and password. In the following connection strings for each authentication type, replace the placeholder parameter values \(for example, &lt;myUser&gt; and &lt;myPassword&gt;\) with actual values:-   **Example:**

For SQL authentication:

    ```
Server=<MY_SERVER>;Database=<MyDatabase>;User Id=<myUser>;Password=<myPassword>;
    ```

For Windows authentication:

    ```
Server=MY_SERVER;Database=MyDatabase;Trusted_Connection=True;
    ```

For Oracle database:

    ```
Data Source=MyTnsName;User Id=myUsername;Password=myPassword;
    ```

For MySQL database:

    ```
Server=MY_SERVER;Database=MyDatabase;User Id=myUsername;Password=myPassword;
    ```

For ODBC database:

    ```
Driver={SQL Server};Server=MY_SERVER;Database=MyDatabase;Uid=myUsername;Pwd=myPassword;
    ```

For OLEDB database:

    ```
Provider=SQLOLEDB;Data Source=MY_SERVER;Initial Catalog=MyDatabase;User Id=myUsername;Password=myPassword;
    ```

</td><td>

Data In

</td></tr><tr><td>

Parameter

</td><td>

Takes the value of the parameter from a previously executed component.

</td><td>

Data In

</td></tr><tr><td>

DataTable

</td><td>

Returns the data table and passes to the next component.

</td><td>

Data Out

</td></tr></tbody>
</table>10. To view the output, right-click the **Return** field and click **Preview Data**.

11. To test the component, under the **DESIGN** tab, click **Run**.


**Parent Topic:**[General](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/general-component.md)

