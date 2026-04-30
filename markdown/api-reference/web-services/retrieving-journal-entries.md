---
title: Retrieve journal entries using direct web services
description: To get the contents of a journal field, make a second soap request against the sys\_journal\_field table to pull the appropriate journal records back for the record in question.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Direct web services, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Retrieve journal entries using direct web services

To get the contents of a journal field, make a second soap request against the sys\_journal\_field table to pull the appropriate journal records back for the record in question.

The URL for the WSDL would be in the following format.

```
https://instance-name.service-now.com/sys_journal_field.do?WSDL

```

To retrieve the journal entries, you will first need to query the incident for its sys\_id value, and then supply it as the `element_id` value in a **getRecords** call. To specify records only for the **comments** field, specify the value `comments` for the **element** field. For example, a SOAP request would look like the following:

```
<soapenv:Envelope xmlns:soapenv= "http://schemas.xmlsoap.org/soap/envelope/" xmlns:sys= "http://www.service-now.com/sys_journal_field" ><soapenv:Header /><soapenv:Body><sys:getRecords><element>comments</element><element_id>9d385017c611228701d22104cc95c371</element_id></sys:getRecords></soapenv:Body></soapenv:Envelope>
```

**Parent Topic:**[Direct web services](c_DirectWebServices.md)

**Related topics**  


[Use forms to limit or extend the query response](using-forms-limit-extend-query-resp.md)

[Return the display value for reference variables](return-display-reference-variables.md)

[Clear values from a target instance](clearing-values-target.md)

[Retrieve choice fields using direct web services](retrieving-choice-fields-direct-ws.md)

[Persist an HTTP session across all SOAP calls](persist-session-all-soap-calls.md)

[SOAP direct web service API functions](../../web-services-apis/reference/r_DirectWebServiceAPIFunctions.md)

