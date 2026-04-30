---
title: ODBC driver installation requirements and supported software
description: Install the ServiceNow ODBC driver on Microsoft Windows computers.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Installing the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# ODBC driver installation requirements and supported software

Install the ServiceNow ODBC driver on Microsoft Windows computers.

## Installation requirements

Before installing the ODBC driver, ensure that your configuration meets these requirements.

<table id="table_rgj_hnz_jp"><thead><tr><th>

Category

</th><th>

Requirement

</th></tr></thead><tbody><tr><td>

Active user

</td><td>

The user record on the instance used to perform the queries.**Note:** The account used to connect to the instance via the ODBC driver must be defined on the instance. Accounts using single sign-on are not supported by the ODBC driver.

</td></tr><tr><td>

The soap\_query role

</td><td>

The user you use to query the database must have the soap\_query role if the instance uses the **glide.soap.strict\_security** high security setting.**Warning:** Do not enable WS-Security for all SOAP requests by setting the **glide.soap.require\_ws\_security** system property. It is incompatible with the ODBC driver. Enabling this setting blocks both ODBC driver and MID Server connections. Instead, use basic authentication.

</td></tr><tr><td>

Target Table ACLs

</td><td>

The user you use to query the database must have read access for the tables that you want to query. For example, a user with the itil role can read task tables, such as Incident.

</td></tr><tr><td>

Target Table Web Service Access

</td><td>

The table you want to query must allow web service interaction. You can enable web service interaction using the application access settings.

</td></tr><tr><td>

[ODBC Driver Dependencies \(2.0.1\)](https://store.servicenow.com/sn_appstore_store.do#!/store/application/072f46d11bf106103ee8a8ea234bcbd6/2.0.1)

</td><td>

[Download](https://store.servicenow.com/sn_appstore_store.do#!/store/application/072f46d11bf106103ee8a8ea234bcbd6) the ZIP files of bcpkix-fips-1.0.3.jar and bc-fips-1.0.2.4.jar mentioned in the dependencies file from [ServiceNow® Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) and extract the JARs to a local folder on your Windows machine.

</td></tr><tr><td>

Java Runtime Environment \(JRE\)

</td><td>

JRE must be enabled on your instance.

</td></tr><tr><td>

Java Development Kit \(JDK\)

</td><td>

version 11

</td></tr><tr><td>

Operating System

</td><td>

The ServiceNow ODBC driver supports installation on the following operating systems:-   Windows XP
-   Windows Server 2003
-   Windows Server 2008
-   Windows Server 2012
-   Windows Server 2016
-   Windows Server 2019
-   Windows Server 2022
-   Windows Vista
-   Windows 7
-   Windows 8
-   Windows 10

</td></tr><tr><td>

Hardware

</td><td>

-   RAM: 1 GB minimum
-   Disk space: 135 MB for installation, 200 MB for writing cache files during usage

</td></tr><tr><td>

Account

</td><td>

The Windows account used for the installation must have local Administrator rights to install an ODBC driver.

</td></tr><tr><td>

Networking

</td><td>

During usage, the ODBC driver requires HTTPS \(port 443\) connectivity to the ServiceNow instance. The communication between the ODBC driver and the ServiceNow instance uses standard SOAP web services for normal mode.

</td></tr><tr><td>

End User License Agreement

</td><td>

Read the End User License Agreement for the ServiceNow ODBC driver.

</td></tr></tbody>
</table>For more information, see [Application access settings](https://www.servicenow.com/docs/access?context=c_ApplicationAccessSettings&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## Supported software

The following table lists the operating systems and reporting applications compatible with each version of the ODBC driver.

<table id="table_zdn_m23_sr"><thead><tr><th>

Driver Version

</th><th>

Operating System

</th><th>

Microsoft Excel

</th><th>

Microsoft SQL Server

</th><th>

Crystal Reports

</th><th>

Tableau

</th><th>

Informatica

</th></tr></thead><tbody><tr><td>

1.0.13 and later

</td><td>

-   Windows XP SP2
-   Windows Vista
-   Windows 7
-   Windows 8.x
-   Windows 10
-   Windows Server 2003
-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016
-   Windows Server 2019
-   Windows Server 2022

</td><td rowspan="3">

-   2007
-   2010
-   2013
-   2016

</td><td rowspan="3">

-   2008
-   2012
-   2014
-   2019
-   2022
-   2023

</td><td rowspan="3">

-   2008
-   2011
-   2013

</td><td>

-   8.1
-   8.2
-   8.3
-   9.0

</td><td rowspan="3">

The ODBC driver provides only basic support for Informatica. Use the ODBC driver with Informatica only for simple operations. Thoroughly test integrations with Informatica before using them in a production environment.

</td></tr><tr><td>

1.0.9 - 1.0.12

</td><td>

-   Windows XP SP2
-   Windows Vista
-   Windows 7
-   Windows 8.x
-   Windows Server 2003
-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2

</td><td>

 

</td></tr><tr><td>

1.0.8 and earlier

</td><td>

-   Windows XP SP2
-   Windows Vista
-   Windows 7
-   Windows 8.x
-   Windows Server 2003
-   Windows Server 2008
-   Windows Server 2008 R2

</td><td>

8.1

</td></tr></tbody>
</table>**Parent Topic:**[Installing the ODBC driver](../concept/c_InstallingTheODBCDriver.md)

