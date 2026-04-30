---
title: Data integration with Edge Encryption
description: To integrate third-party data with an instance using Edge Encryption, you must route the data through the Edge Encryption proxy server using supported integrations. Supported integrations use base system encryption rules that map data in each payload to fields in a table.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Data integration with Edge Encryption

To integrate third-party data with an instance using Edge Encryption, you must route the data through the Edge Encryption proxy server using supported integrations. Supported integrations use base system encryption rules that map data in each payload to fields in a table.

## Upload data to fields marked for encryption

Edge Encryption does not support importing data from or exporting data to Excel, CSV, XML, or other file types to or from fields with encryption configurations defined.

-   **ODBC driver**

    Encrypt requests and query data through the Edge Encryption proxy server using the ODBC driver.

    Learn more: [Edge Encryption ODBC driver integration](c_IntegrateODBCWithEdge.md#)

-   **MID Server**

    You can configure the MID Server to route data through an Edge Encryption proxy server. However, some restrictions apply.

    Learn more: [Edge Encryption MID Server integration](edge-mid-pass-through.md#)

-   **REST/SOAP web services**

    Use REST/SOAP web services to update or retrieve record data through the Edge Encryption proxy server.

    Learn more: [Web services](https://www.servicenow.com/docs/access?context=r_AvailableWebServices&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

-   **JSONv2 web service**

    Use JSONv2 web service APIs to update or retrieve record data through the Edge Encryption proxy server. Base system encryption rules support data retrieval and data modification APIs.

    -   To insert a single record using the data modification API, use the insert\(\) or insertMutiple\(\) methods.
    -   To insert multiple records using the data modification API, use the insertMultiple\(\) method.
    Learn more: [JSONv2 Web Service](https://www.servicenow.com/docs/access?context=c_JSONv2WebService&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)


To encrypt data from custom third-party integrations not listed above, create custom encryption rules. See [Define a custom encryption rule](c_EncryptionRules.md).

## Upload attachments to records marked for encryption

Attachments can be uploaded to tables with attachment encryption configured using REST and SOAP web services.

-   **[Edge Encryption ODBC driver integration](c_IntegrateODBCWithEdge.md#)**  
Configure your ODBC driver to query data encrypted by Edge Encryption. The Edge Encryption proxy server encrypts ODBC driver requests to the ServiceNow instance when Edge Encryption is integrated with the ODBC driver.
-   **[Edge Encryption MID Server integration](edge-mid-pass-through.md#)**  
Configure the MID Server to route data through an Edge Encryption proxy server.

**Parent Topic:**[Configuring Edge Encryption](edge-config.md)

