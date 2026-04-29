---
title: Override a SOAP endpoint
description: The SOAP endpoint address where the SOAP message is posted is consistent with the endpoint of the WSDL.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Override a SOAP endpoint

The SOAP endpoint address where the SOAP message is posted is consistent with the endpoint of the WSDL.

In some cases, however, the WSDL may reference an incorrect endpoint URL. If this happens, it is necessary to over-ride the generated URL by creating the property **com.glide.soap\_address\_base\_url** to contain the new URL. You may have to add the property manually as this is not an base system property.

For instance, a generated SOAP endpoint may look like this:

```
https://instance.service-now.com/incident.do?SOAP
```

You can specify a property to define the endpoint such that it goes through a proxy by setting the property:

```
com.glide.soap_address_base_url = "https://myproxy.mycompany.com/service-now/"
```

This will result in the endpoint being generated to appear as:

```
https://myproxy.mycompany.com/service-now/incident.do?SOAP

```

**Parent Topic:**[SOAP web service](c_SOAPWebService.md)

