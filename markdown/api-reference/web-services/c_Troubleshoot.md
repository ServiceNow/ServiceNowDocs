---
title: Troubleshoot a null response in a C Sharp integration
description: Receiving a null response from ServiceNow's web service.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [.NET tutorial, Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Troubleshoot a null response in a C Sharp integration

Receiving a null response from ServiceNow's web service.

If you are receiving a "null" response from your web service in your client code, then you may have missed the step in this tutorial for setting the elementFormDefault setting to "False".

Remember to recompile your code against the WSDL after you have changed this setting and saved it.

**Parent Topic:**[Web services C Sharp .NET end to end tutorial](c_CSharpNETEndEnd.md)

