---
title: Perform export steps
description: Export a file from a local source, a remote network server, or another instance by providing a path and authentication information.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Procurement File Transfer Framework, Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Perform export steps

Export a file from a local source, a remote network server, or another instance by providing a path and authentication information.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Procurement Integrations** &gt; **File Transfer Setup** &gt; **FTP Integration Configurations**.

2.  Select **New**.

3.  Select one of the following operations:

    -   Post Purchase Order
    -   Post Catalog Error
    -   Post Shipment Error
    -   Post Invoice Error
    -   Post Price Error
    -   Post Availability Error
4.  Provide **Mid server** connection and path details.

    The MID Server facilitates communication and the movement of data between a ServiceNow instance and external applications, data sources, and services. For more information on the MID server, see the related topics.

5.  Provide **FTP server** connection and path details.

    For more information on connection, path, and HTTP connection, see the related topics.

    Verify the accuracy of the data, identify any discrepancies, and share the errors with the reseller on the same FTP server. You may use flow designer to move the data from your instance to external applications.


-   **[Export data to the FTP server](export-data-ftp.md)**  
Export a file from a local source, a remote network server, or another instance by providing a path and authentication information.

**Parent Topic:**[Procurement File Transfer Framework](../concept/procurement-file-transfer-framework.md)

**Related topics**  


[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

[Introduction to credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)

