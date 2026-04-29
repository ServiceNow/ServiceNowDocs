---
title: Install an ODBC driver patch
description: Use ServiceNow patches to install incremental ODBC fixes that occur between major ODBC releases.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Installing the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Install an ODBC driver patch

Use ServiceNow patches to install incremental ODBC fixes that occur between major ODBC releases.

## Before you begin

Before applying a new ODBC driver patch, do the following actions:

-   Ensure that you have the Java Runtime Environment \(JRE\) already installed in your instance.
-   Close any applications currently using the ODBC driver.

You must have administrator-level access for the Windows computer that you want to install the ODBC driver patch on.

Role required: admin

## About this task

Incremental ODBC patches contain only fixes to the ODBC driver and do not include fixes for third-party products such as Progress SDK. Third-party product fixes are included only in major ODBC release updates.

## Procedure

1.  Download and unzip the ODBC patch zip file from [KB0540707](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsysparm_article%3DKB0540707%26sysparm_stack%3D%26sysparm_view%3D) in the ServiceNow Knowledge Base.

2.  Extract the zip files into a folder named `odbc-patch`.

3.  From the **Start** menu, right-click **Command Prompt** and select **Run as administrator**.

4.  In the Command Prompt window, `cd` to the `odbc-patch` folder created in step 2, type `update.bat`, and press **Enter**.

    The installer prompts for the installation directory of the ODBC driver. The default installation location is `C:\Program Files\ServiceNow\ODBC`.

5.  Do one of the following actions if the ODBC driver is installed or not installed in the default installation location.

    -   If the ODBC driver is installed in `C:\Program Files\ServiceNow\ODBC`, enter **y** and press **Enter**.
    -   If the ODBC driver is not installed in `C:\Program Files\ServiceNow\ODBC`, enter the complete path to the ODBC installation directory and press **Enter**.
    The installer validates the installation location. If the location specified is not valid, the installer prompts for the correct location of the installed ODBC driver.

    Once you enter a valid installation location, the installer checks for the installed version and compares it with the version of the patch.

    -   If the currently installed version is the latest version, the installer aborts the installation process and displays the following message:

        ```
        The version you are trying to install is same as the existing version. Installation aborted.
        ```

    -   If the currently installed version is the same as the patch version, the installer aborts the installation process and displays the following message:

        ```
        The current installed version is the most recent version. Installation aborted.
        ```

    -   If the patch version is the latest version, the installer continues with the patch installation. After the installation is complete, you receive the following confirmation message:

        ```
        Patch is successfully installed.
        ```


**Parent Topic:**[Installing the ODBC driver](../concept/c_InstallingTheODBCDriver.md)

