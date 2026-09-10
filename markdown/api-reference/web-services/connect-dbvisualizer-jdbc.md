---
title: Connect DB Visualizer to JDBC driver
description: Connect the DB Visualizer database tool to your ServiceNow instance using the JDBC driver to query ServiceNow data. Access authorized tables and perform read-only queries on your ServiceNow data to create visualizations, and perform ad-hoc analysis using industry-standard SQL commands.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/connect-dbvisualizer-jdbc.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrate, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Connect DB Visualizer to JDBC driver

Connect the DB Visualizer database tool to your ServiceNow instance using the JDBC driver to query ServiceNow data. Access authorized tables and perform read-only queries on your ServiceNow data to create visualizations, and perform ad-hoc analysis using industry-standard SQL commands.

## Before you begin

-   The Live Connect plugin is installed on your ServiceNow instance.
-   The ServiceNow JDBC driver is installed and configured on your client machine.
-   You have a personal user account or service account with the **sn\_jdbc\_rest\_access** role assigned.
-   Access Control Lists \(ACLs\) are configured for the tables you must query.
-   IP filter criteria are configured to allow connections from your client machine.
-   Select your authentication method:

<table><thead><tr><th>

Authentication method

</th><th>

Usage

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Basic Authentication

</td><td>

Use to authenticate with a user account \(personal or service account\). Service accounts are recommended for production.

</td><td>

-   Complete steps 4–7
-   skip steps 8–9


</td></tr><tr><td>

OAuth

</td><td>

Use to authenticate with OAuth credentials

</td><td>

Skip steps 4–7 and complete steps 8–9

</td></tr></tbody>
</table>
Role required: admin

## About this task

**Note:**

Step-by-step instructions for third-party tools are illustrative. Consult tool-specific documentation for the latest updates. DB Visualizer is solely used as an example.

## Procedure

1.  Open DB Visualizer on your client machine.

2.  Navigate to **Tools** &gt; **Driver Manager**.

3.  Select the **+** \(plus\) icon to create a custom driver entry, and then select **Custom**.

4.  In the Database connection dialog box, configure the driver settings.

    1.  In the **Name** field, enter a name for the driver \(for example, SN Driver 1\).

    2.  Attach the ServiceNow JDBC driver JAR file by selecting the **+** icon on the right side of the screen.

        The system auto-detects the **Driver Class** value \(`com.snc.db.jdbc.JDBCDriver`\). Your new driver entry is created in DB Visualizer.\[Omitted image "sql-api-dbvisualizer-1.png"\] Alt text: DB Visualizer UI screen to enter your name and driver class.

5.  In the left panel under **User Drivers**, right-click your newly created driver entry \(SN Driver 1\) and select **Create Database Connection**.

    Alternatively, select the **+** icon in the connection panel.\[Omitted image "sql-api-dbvisualizer-4.png"\] Alt text: DB Vizualizer UI screen to connect the driver.

6.  Select and double-click \(or use the keyboard shortcut\) the newly created driver \(SN Driver 1\).

7.  In the Connection window, configure the connection details for basic authentication.

    **Note:** Skip this step if you're using OAuth; proceed to step 8.

    1.  In the **Database URL** field, enter the JDBC connection string for your ServiceNow instance:

        ```
        jdbc:servicenow://https://<servicenow_instance_url>.service-now.com 
        ```

        Replace `<servicenow_instance_url>` with your instance name. For example, if your instance is `exampleinstance.service-now.com`, enter `exampleinstance`.

    2.  In the **Database Userid** field, enter the user ID of your personal account or service account.

        \[Omitted image "sql-api-dbvisualizer-2.png"\] Alt text: DB Visualizer UI screen to configure the connection properties and test the connection.

    3.  In the **Database Password** field, enter the password for your personal account or service account.

8.  Select the **Properties** tab and configure the driver properties to connect via OAuth.

    **Note:** Complete this step only if you selected OAuth as your authentication method; skip if using basic authentication.

    1.  Enter the following OAuth properties obtained from your ServiceNow OAuth Application Registry:

        -   **oauthclientid** — Client ID from OAuth Application Registry
        -   **oauthclientsecret** — Client Secret from OAuth Application Registry
        -   **oauthrefreshtoken** — Refresh token for obtaining new access tokens
    2.  Set the **useoauth** property value to `true`.

        For detailed OAuth setup instructions, see [Enable OAuth for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/enable-oauth-for-live-connect.md).

9.  Select **Connect**.

    If the connection is successful, DB Visualizer displays a confirmation message and the available ServiceNow tables appear in the database tree.

10. Navigate to **SQL Commander** &gt; **New SQL Commander**, select the driver and database, and run your query.

    \[Omitted image "sql-api-dbvisualizer-3.png"\] Alt text: DB Visualizer UI screen to run your SQL query.


## Result

You have successfully connected DB Visualizer to your ServiceNow instance using the JDBC driver. You can now query authorized ServiceNow tables using SQL commands in DB Visualizer. The connection respects all ServiceNow Access Control Lists \(ACLs\) and security policies configured for your user account.

**Parent Topic:**[Integrate Live Connect Drivers with third-party BI tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configure-drivers-bi-tools.md)

