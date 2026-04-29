---
title: Create data sources from other apps using ODBC driver
description: The ServiceNow open database connectivity \(ODBC\) driver provides read-only access to the database associated with your ServiceNow instance.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Create data sources from other apps using ODBC driver

The ServiceNow open database connectivity \(ODBC\) driver provides read-only access to the database associated with your ServiceNow instance.

**Note:** Versions of the ODBC driver older than 2.1.1 are no longer supported.

The ODBC driver is compliant to version 3.52 of the Microsoft ODBC core API conformance. The ServiceNow ODBC driver uses ServiceNow web services support for a query-only interface. The ODBC driver supports only select statements or read-only functions and does not modify your instance data. Because the ODBC driver uses the web services interface, platform-wide access control \(ACL\) is enforced and data security is in place.

**Note:**

The ODBC driver has these limitations:

-   The ODBC driver supports only select statements or read-only functions, and does not modify your instance data.
-   There is no supported way to use the ODBC driver with a Java client application or with a Java JDBC-ODBC bridge.
-   There is a hard-coded limit of 512 characters when accessing views through ODBC. Because of this limitation, a maximum of 11 table sys\_ids can be included in an ODBC view query. Anything over 11 tables results in an error.

-   **[Getting started with ODBC](c_GettingStartedWithODBC.md)**  
Before installing the ODBC driver, create an ODBC user account, assign the odbc role, and define an ACL rule for the odbc role.
-   **[Installing the ODBC driver](c_InstallingTheODBCDriver.md)**  
Review setup requirements, download the ODBC driver installer, and install the ODBC driver to a computer.
-   **[Configuring the ODBC driver](configuring-odbc.md)**  
After installing the ODBC driver, configure it to connect to your ServiceNow instance and to communicate through a proxy server, if applicable, and set properties to control ODBC behavior.
-   **[Test the ODBC driver](../task/t_TestingTheODBCDriver.md)**  
After configuring the ODBC driver, test that the driver can connect to the base instance as the ODBC user and can query data from a target table.
-   **[ODBC behavior](../reference/r_ODBCBehavior.md)**  
After testing the ODBC driver, you can use it to query your instance database from a variety of client applications.
-   **[ODBC and client applications](../reference/r_ODBCAndClientApplications.md)**  
See the following pages for examples of how to use the ODBC driver to create data sources from other applications.
-   **[Domain separation and ODBC driver](domain-separation-odbc-driver.md)**  
This is an overview of domain separation and ODBC drivers.Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Additional integration resources](../../outbound-web-services/concept/additional-integration-resources.md)

