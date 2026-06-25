---
title: Return the display value for reference variables
description: When you query a record using a get or getRecords function, the instance returns all fields associated with that record. The fields are often reference fields that contain a sys\_id for a record on another table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/return-display-reference-variables.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Return the display value for reference variables

When you query a record using a **get** or **getRecords** function, the instance returns all fields associated with that record. The fields are often reference fields that contain a sys\_id for a record on another table.

Use one of these options if you want the display value for the field to be returned instead of the sys\_id:

1.  Add the **glide.soap.return\_displayValue** property to your system properties, and every SOAP request will return a display value for a reference field.
2.  Add the **displayvalue=true** parameter to your SOAP request URL, and SOAP requests with that parameter will return a display value for a reference field as a string, instead of the sys\_id. The SOAP URL would look as follows: `https://<instance name>.service-now.com/incident.do?displayvalue=true&SOAP`.
3.  Add the **displayvalue=all** parameter to your SOAP request URL, and SOAP requests with that parameter will return a display value for a reference field, in addition to the sys\_id. The response element name for the display value field will be prefixed with `dv`, such as `dv_caller_id`.

**Parent Topic:**[Direct web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_DirectWebServices.md)

**Related topics**  


[Use forms to limit or extend the query response]()

[Clear values from a target instance]()

[Retrieve journal entries using direct web services]()

[Retrieve choice fields using direct web services]()

[Persist an HTTP session across all SOAP calls]()

[SOAP direct web service API functions]()

