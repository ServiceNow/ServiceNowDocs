---
title: Create a SOAP message
description: Create a SOAP message to define the remote endpoint, WSDL, and authentication settings.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SOAP message, Outbound SOAP web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Create a SOAP message

Create a SOAP message to define the remote endpoint, WSDL, and authentication settings.

## Before you begin

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **SOAP Message**.

2.  Click **New**.

3.  Enter a Name to identify the SOAP message.

4.  Specify a WSDL using one of these options:

    -   To download and use an online WSDL source, select the **Download WSDL** check box and enter the URL for the WSDL in the WSDL field.
    -   To enter the WSDL directly, clear the **Download WSDL** check box, and then copy and paste the WSDL XML into the WSDL XML field.
5.  If the endpoint is protected by basic authentication, select the **Use basic auth** check box and enter the credentials.

6.  If the endpoint requires mutual authentication, select the **Enable mutual authentication** check box and select a Protocol profile to use for mutual authentication.

7.  Click **Submit**.

    This image shows an example of a SOAP message that connects to a demo instance of ServiceNow.

    ![Soap message demo 1](../image/SoapMessageDemoi1.png)


**Parent Topic:**[SOAP message](../concept/c_SOAPMessage.md)

