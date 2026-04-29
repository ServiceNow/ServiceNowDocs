---
title: Use forms to limit or extend the query response
description: On occasion, there is a need to limit the number of field values that a SOAP query returns.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Use forms to limit or extend the query response

On occasion, there is a need to limit the number of field values that a SOAP query returns.

You can use a form view to limit the number of field values returned by a SOAP query. Specifying a form view has the effects of:

1.  Limiting the response elements to contain only the fields on the view.
2.  Specifying reference record field values from referenced fields such as **caller\_id.email**. This causes the value of the caller's email to be returned in the SOAP response.

To enable form views for SOAP queries, configure the **com.glide.soap.view** property to contain the name of the view that you want to use for all SOAP query responses. The default is **soap\_response**. You can also specify the view name as a URL parameter, **sysparm\_view=&lt;view name&gt;**, when making the SOAP call. For example:

```
https://<instance name>.service-now.com/incident.do?SOAP&sysparm_view=ess

```

By default, if a specified view name does not exist, the response contains all fields.

**Parent Topic:**[Direct web services](c_DirectWebServices.md)

**Related topics**  


[Return the display value for reference variables](return-display-reference-variables.md)

[Clear values from a target instance](clearing-values-target.md)

[Retrieve journal entries using direct web services](retrieving-journal-entries.md)

[Retrieve choice fields using direct web services](retrieving-choice-fields-direct-ws.md)

[Persist an HTTP session across all SOAP calls](persist-session-all-soap-calls.md)

[SOAP direct web service API functions](../../web-services-apis/reference/r_DirectWebServiceAPIFunctions.md)

