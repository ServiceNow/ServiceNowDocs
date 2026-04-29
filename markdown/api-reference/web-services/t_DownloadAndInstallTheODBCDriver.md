---
title: Download and install the ODBC driver
description: Download the ODBC driver \(32-bit or 64-bit\) that is compatible with your computer's operating system from the ServiceNow Store.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Installing the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Download and install the ODBC driver

Download the ODBC driver \(32-bit or 64-bit\) that is compatible with your computer's operating system from the ServiceNow Store.

## Before you begin

-   Make sure that you have administrator-level access for the Windows computer that you want to install the ODBC driver on.
-   Role required: admin

## About this task

If this is the first time that the driver is installed, the installer is in first time installation mode and prompts for the driver to be installed. Install only one version of the ODBC driver on a computer. If the ODBC driver was previously installed, the installer is in upgrade mode and prompts for the removal of the previous driver first.

**Note:** Versions of the ODBC driver older than 2.1.1 are no longer supported.

## Procedure

1.  To download the latest ODBC drivers, click the following links:

    -   2.2.0 \(32-bit\) [download](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c847b9ffdb9c5050f20ff5471d9619d6)
    -   2.2.0 \(64-bit\) [download](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c847b9ffdb9c5050f20ff5471d9619d6)
2.  Download the ODBC driver version compatible with your computer's operating system and the application you are using to query the database.

    The ODBC driver is available as 32-bit or 64-bit. Most applications require the 32-bit ODBC driver even if the operating system is 64-bit.

3.  Right-click the executable and select **Run as Administrator** to launch the installer.

    The ODBC Driver Setup Wizard appears.

    ![f ODBC Driver Setup Wizard.](../image/OdbcStep1.png)

4.  Click **Next**.

5.  Read and accept the End User License Agreement.

    The installer prompts for the **Installation Directory**.

6.  Select the target directory for installing the ServiceNow ODBC driver.

    The default directory is `C:\Program Files\Service-now\ODBC`.

7.  When the prompted for the **Service Name**, enter a name to identify the service \(for example, `ServiceNow_ODBC`\) and press **Next**.

8.  When prompted for the **Java Virtual Machine Location**, do the following actions.

    -   Browse to and select the directory where the `jvm.dll` file is located \(usually `C:\Program Files\Java\jre<version>\bin\server`\).
    -   If you do not want to enter the JRE location at the time of the installation, click **Next**.

        On the popup window, click **Yes** to enter the JRE location now, or click **No** to enter the JRE location later.

        **Important:** You must specify the JRE location before the ODBC driver will work. After the installation, you can access the Management console as an administrator and navigate to **Services** &gt; **&lt;Service\_Name&gt;** &gt; **Service Settings** &gt; **IP Parameters** and enter the JRE location in the **ServiceJVMLocation** property.

    **Tip:** For the configuration of a Java service, ServiceNow strongly recommends using the server `jvm.dll` file from the Java Development Kit \(JDK\).

9.  When prompted for the **ODBC Data Source** details, specify the following parameters to create an ODBC data source that can be used to create a DSN.

    -   **Data Source Name**: A short name to identify this data source.
    -   **Description**: A short description of the driver. The driver's version number is appended to the end of this value.
    -   **Service Name**: Enter the same **Service Name** entered at step 7.
    -   **Service Data Source**: The name that can be selected in the **Service Data Source** field of the ODBC Administrator.
    Usually, the default values are appropriate.

    ![Service Configuration.](../image/OdbcStep5.png)

10. Under the Start menu, select the **Program Folder** to create links for the driver.

    ![ODBC Driver Setup - Select Program Folder.](../image/OdbcStep6.png)

    The installation creates the following links in the menu:

    -   **Interactive SQL \(ODBC\)**: An interactive SQL command window for directly testing SQL statements.
    -   **Management Console**: A Microsoft MMC snap-in for configuring default properties for the ODBC driver.
    -   **ODBC Administrator**: A Microsoft ODBC Administrator program.
    ![ODBC Program Menu.](../image/OdbcProgramMenu.png)

    The driver code is copied to the target folder.

    ![ODBC Driver Setup - Start Copying Files.](../image/OdbcStep7.png)

    A progress bar appears.

11. When prompted, click **Finish** to complete the installation.

12. Download the [ODBC Driver Dependencies \(2.0.1\)](https://store.servicenow.com/sn_appstore_store.do#!/store/application/072f46d11bf106103ee8a8ea234bcbd6/2.0.1) file from ServiceNow Store after the installation is successful.

    Then, extract the JARs \(bcpkix-fips-1.0.3.jar, bc-fips-1.0.2.4.jar\) to a local folder on your Windows machine. For example, `<Windows-machine-local-path>\<folder-name>`.

13. Navigate to **All** &gt; **ServiceNow ODBC** &gt; **Management Console** &gt; **ServiceNow ODBC Manager** &gt; **Manager \(local configuration\)** &gt; **&lt;drive&gt;:\\Program Files\\ServiceNow\\ODBC\\cfg\\adm.in** &gt; **Services** &gt; **ServiceNow\_ODBC** &gt; **Service Settings** &gt; **IP Parameters**.

14. Open the **ServiceJVMClassPath** parameter.

15. Append the value with the location where the **bc-fips-1.0.2.4.jar** and **bcpkix-fips-1.0.3.jar** JARs are extracted.

    For example, the location of jars will be in this format: `<Windows-machine-local-path>\<folder-name>\bc-fips-1.0.2.4.jar;<Windows-machine-local-path>\<folder-name>\bcpkix-fips-1.0.3.jar`


## Result

The ODBC driver application is ready for testing.

**Parent Topic:**[Installing the ODBC driver](../concept/c_InstallingTheODBCDriver.md)

