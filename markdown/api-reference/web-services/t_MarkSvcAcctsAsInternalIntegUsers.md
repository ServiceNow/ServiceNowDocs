---
title: Mark service accounts as internal integration users
description: Allow internal integration communications to bypass the WSS authentication requirement by marking their user accounts as internal integration users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/t\_MarkSvcAcctsAsInternalIntegUsers.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enable WS-Security verification, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Mark service accounts as internal integration users

Allow internal integration communications to bypass the WSS authentication requirement by marking their user accounts as internal integration users.

## Before you begin

Role required: admin

## About this task

When WS-Security is enabled, authentication is required for all SOAP requests including internal integration communications such as the MID Server, ODBC Driver, Remote Update Sets, and high availability cloning. SOAP requests for these internal integration communications cannot implement WS-Security due to technical implications. If your instance uses these SOAP interfaces, you can allow them to bypass the WS-Security authentication requirement by marking their user accounts as internal integration users.

**Note:** Any web services other than ODBC, MID Server, Remote Update Sets, or high availability cloning must implement WS-Security headers when WS-Security is enabled.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Select the user account for the MID Server or ODBC Driver.

3.  Configure the form to add the **Internal Integration User** field.

4.  Select the **Internal Integration User** check box.

5.  Click **Update**.


**Parent Topic:**[Enable WS-Security verification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_EnableWS-SecurityVerification.md)

**Related topics**  


[Enable WS-Security verification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_EnableWS-SecurityVerification.md)

[WS-Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_SOAPWebService.md)

