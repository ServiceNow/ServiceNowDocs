---
title: Enable HTTP compression
description: By default, the SOAP request is accepted un-compressed and the result of the request is returned un-compressed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/c\_EnablingHTTPCompression.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
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

**Parent Topic:**[SOAP web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_SOAPWebService.md)

