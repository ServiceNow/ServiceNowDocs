---
title: Connect DB Visualizer to JDBC driver
description: Connect the DB Visualizer database tool to your ServiceNow instance using the JDBC driver to query ServiceNow data. Access authorized tables and perform read-only queries on your ServiceNow data to create visualizations, and perform ad-hoc analysis using industry-standard SQL commands.
locale: en-us
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate, Access your ServiceNow data using SQL API, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Connect DB Visualizer to JDBC driver

Connect the DB Visualizer database tool to your ServiceNow instance using the JDBC driver to query ServiceNow data. Access authorized tables and perform read-only queries on your ServiceNow data to create visualizations, and perform ad-hoc analysis using industry-standard SQL commands.

## Before you begin

Before you begin, verify the following prerequisites are in place:

-   The SQL API plugin is installed on your ServiceNow instance.
-   The ServiceNow JDBC driver is installed and configured on your client machine.
-   You have a Service Account with the **sn\_jdbc\_rest\_access** role assigned.
-   Access Control Lists \(ACLs\) are configured for the tables you must query.
-   IP filter criteria are configured to allow connections from your client machine.

Role required: admin

## About this task

**Important:**

Step-by-step instructions for external tools in this guide are illustrative — you must consult tool-specific documentation for latest updates. DB Visualizer is solely used as an example in this guide.

## Procedure

1.  Open DB Visualizer on your client machine.

2.  Navigate to **Tools** &gt; **Driver Manager**.

3.  Select the **+** icon to create driver and select **Custom**.

4.  In the Database connection dialog box, configure the driver settings.

    1.  In the **Name** field, enter a name for the driver \(for example, SN Driver 1\).

    2.  Attach the ServiceNow JDBC driver JAR file that you downloaded and configured on your client machine by selecting the **+** icon on the right side of the screen.

        The Driver Class loads automatically and your new driver is created in DB Visualizer.![DB Visualizer UI screen to enter your name and driver class.](../image/sql-api-dbvisualizer-1.png)

5.  Select the **+** icon to create a connection.

    ![DB Vizualizer UI screen to connect the driver.](../image/sql-api-dbvisualizer-4.png)

6.  Select and double-click \(or use the keyboard shortcut\) the newly created driver \(SN Driver 1\).

    The Connection window opens.

7.  Configure the connection properties.

    1.  In the **Database URL** field, enter the JDBC connection string for your ServiceNow instance in the format: `jdbc:servicenow://https://<servicenow_instance_url>.service-now.com`

    2.  In the **Database Userid** field, enter the User ID of your Service Account.

    3.  In the **Database Password** field, enter the password for your Service Account.

        ![DB Visualizer UI screen to configure the connection properties and test the connection.](../image/sql-api-dbvisualizer-2.png)

8.  Select **Connect**.

    If the connection is successful, DB Visualizer displays a confirmation message and you can see the available ServiceNow tables in the database tree.

9.  Navigate to **SQL Commander** &gt; **New SQL Commander**, select the driver and database, and run your query.

    ![DB Visualizer UI screen to run your SQL query.](../image/sql-api-dbvisualizer-3.png)


## Result

You have successfully connected DB Visualizer to your ServiceNow instance using the JDBC driver. You can now query authorized ServiceNow tables using SQL commands in DB Visualizer. The connection respects all ServiceNow Access Control Lists \(ACLs\) and security policies configured for your Service Account.

**Parent Topic:**[Integrate SQL API Drivers with external BI tools](../reference/configure-drivers-bi-tools.md)

