---
title: Upgrade the ODBC driver
description: If you have previously installed an older version of the ODBC driver, run the installer to uninstall the previous version, and then run the installer again to upgrade.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Installing the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Upgrade the ODBC driver

If you have previously installed an older version of the ODBC driver, run the installer to uninstall the previous version, and then run the installer again to upgrade.

## Before you begin

Role required: admin

## About this task

To check the build date and time of the ODBC driver, use **CheckVersion** located in the `Service-Now\ODBC\ip\tools` folder. This executable Windows host script reports the build date and time of the current ODBC driver. Use it to assist ServiceNow Technical Support to determine which build of the ODBC driver is running. If the **CheckVersion** tool is absent, the ODBC driver is out of date. Upgrade to the current version. To check the version of an older ODBC driver, see the previous version information.

**Note:** The ODBC installation also has a `Service-Now\ODBC\tools` folder, which is not the correct path for the CheckVersion tool.

## Procedure

1.  Right-click the executable and select **Run as Administrator**.

    ![ODBC Remove.](../image/OdbcRemove.png)

2.  Click **OK** when prompted to uninstall the current driver, which is required for the upgrade.

    A list appears, displaying the existing ODBC DSN names that you have previously created. You have the option to delete them.

3.  Select **Yes** to remove all previous DSNs or **No** to keep them for use with the upgraded driver.

    An ODBC DSN is a connection handle to use the ODBC driver in an application. For more information from Microsoft, see [Administer ODBC data sources](http://office.microsoft.com/en-us/access-help/administer-odbc-data-sources-HA010275550.aspx).

    ![ODBC Remove DSN.](../image/OdbcRemoveDsn.png)

4.  After removing the previous ODBC driver, double-click the executable again to run the installer and then follow the steps in [Download and install the ODBC driver](t_DownloadAndInstallTheODBCDriver.md).

    If you encounter errors when uninstalling the ODBC driver, see the [Troubleshooting uninstalling ODBC driver](https://support.servicenow.com/kb_view.do?sysparm_article=KB0539014) knowledge article.


## What to do next

After installing the ODBC driver, configure it to connect to your ServiceNow instance.

**Parent Topic:**[Installing the ODBC driver](../concept/c_InstallingTheODBCDriver.md)

