---
title: Clear values from a target instance
description: You can pass an empty value through a SOAP parameter to clear the respective value in the target instance.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Direct web services, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Clear values from a target instance

You can pass an empty value through a SOAP parameter to clear the respective value in the target instance.

You can also pass an empty \(null\) value through the **&amp;allow\_empty\_value=true** SOAP query parameter to clear the respective value in the target instance.

For example, `https://<instance name>.service-now.com/incident.do?SOAP&allow_empty_value=true` lets you pass an empty value to the incident record in an instance.

You can then enter lines like the following in the SOAP request:

```
<assigned_to>value</assigned_to>
<assignment_group>value</assignment_group>
<category></category>
```

In the above example,

-   `<assigned_to>value</assigned_to>` changes the value in the **Assigned to** field to the value specified in the SOAP request.
-   `<assignment_group>value</assignment_group>` changes the value in the **Assignment group** field to the value specified in the SOAP request.
-   `<category></category>` clears the value in the **Category** field.

**Parent Topic:**[Direct web services](c_DirectWebServices.md)

**Related topics**  


[Use forms to limit or extend the query response](using-forms-limit-extend-query-resp.md)

[Return the display value for reference variables](return-display-reference-variables.md)

[Retrieve journal entries using direct web services](retrieving-journal-entries.md)

[Retrieve choice fields using direct web services](retrieving-choice-fields-direct-ws.md)

[Persist an HTTP session across all SOAP calls](persist-session-all-soap-calls.md)

[SOAP direct web service API functions](../../web-services-apis/reference/r_DirectWebServiceAPIFunctions.md)

