---
title: ODBC Driver release notes
description: Version history for the ODBC Driver in ancillary software on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-ancillary-software-odbc.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Integration Hub, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# ODBC Driver release notes

Version history for the ODBC Driver in ancillary software on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.2.0 - November 2024**

    Internal bug fixes.

-   **Version 2.1.1 - August 2024**

    Internal bug fixes and JDK 11 compatibility.

-   **Version 2.0.0 - May 2024**

    Internal bug fixes and JDK 11 compatibility.

-   **Version 1.0.15 - August 2020**
    -   Fixed:
        -   Supports parallel queries when connected to different instances through different data sources.
        -   When a column is made inactive, the column is shown in the result. Added a new config property to show/hide inactive fields.
-   **Version 1.0.14 - December 2018**
    -   Fixed:

        -   When a ServiceNow ODBC user types incorrect user credentials, 4 login.failed events are created instead of 1.
        -   An ODBC query to a 'string' with the value of a field name will translate to the incorrect 'same as' query, returning incorrect rows. When using ODBC to query to a 'string' that matches the value of a field name, it translates to an incorrect 'same as' query. The incorrect query can return the incorrect rows.
        -   The JRE was removed from ODBC installers.
        -   The 64-bit ODBC Driver fails to connect to instances hosted in FedRAMP datacenter due to TLSv1.2 requirements. FedRAMP data centers no longer allow for connections made with TLSv1.1 or lower. The 64-bit version of the 1.0.13 driver uses JDK 1.8.152, which has been known to have issues with TLS. As a result, the server rejects the connection when falling back to the next highest version. For symptoms, cause, and resolution information, see [KB0563593](https://support.servicenow.com/kb_view.do?sysparm_article=KB0563593) in the HI Knowledge Base.
        **Note:** The ODBC driver Version 1.0.14\_01 \(32-bit and 64-bit\) is available. ODBC 1.0.14 is a prerequisite to install ODBC 1.0.14\_01.

    -   Related information:
        -   Install an ODBC driver patch
        -   ODBC driver installation requirements and supported software
        -   Download and install the ODBC driver
-   **Version 1.0.13 - November 2017**
    -   Fixed: The ODBC driver returns non-integer fields as NTEXT where varchar is expected.
    -   Related information:
        -   ODBC driver installation requirements and supported software
        -   Setting ODBC properties
        -   Configure the ODBC driver for large data sets
-   **Version 1.0.12 - June 2017**
    -   Additional requirement: Version 1.0.12 of the ODBC Driver uses Java 1.8. You may need to configure your Java path after installing this version. See [KB0597981](https://support.servicenow.com/kb_view.do?sysparm_article=KB0597981) for more information.
    -   Fixed:
        -   Querying more than 4MB with ODBC driver creates temp files.
        -   The ODBC driver outputting incorrect number of records when using LEFT JOIN ON SELECT \* query.
-   **Version 1.0.11 - October 2016**
    -   Additional requirement: Version 1.0.11 of the ODBC Driver uses Java 1.8. You may need to configure your Java path after installing this version. See [KB0597981](https://support.servicenow.com/kb_view.do?sysparm_article=KB0597981) for more information.
    -   Fixed:
        -   When querying a table that has a string field whose value exceeds 65535 kb, the following error occurs: \[SN\]\[ODBC ServiceNow driver\]\[OpenAccess SDK SQL Engine\]Disk cache error. Field length:93238 exceeds maximum limit of 65535.
        -   The ODBC query on Display Value for a state does not return the entire Display Value.
        -   The iSQL returns only 16383 bytes even if a field contains more data.
-   **Version 1.0.10 - April 2016**
    -   New:
        -   Improvements to timer and duration fields. The display format for timer and duration fields has been improved. Queries on timer and duration fields now return the field value in the UTC timezone. You can query the field display value, as shown in the UI, by adding dv\_ to the field name. The property LegacyDurationTimeZone has been added to preserve compatibility with legacy integrations. Refer to [KB0583982](https://support.servicenow.com/kb_view.do?sysparm_article=KB0583982) for details.
        -   Database schema and caching properties. The EnableDBSchema and ExtendedSchemaCache properties enable you to control how the ODBC driver queries and caches database schemas. Refer to Setting ODBC properties for details.
    -   Fixed:
        -   The ODBC driver fails to get data or connect when invoking multiple or parallel connections.
        -   The ODBC select query does not return columns in the defined order.
        -   The ODBC driver caches schema between different connections.
        -   The ODBC driver does not use the SOAP aggregate API for aggregate queries.
        -   The ODBC driver does not optimize select top N queries.

**Parent Topic:**[ServiceNow Store - Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-integrationhub-landing.md)

