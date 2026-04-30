---
title: Enable WS-Security for outbound SOAP
description: You can sign outbound SOAP messages using username and password or a key store and trusted server certificate saved on the instance.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Outbound SOAP security, Outbound SOAP web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Enable WS-Security for outbound SOAP

You can sign outbound SOAP messages using username and password or a key store and trusted server certificate saved on the instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **SOAP Message**.

2.  Select a SOAP message record.

3.  In the **SOAP Message Functions** related list, select a function.

4.  In the **WS-Security type** field select the type of credentials to use, such as Username or X.509.

    Some web service providers may require you to submit both types of credential.

5.  In the **WS-Security x.509 profile** or **WS-Security Username profile** field, select the profile that contains the credentials you want to use.

    If the record was configured with x.509 security prior to the Helsinki release, you can migrate the security settings to a WS-Security x.509 profile record by clicking the **Migrate to X509 Security Profile** button. When you click this button, security configuration field values \(**Key store**, **Certificate**, **Key store alias**, and **Password**\) are migrated to a new WS-Security x.509 profile record and that record is referenced from the SOAP message function. If an x.509 profile record already exists with matching values, that record is referenced.

    **Note:** Existing SOAP message functions that use the legacy security configuration will still work, however new records can use only an x.509 profile record for x.509 security.

6.  Click **Update**.

    Credentials from the selected profile are sent as part of the SOAP message header.


**Parent Topic:**[Outbound SOAP security](../concept/c_OutboundSOAPSecurity.md)

**Related topics**  


[Create a new WS-Security profile](../../inbound-soap/task/t_CreateANewWS-SecurityProfile.md)

