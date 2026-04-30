---
title: Set up the Jack Henry jXchange spoke
description: Integrate ServiceNow and Jack Henry jXchange account by using the Jack Henry jXchange connection and credential record to authenticate ServiceNow requests.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Jack Henry jXchange Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Jack Henry jXchange spoke

Integrate ServiceNow and Jack Henry jXchange account by using the Jack Henry jXchange connection and credential record to authenticate ServiceNow requests.

## Before you begin

Role required: admin

## Procedure

1.  Log in to your ServiceNow instance as an admin.

2.  Navigate to **Integration Hub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

3.  Open the record, **JHA**.

4.  Click the **Create New Connection &amp; Credential** related link.

5.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |SOAP Connection URL|SOAP endpoint to connect to the Jack Henry jXchange account. Enter `https://jxdmz.jackhenry.com/jxchange/2008/ServiceGateway/ServiceGateway.svc`.|
    |Valid Consumer Name|Valid consumer name for provider.|
    |Valid Consumer Product|Valid consumer product for provider.|
    |Institute Routing ID|Institute Routing ID for provider.|
    |Institute Environment|Institute Environment for provider.|
    |User Name|User name to authenticate the outbound requests.|
    |Password|Password to authenticate the outbound requests.|

6.  Click **Create**.

7.  Navigate to **Integration Hub** &gt; **SOAP Security Policies**.

8.  Open the record, **JHA Security Policy**.

9.  For **WS-Security Username Profile**, select the credential record that is created for the Jack Henry jXchange spoke.

10. Click **Update**.


