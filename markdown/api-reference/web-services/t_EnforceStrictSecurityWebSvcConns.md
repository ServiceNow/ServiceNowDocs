---
title: Enforce strict security for inbound SOAP
description: Strict security for web services requires that users meet Contextual Security requirements to access instance resources.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Enforce strict security for inbound SOAP

Strict security for web services requires that users meet Contextual Security requirements to access instance resources.

## Before you begin

Role required: admin

## About this task

**Note:** ServiceNow does not support digital certificates, digital signatures, or other digested token methods in SOAP web service calls.

To enforce strict security for web services connections:

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Web Services**.

2.  Select **Yes** for **Enforce strict security on incoming SOAP requests**.

    **Note:** To learn more about this property, see SOAP request strict security \(instance security hardening\) in Instance Security Hardening Settings.


**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

