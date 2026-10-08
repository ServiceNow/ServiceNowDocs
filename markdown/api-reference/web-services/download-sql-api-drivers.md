---
title: Download the Live Connect drivers on a client machine
description: Download ODBC and JDBC drivers to enable third-party Business Intelligence tools and data analysis platforms to connect to your ServiceNow instance data.
locale: en-us
canonical_url: https://www.servicenow.com/docs/r/australia/api-reference/web-services/download-sql-api-drivers.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Access your ServiceNow data using Live Connect, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Download the Live Connect drivers on a client machine

Download ODBC and JDBC drivers to enable third-party Business Intelligence tools and data analysis platforms to connect to your ServiceNow instance data.

## Before you begin

Verify that your client machine meets the following requirements:

|Requirement|Description|
|-----------|-----------|
|Operating system|Windows with administrator permissions. For supported versions and troubleshooting guidance, see [Troubleshooting Live Connect — Connection, Authentication, and Query Errors](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2917911) \[KB2917911\] in the Now Support Knowledge Base.|
|Java Development Kit \(JDK\)|JDK 17. Using a different JDK version may cause installation or configuration issues.|
|Microsoft Visual C++ Redistributable|Required dependency for the ODBC driver.|

Role required: admin

## Procedure

1.  Navigate to [store.servicenow.com](https://store.servicenow.com).

2.  Search for `Live Connect`.

    The Live Connect tile appears in the search results.

3.  Select Live Connect.

    The download page appears.

    If the download page does not appear, verify that you selected the correct tile in the search results.

4.  Select **Download**.

    The ZIP file contains the following folders:

    |Folder|Contents|
    |------|--------|
    |`ServiceNow Live Connect - ODBC driver`|ODBC driver executables for 32-bit and 64-bit architectures, and a dependencies folder with BCFIPS JAR files.|
    |`ServiceNow Live Connect - JDBC driver`|JDBC driver JAR files.|


## Result

The Live Connect drivers are downloaded to your client machine and ready for installation and configuration.

**Parent Topic:**[Configuring Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/api-reference/web-services/configuring-sql-api.md)

