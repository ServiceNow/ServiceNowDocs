---
title: Enable HTTP compression
description: By default, the SOAP request is accepted un-compressed and the result of the request is returned un-compressed.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Enable HTTP compression

By default, the SOAP request is accepted un-compressed and the result of the request is returned un-compressed.

To enable HTTP compression using \[gzip\] when sending in your SOAP request, set the following HTTP header:

```
Content-Encoding: gzip
```

To receive the SOAP response compressed using \[gzip\] send in your SOAP request with the following HTTP header:

```
Accept-Encoding: gzip

```

**Parent Topic:**[SOAP web service](c_SOAPWebService.md)

