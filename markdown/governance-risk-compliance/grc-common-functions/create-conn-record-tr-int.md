---
title: Establish an SFTP or REST API connection
description: Establish an SFTP or REST API connection for the GRC integration with Thomson Reuters Regulatory Intelligence application. You can create an SFTP or REST API connection with the SFTP server by using the Connection &amp; Credential aliases that are shipped with the Thomson Reuters platform.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration with Thomson Reuters Regulatory Intelligence \(TRRI\), GRC integrations, Common GRC features, Governance, Risk, and Compliance]
---

# Establish an SFTP or REST API connection

Establish an SFTP or REST API connection for the GRC integration with Thomson Reuters Regulatory Intelligence application. You can create an SFTP or REST API connection with the SFTP server by using the Connection &amp; Credential aliases that are shipped with the Thomson Reuters platform.

## Before you begin

Role required: sn\_grc\_reg\_change.admin

## About this task

Thomson Reuters deposits the regulatory feed files at the SFTP location that is configured in Thomson Reuters portal. To import the feed files from the SFTP location into the ServiceNow instance, you can create a connection with this SFTP server.

## Procedure

1.  Navigate to **All** &gt; **Regulatory Change Management** &gt; **Thomson Reuters** &gt; **Connection &amp; Credential Aliases**.

    The following two Connection &amp; Credential aliases are shipped with the Thomson Reuters platform:

    -   The Thomson Reuters platform REST API
    -   The Thomson Reuters platform SFTP
2.  In either the Thomson Reuters platform REST API alias or the Thomson Reuters platform SFTP alias, select the **Create New Connection &amp; Credential** related link.

    You can create a connection with either the REST alias or the SFTP alias, but not both. The details to be provided in the SFTP alias and the REST alias are different from each other.

    When you enter the details in the Create Connection &amp; Credential alias form, a new connection is created.

3.  On the form, fill in the fields.

    -   If you selected the Create Connection &amp; Credential SFTP alias form, then fill in the following fields.

        |Field|Description|
        |-----|-----------|
        |Connection information|
        |Name|Name of the SFTP connection.|
        |Host|Information about the SFTP server host.|
        |Port|Port number of the SFTP server.|
        |Credential information|
        |Name|Credential name that is used to access the SFTP server.|
        |User Name|User name that is used to access the SFTP server.|
        |Password|Password that is used to access the SFTP server.|
        |Post processing information|
        |Source path|Location of the directory that contains the regulatory feed files.|
        |Destination path|Location of the directory where the successfully imported files are placed.|

    -   If you selected the Create Connection &amp; Credential REST alias form, then fill in the following fields.

        |Field|Description|
        |-----|-----------|
        |Credential information|
        |OAuth client ID|Client ID of the application that is registered in the third-party OAuth OIDC server.|
        |OAuth client secret|Client secret ID of the application that is registered in the third-party OAuth OIDC server.|

4.  Depending on your previous step, select either **Create** in the SFTP alias form or select **Create and Get OAuth Token** in the REST alias form.

    The File Connection Information record is created.


## Result

When a new connection is established, a file connection information record is created in the instance. After the file connection information record is created, you can no longer create more file connection information records by selecting **New** in the Connections related list.

**Parent Topic:**[GRC integration with Thomson Reuters Regulatory Intelligence](../concept/grc-trri-integration.md)

