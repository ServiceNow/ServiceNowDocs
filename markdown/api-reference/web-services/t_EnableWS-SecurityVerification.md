---
title: Enable WS-Security verification
description: Administrators can enable Web Services Security \(WSS\) verification from the Web Services system properties.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Enable WS-Security verification

Administrators can enable Web Services Security \(WSS\) verification from the Web Services system properties.

## Before you begin

Role required: web\_service\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Properties**.

2.  For **Require WS-Security header verification for all incoming SOAP requests**, select **Yes**.

    ![Require WS-Security header verification](../image/RequireWS-Security.png)

    **Note:** Selecting this option enables WS-Security for all inbound SOAP requests. It is not possible to enable WS-Security for only some requests.

3.  Click **Save**.

4.  Create a [WS-security profile](t_CreateANewWS-SecurityProfile.md).

5.  Update the user record for the [Mid Server](https://www.servicenow.com/docs/access?context=t_SetupMIDServerRole&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [ODBC driver](../../odbc-driver/concept/c_ODBCDriver.md) to [mark these users as internal integration users](t_MarkSvcAcctsAsInternalIntegUsers.md).

6.  Download and install the latest [MID Server](https://www.servicenow.com/docs/access?context=mid-server-installation&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [ODBC driver](../../odbc-driver/concept/c_ODBCDriver.md).

7.  To validate SOAP request signatures, upload the remote web service's certificate as a JKS and create the web service's WSS Username Token Profile.

    **Note:** Because ServiceNow WSS implementation does not verify the CA certificate, you do not need to upload the web service's CA certificate.


-   **[Mark service accounts as internal integration users](t_MarkSvcAcctsAsInternalIntegUsers.md)**  
Allow internal integration communications to bypass the WSS authentication requirement by marking their user accounts as internal integration users.

**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

**Related topics**  


[Basic authentication](../concept/c_SOAPWebService.md#SOAP-basic-auth)

