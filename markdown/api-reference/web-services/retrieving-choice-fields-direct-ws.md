---
title: Retrieve choice fields using direct web services
description: To retrieve or set choice fields, use the choice Value, not the Label.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/retrieving-choice-fields-direct-ws.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Retrieve choice fields using direct web services

To retrieve or set choice fields, use the choice **Value**, not the **Label**.

For example, if you want to retrieve a list of all closed incidents, use the numerical value for **Closed**, which is **7** by default.

```
<state>7</state>
```

To see a list of choice values:

1.  Navigate to the form containing the choice field. For example, navigate to **Incident &gt; Open** and select an incident.
2.  Right-click the choice value field and select **Configure Dictionary**. For example, configure the dictionary for the **State** field.
3.  From the Choices related list, note the value for the label you want to query. For example, note that the **Closed** choice has a value of **7**.

**Parent Topic:**[Direct web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_DirectWebServices.md)

**Related topics**  


[Use forms to limit or extend the query response]()

[Return the display value for reference variables]()

[Clear values from a target instance]()

[Retrieve journal entries using direct web services]()

[Persist an HTTP session across all SOAP calls]()

[SOAP direct web service API functions]()

