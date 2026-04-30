---
title: Specify requirement for signed SOAP requests
description: Use a SOAP security policy to specify whether the instance requires signed SOAP requests for all inbound SOAP traffic.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Specify requirement for signed SOAP requests

Use a SOAP security policy to specify whether the instance requires signed SOAP requests for all inbound SOAP traffic.

## Before you begin

Role required: web\_service\_admin or admin

## About this task

By default, all inbound SOAP traffic must be signed. Administrators may want to disable this policy and allow unsigned SOAP requests to ServiceNow web services.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **SOAP Security Policies**.

2.  Select the **Default Policy**.

3.  Clear the **Required to Sign SOAP Request** check box \(selected by default\) to disable the requirement.

4.  Click **Update**.


**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

