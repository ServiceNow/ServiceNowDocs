---
title: Install the ServiceNow Live Connect ODBC driver on a client machine
description: Use the installation wizard to install the ODBC driver and configure the connection between your Business Intelligence tools and ServiceNow data.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/install-odbc-driver.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Install the ServiceNow Live Connect ODBC driver on a client machine

Use the installation wizard to install the ODBC driver and configure the connection between your Business Intelligence tools and ServiceNow data.

## Before you begin

-   Verify that your client machine meets the system requirements listed in [Download the Live Connect drivers on a client machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/download-sql-api-drivers.md).
-   Verify that you have OAuth Application Registry configured if you plan to connect using OAuth instead of basic authentication. See [Enable OAuth for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/enable-oauth-for-live-connect.md).

Role required: local administrator on client machine for installation, admin on ServiceNow instance for server-side configuration.

## Procedure

1.  Locate the downloaded ODBC driver installation file on your client machine.

2.  Select and hold \(or right-click\) the appropriate installation file based on your BI tool’s architecture \(32-bit or 64-bit\) and select **Run as administrator**.

    The ServiceNow ODBC Driver Setup wizard opens.

3.  Follow the wizard prompts to accept the license agreement and select the installation location.

    The default installation path is `C:\Program Files\ServiceNow\ODBC`.

4.  When prompted for the **Service Name**, enter a name to identify the service \(for example, ServiceNow\_ODBC\) and select **Next**.

5.  When prompted for the **Java Virtual Machine Location**, select **Browse** and navigate to the `bin\server` directory of your JDK installation and select the `jvm.dll` file.

    Example path: `C:\Program Files\Eclipse Adoptium\jdk-17.0.19.10-hotspot\bin\server\jvm.dll`

    \[Omitted image "sql-api-jvm-location.png"\] Alt text: Browse for JVM Location dialog showing bin\\server folder structure

    **Note:**

    The `jvm.dll` file location is required for the driver to work. You can enter it now or configure it later by navigating to **ServiceNow Live Connect - ODBC Manager** &gt; **Management Console** &gt; **Services** &gt; **\(Service\_Name\)** &gt; **Service Settings** &gt; **IP Parameters** and entering the path in the **ServiceJVMLocation** property.

6.  When prompted to create the ODBC data source, either accept the default values or customize the following fields:

    |Field|Description|
    |-----|-----------|
    |**Data Source Name**|Name to identify this data source.|
    |**Description**|Description of the data source.|
    |**Service Name**|Service name entered earlier in the wizard.|
    |**Service Data Source**|Data source name used in the ODBC Data Source administrator.|

7.  Accept the default program folder or select a custom location, then select **Next**.

8.  Review the installation summary and select **Next** to begin the installation, then select **Finish** when complete.


## Result

The installation creates a ServiceNow Live Connect - ODBC Manager folder in the Start menu with these applications:

-   **Interactive SQL \(ODBC\)**: Interactive SQL command window for testing SQL statements.
-   **Management Console**: Microsoft MMC snap-in for configuring ODBC driver properties.
-   **ODBC Administrator**: Microsoft ODBC administrator program \(searchable as **ODBC Data Sources**\).

The ServiceNow ODBC driver is installed on your client machine and registered with the Windows ODBC Data Source administrator.

**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/configuring-sql-api.md)

